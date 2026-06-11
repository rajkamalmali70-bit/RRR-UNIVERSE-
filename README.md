<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>RRR Universe - Pro Trading Platform</title>

<style>

/* RESET */
*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:Arial;
scroll-behavior:smooth;
}

body{
background: radial-gradient(circle at top, #0d1b2a, #000);
color:white;
overflow-x:hidden;
}

/* GOLD GLOW BACKGROUND */
body::before,
body::after{
content:"";
position:fixed;
width:300px;
height:300px;
background:gold;
filter:blur(150px);
opacity:0.12;
z-index:-1;
animation:move 7s infinite alternate;
}

body::before{top:10%;left:10%;}
body::after{bottom:10%;right:10%;}

@keyframes move{
from{transform:translate(0,0);}
to{transform:translate(100px,-100px);}
}

/* NAV */
nav{
display:flex;
justify-content:space-between;
align-items:center;
padding:15px 25px;
background:rgba(0,0,0,0.6);
backdrop-filter:blur(10px);
position:fixed;
width:100%;
top:0;
z-index:1000;
border-bottom:1px solid #222;
}

nav h2{
color:gold;
}

nav button{
background:gold;
border:none;
padding:8px 15px;
cursor:pointer;
font-weight:bold;
border-radius:6px;
}

/* HERO */
.hero{
height:100vh;
display:flex;
flex-direction:column;
justify-content:center;
align-items:center;
text-align:center;
padding:20px;
}

.hero h1{
font-size:55px;
color:gold;
text-shadow:0 0 20px gold;
}

.hero p{
color:#aaa;
margin-top:10px;
}

.btn{
margin-top:20px;
padding:12px 25px;
border:none;
background:linear-gradient(90deg,gold,#ffcc00);
color:black;
font-weight:bold;
border-radius:8px;
cursor:pointer;
transition:0.3s;
}

.btn:hover{
transform:scale(1.1);
box-shadow:0 0 20px gold;
}

/* TICKER */
.ticker{
background:#000;
border-top:1px solid gold;
border-bottom:1px solid gold;
padding:10px;
white-space:nowrap;
overflow:hidden;
}

.ticker span{
display:inline-block;
padding-left:100%;
animation:scroll 15s linear infinite;
color:gold;
}

@keyframes scroll{
0%{transform:translateX(0);}
100%{transform:translateX(-100%);}
}

/* SECTIONS */
section{
padding:80px 20px;
text-align:center;
}

.card{
background:rgba(255,255,255,0.05);
border:1px solid rgba(255,215,0,0.2);
border-left:4px solid gold;
padding:20px;
margin:15px auto;
width:80%;
border-radius:12px;
backdrop-filter:blur(10px);
}

/* CHAT BOX */
.chat{
width:80%;
margin:auto;
background:rgba(255,255,255,0.05);
padding:20px;
border-radius:10px;
border:1px solid #333;
}

input{
width:70%;
padding:10px;
border:none;
border-radius:6px;
margin-top:10px;
}

.send{
padding:10px 15px;
background:gold;
border:none;
cursor:pointer;
margin-left:5px;
}

/* LOGIN POPUP */
.popup{
display:none;
position:fixed;
top:50%;
left:50%;
transform:translate(-50%,-50%);
background:#111;
padding:30px;
border:1px solid gold;
border-radius:10px;
z-index:2000;
}

.popup input{
width:100%;
margin:8px 0;
}

footer{
text-align:center;
padding:20px;
color:#777;
border-top:1px solid #222;
}

</style>
</head>

<body>

<!-- NAV -->
<nav>
<h2>RRR Universe</h2>
<button onclick="openLogin()">Login</button>
</nav>

<!-- TICKER -->
<div class="ticker">
<span>BTC $43,200 ▲ | ETH $2,300 ▲ | NASDAQ 18,200 ▲ | GOLD 2,100 ▲ | MARKET LIVE RUNNING... </span>
</div>

<!-- HERO -->
<div class="hero">
<h1>RRR Universe</h1>
<p>Elite Trading & Investment Platform</p>
<button class="btn" onclick="join()">Join Community</button>
</div>

<!-- ABOUT -->
<section>
<h2 style="color:gold;">About</h2>
<div class="card">
Professional trading community for Forex, Crypto & Stocks with daily insights and learning system.
</div>
</section>

<!-- CHAT -->
<section>
<h2 style="color:gold;">Community Chat</h2>

<div class="chat">
<div id="messages">💬 Welcome to RRR Universe chat</div>

<input id="msg" placeholder="Type message...">
<button class="send" onclick="send()">Send</button>
</div>

</section>

<!-- JOIN -->
<section>
<h2 style="color:gold;">Join Now</h2>
<div class="card">
Instagram: @rrr_universe_
<br><br>
<button class="btn" onclick="join()">Join Instagram</button>
</div>
</section>

<!-- FOOTER -->
<footer>
© 2026 RRR Universe | All Rights Reserved
</footer>

<!-- LOGIN POPUP -->
<div class="popup" id="loginBox">
<h3 style="color:gold;">Login</h3>
<input placeholder="Username">
<input placeholder="Password" type="password">
<button class="btn">Login</button>
<br><br>
<button onclick="closeLogin()">Close</button>
</div>

<script>

function join(){
window.open("https://instagram.com/rrr_universe_","_blank");
}

function send(){
let msg = document.getElementById("msg").value;
if(msg !== ""){
document.getElementById("messages").innerHTML += "<br>🟡 " + msg;
document.getElementById("msg").value = "";
}
}

function openLogin(){
document.getElementById("loginBox").style.display="block";
}

function closeLogin(){
document.getElementById("loginBox").style.display="none";
}

</script>

</body>
</html>
