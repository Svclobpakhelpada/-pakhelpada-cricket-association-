<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Pakhelpada Cricket Association</title>

<style>
*{box-sizing:border-box}
body{
 margin:0;
 font-family:Arial,sans-serif;
 background:#f2f5f3;
 color:#222;
}
header{
 background:#064d32;
 color:white;
 text-align:center;
 padding:25px 10px;
}
header h1{margin:0;font-size:28px}
nav{
 background:#033b27;
 padding:15px;
 text-align:center;
}
nav a{
 color:white;
 text-decoration:none;
 margin:8px;
 font-weight:bold;
}
.hero{
 background:linear-gradient(120deg,#075b39,#15945b);
 color:white;
 text-align:center;
 padding:65px 15px;
}
.hero h2{font-size:32px}
section{
 background:white;
 margin:20px auto;
 padding:25px;
 max-width:950px;
 border-radius:12px;
}
h2{color:#075b39}
.card{
 background:#eaf5ee;
 padding:15px;
 margin:10px 0;
 border-radius:8px;
}
button{
 background:#087844;
 color:white;
 border:0;
 padding:10px 15px;
 border-radius:6px;
 margin:4px;
 cursor:pointer;
}
.score{
 background:#063d2a;
 color:white;
 text-align:center;
 padding:25px;
 border-radius:10px;
}
.score h2{color:white}
footer{
 background:#033b27;
 color:white;
 text-align:center;
 padding:20px;
}
input{
 padding:10px;
 margin:5px;
 max-width:100%;
}
</style>
</head>

<body>

<header>
<h1>🏏 PAKHELPADA CRICKET ASSOCIATION</h1>
<p>Village Cricket • Unity • Sportsmanship</p>
</header>

<nav>
<a href="#home">Home</a>
<a href="#about">About</a>
<a href="#matches">Matches</a>
<a href="#score">Live Score</a>
<a href="#teams">Teams</a>
<a href="#gallery">Gallery</a>
<a href="#contact">Contact</a>
</nav>

<div class="hero" id="home">
<h2>Welcome to Pakhelpada Cricket Association</h2>
<p>Promoting Cricket and Village Sports</p>
<button onclick="location.href='#matches'">
View Matches
</button>
</div>

<section id="about">
<h2>About Association</h2>
<p>
Pakhelpada Cricket Association is a village-level
cricket association dedicated to promoting cricket,
sportsmanship and unity among local players.
</p>
</section>

<section id="matches">
<h2>🏆 Match Schedule</h2>
<div class="card">
<h3>Upcoming Cricket Tournament</h3>
<p>Match Date: To Be Announced</p>
<p>Venue: Pakhelpada Cricket Ground</p>
</div>
</section>

<section id="score">
<h2>🔴 Cricket Scoreboard</h2>
<div class="score">
<h2>PAKHELPADA XI</h2>
<h1><span id="runs">0</span>/<span id="wickets">0</span></h1>
<p>Overs: <span id="overs">0.0</span></p>

<button onclick="addRun(1)">1 Run</button>
<button onclick="addRun(2)">2 Runs</button>
<button onclick="addRun(4)">Four</button>
<button onclick="addRun(6)">Six</button>
<button onclick="addBall()">Dot Ball</button>
<button onclick="addWicket()">Wicket</button>
<button onclick="resetScore()">Reset</button>
</div>
<p>Note: This is a local demo scoreboard.
It is not yet connected to a shared online live-score system.</p>
</section>

<section id="teams">
<h2>👥 Cricket Teams</h2>
<div class="card">
<h3>Pakhelpada XI</h3>
<p>Team Players: To Be Updated</p>
</div>
<div class="card">
<h3>Guest Team</h3>
<p>Team Players: To Be Updated</p>
</div>
</section>

<section>
<h2>🥇 Match Results</h2>
<div class="card">
<p>Previous Match Results will be published here.</p>
</div>
</section>

<section id="gallery">
<h2>📸 Photo Gallery</h2>
<p>Cricket tournament photos will be added here.</p>
</section>

<section>
<h2>📢 Latest Notices</h2>
<p>All cricket tournament announcements will appear here.</p>
</section>

<section id="contact">
<h2>📞 Contact Association</h2>
<p>Pakhelpada Cricket Association</p>
<p>Location: Pakhelpada, Odisha</p>
<p>Contact: To Be Updated</p>
</section>

<footer>
<p>© 2026 Pakhelpada Cricket Association</p>
<p>All Rights Reserved</p>
</footer>

<script>
let runs=0;
let wickets=0;
let balls=0;

function update(){
 document.getElementById("runs").innerText=runs;
 document.getElementById("wickets").innerText=wickets;
 document.getElementById("overs").innerText=
 Math.floor(balls/6)+"."+(balls%6);
}

function addRun(n){
 runs+=n;
 balls++;
 update();
}

function addBall(){
 balls++;
 update();
}

function addWicket(){
 if(wickets<10){
 wickets++;
 balls++;
 update();
 }
}

function resetScore(){
 runs=0;
 wickets=0;
 balls=0;
 update();
}
</script>

</body>
</html>
