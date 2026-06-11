<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>HitungCepat</title>

<!-- FONT -->
<link href="https://fonts.googleapis.com/css2?family=Chakra+Petch:wght@400;500;600;700&family=Oxanium:wght@500;700;800&display=swap" rel="stylesheet">

<style>

*{
  margin:0;
  padding:0;
  box-sizing:border-box;
}

body{
  font-family:'Chakra Petch',sans-serif;
  min-height:100vh;
  overflow-x:hidden;

  background:
  radial-gradient(circle at top left,#7928ff 0%,transparent 30%),
  radial-gradient(circle at bottom right,#00e5ff 0%,transparent 30%),
  linear-gradient(135deg,#090814,#16102f,#0a0a16);

  display:flex;
  justify-content:center;
  align-items:flex-start;

  padding:12px;

  color:white;
}

/* FALLING FORMULAS */

#fallingMath{
  position:fixed;
  inset:0;
  overflow:hidden;
  z-index:0;
  pointer-events:none;
}

.math-fall{
  position:absolute;
  top:-120px;

  color:rgba(255,255,255,0.12);

  font-family:'Oxanium',sans-serif;
  font-weight:700;

  white-space:nowrap;

  animation-name:fallDown;
  animation-timing-function:linear;
  animation-iteration-count:infinite;
}

@keyframes fallDown{

  0%{
    transform:
    translateY(-120px)
    rotate(0deg);

    opacity:0;
  }

  10%{
    opacity:1;
  }

  100%{
    transform:
    translateY(120vh)
    rotate(8deg);

    opacity:0;
  }
}

/* APP */

.app{
  position:relative;
  z-index:2;

  width:100%;
  max-width:430px;

  display:flex;
  flex-direction:column;

  padding-bottom:30px;
}

/* GLASS */

.glass{
  background:rgba(255,255,255,0.08);

  border:1px solid rgba(255,255,255,0.12);

  backdrop-filter:blur(18px);

  border-radius:28px;

  box-shadow:
  0 10px 35px rgba(0,0,0,0.35);
}

/* START SCREEN */

.start-screen{
  margin-top:70px;
  text-align:center;
}

.logo{
  font-family:'Oxanium',sans-serif;

  font-size:58px;
  font-weight:800;

  background:
  linear-gradient(90deg,#00e5ff,#ff00d4);

  -webkit-background-clip:text;
  -webkit-text-fill-color:transparent;

  letter-spacing:2px;
}

.tagline{
  margin-top:14px;
  color:#d8d8d8;
  font-size:16px;
}

.start-card{
  margin-top:38px;
  padding:28px;
}

.start-btn{
  width:100%;
  height:74px;

  border:none;
  border-radius:24px;

  cursor:pointer;

  font-family:'Chakra Petch',sans-serif;

  font-size:24px;
  font-weight:800;

  background:
  linear-gradient(90deg,#00e5ff,#8aff00);

  color:#111;

  box-shadow:
  0 0 25px rgba(0,229,255,0.35);

  transition:0.2s;
}

.start-btn:active{
  transform:scale(0.97);
}

/* MENU */

.menu-screen{
  display:none;
  margin-top:30px;
}

.menu-card{
  padding:24px;
}

.section-title{
  margin-bottom:14px;
  margin-top:12px;

  font-size:18px;
  font-weight:700;
}

.option-group{
  display:flex;
  flex-direction:column;
  gap:12px;
}

.option-btn{
  height:62px;

  border:none;
  border-radius:18px;

  cursor:pointer;

  font-family:'Chakra Petch',sans-serif;

  color:white;

  font-size:16px;
  font-weight:700;

  background:
  linear-gradient(
  145deg,
  rgba(255,255,255,0.1),
  rgba(255,255,255,0.05));

  border:1px solid rgba(255,255,255,0.08);

  transition:0.2s;
}

.option-btn.active{
  background:
  linear-gradient(90deg,#00e5ff,#7f5af0,#ff00d4);

  box-shadow:
  0 0 18px rgba(0,229,255,0.4);
}

.name-input{
  width:100%;
  height:60px;

  margin-bottom:20px;

  border:none;
  border-radius:18px;

  padding:0 18px;

  background:
  rgba(255,255,255,0.08);

  color:white;

  font-family:'Chakra Petch',sans-serif;
  font-size:18px;

  outline:none;
}

.name-input::placeholder{
  color:#cfcfcf;
}

.play-btn{
  width:100%;
  margin-top:28px;

  height:70px;

  border:none;
  border-radius:22px;

  cursor:pointer;

  font-family:'Chakra Petch',sans-serif;

  font-size:22px;
  font-weight:800;

  background:
  linear-gradient(90deg,#00e5ff,#8aff00);

  color:#111;
}

/* GAME */

.game-screen{
  display:none;
  flex-direction:column;
  margin-top:10px;
}

/* TOP */

.top-bar{
  display:flex;
  gap:14px;
}

.score-card{
  flex:1;
  padding:16px;
  text-align:center;
}

.score-label{
  font-size:13px;
  color:#ddd;
}

.score-value{
  margin-top:4px;

  font-family:'Oxanium',sans-serif;

  font-size:32px;
  font-weight:800;
}

/* BOARD */

.board{
  margin-top:22px;
  padding:28px 20px;
  text-align:center;
}

.level-badge{
  display:inline-block;

  padding:8px 18px;

  border-radius:999px;

  background:
  linear-gradient(90deg,#ff00d4,#7f5af0);

  font-family:'Oxanium',sans-serif;

  font-size:14px;
  font-weight:700;
}

.timer{
  margin-top:18px;

  font-family:'Oxanium',sans-serif;

  font-size:20px;
  font-weight:700;

  color:#00e5ff;
}

.question{
  margin-top:30px;

  font-family:'Oxanium',sans-serif;

  font-size:58px;
  font-weight:800;

  letter-spacing:3px;

  min-height:80px;
}

.message{
  margin-top:18px;

  min-height:30px;

  font-size:20px;
  font-weight:700;
}

.game-over{
  margin-top:18px;

  font-size:26px;
  font-weight:800;

  color:#ffe600;
}

/* ANSWERS */

.answers{
  margin-top:26px;

  display:flex;
  gap:14px;
}

.answer-btn{
  flex:1;

  height:92px;

  border:none;
  border-radius:24px;

  cursor:pointer;

  background:
  linear-gradient(
  145deg,
  rgba(255,255,255,0.16),
  rgba(255,255,255,0.05));

  border:1px solid rgba(255,255,255,0.08);

  color:white;

  font-family:'Chakra Petch',sans-serif;

  font-size:32px;
  font-weight:800;

  transition:0.15s;
}

.answer-btn:active{
  transform:scale(0.95);
}

/* BUTTONS */

.bottom-buttons{
  margin-top:22px;

  display:flex;
  gap:12px;
}

.bottom-btn{
  flex:1;

  height:60px;

  border:none;
  border-radius:18px;

  cursor:pointer;

  font-family:'Chakra Petch',sans-serif;

  font-size:16px;
  font-weight:700;
}

.restart-btn{
  background:
  linear-gradient(90deg,#00e5ff,#00ffa3);

  color:#111;
}

.menu-btn{
  background:
  rgba(255,255,255,0.12);

  color:white;
}

/* LEADERBOARD */

.leaderboard{
  margin-top:22px;
  padding:22px;
}

.leaderboard h2{
  text-align:center;
  margin-bottom:16px;

  font-family:'Oxanium',sans-serif;
}

.leaderboard-item{
  display:flex;
  justify-content:space-between;

  padding:12px 14px;

  margin-bottom:10px;

  border-radius:14px;

  background:
  rgba(255,255,255,0.08);

  font-weight:700;
}

/* MOBILE */

@media(max-width:480px){

  .question{
    font-size:48px;
  }

  .answer-btn{
    height:78px;
    font-size:26px;
  }

}


/* NEW FEATURES */

.combo-bar{
  margin-top:14px;
  font-size:16px;
  color:#ffe600;
  font-weight:700;
  text-align:center;
}

.progress-wrap{
  margin-top:18px;
  width:100%;
  height:12px;
  background:rgba(255,255,255,0.08);
  border-radius:999px;
  overflow:hidden;
}

.progress-bar{
  width:100%;
  height:100%;
  background:linear-gradient(90deg,#00e5ff,#00ff88);
  transition:0.8s linear;
}

.streak{
  margin-top:14px;
  color:#00ffbf;
  font-weight:700;
}

.powerup{
  margin-top:14px;
  color:#ffb700;
  font-weight:700;
}

.fade-in{
  animation:fadeIn 0.3s ease;
}

@keyframes fadeIn{
  from{
    opacity:0;
    transform:translateY(10px);
  }
  to{
    opacity:1;
    transform:translateY(0);
  }
}


/* SUPER FEATURES */

.answer-btn:hover{
  transform:translateY(-5px) scale(1.04);
  box-shadow:0 0 24px rgba(0,229,255,0.5);
}

.play-btn:hover,
.start-btn:hover{
  transform:scale(1.03);
  box-shadow:0 0 28px rgba(0,255,170,0.5);
}

.glow-correct{
  animation:correctFlash 0.5s ease;
}

@keyframes correctFlash{
  0%{
    box-shadow:0 0 0 rgba(0,255,120,0);
  }
  50%{
    box-shadow:0 0 40px rgba(0,255,120,0.8);
  }
  100%{
    box-shadow:0 0 0 rgba(0,255,120,0);
  }
}

.shake{
  animation:shake 0.4s;
}

@keyframes shake{
  0%{transform:translateX(0);}
  25%{transform:translateX(-8px);}
  50%{transform:translateX(8px);}
  75%{transform:translateX(-8px);}
  100%{transform:translateX(0);}
}

.theme-btn{
  margin-top:12px;
  width:100%;
  height:54px;
  border:none;
  border-radius:16px;
  cursor:pointer;
  font-weight:700;
  background:linear-gradient(90deg,#ff00d4,#00e5ff);
  color:white;
}


/* NEW EPIC FEATURES */

.correct-answer{
  background:linear-gradient(90deg,#00ff88,#00e676)!important;
  color:#111!important;
  box-shadow:0 0 25px rgba(0,255,120,0.7)!important;
}

.wrong-answer{
  background:linear-gradient(90deg,#ff1744,#ff5252)!important;
  color:white!important;
  box-shadow:0 0 25px rgba(255,0,80,0.7)!important;
}

.level-up{
  animation:levelUp 0.8s ease;
}

@keyframes levelUp{
  0%{
    transform:scale(1);
  }
  50%{
    transform:scale(1.08);
  }
  100%{
    transform:scale(1);
  }
}

.xp-bar-wrap{
  margin-top:16px;
  height:12px;
  border-radius:999px;
  overflow:hidden;
  background:rgba(255,255,255,0.08);
}

.xp-bar{
  width:0%;
  height:100%;
  background:linear-gradient(90deg,#ffe600,#ff9100);
  transition:0.3s;
}

.player-level{
  margin-top:10px;
  color:#ffe600;
  font-weight:700;
  font-size:15px;
}

.speed-text{
  margin-top:10px;
  color:#00e5ff;
  font-size:14px;
  font-weight:700;
}


.mute-icon{
  position:fixed;
  top:16px;
  right:16px;
  width:48px;
  height:48px;
  border:none;
  border-radius:50%;
  cursor:pointer;
  z-index:9999;
  font-size:22px;
  background:rgba(255,255,255,0.12);
  backdrop-filter:blur(12px);
  color:white;
  box-shadow:0 4px 16px rgba(0,0,0,0.25);
}


.mute-fab{
 position:fixed;
 top:18px !important;
 right:18px !important;
 top:18px;
 right:18px;
 width:56px;
 height:56px;
 border:none;
 border-radius:50%;
 cursor:pointer;
 z-index:9999;
 backdrop-filter:blur(14px);
 background:rgba(255,255,255,.12);
 box-shadow:0 8px 24px rgba(0,0,0,.25);
 transition:transform .25s ease, background .25s ease;
 overflow:hidden;
}
.mute-fab:hover{transform:scale(1.08)}
.mute-fab.muted{transform:scale(.92) rotate(-10deg);}
.mute-fab svg{width:28px;height:28px;fill:white}
.ripple{
 position:absolute;border-radius:50%;
 transform:scale(0);
 animation:ripple .6s linear;
 background:rgba(255,255,255,.35);
}
@keyframes ripple{
 to{transform:scale(4);opacity:0}
}

</style>
</head>
<body>

<button id="muteBtn" class="mute-fab" onclick="toggleMusic(event)">
<svg id="soundIcon" viewBox="0 0 24 24">
<path d="M14 3.23v17.54L7.91 16H4a1 1 0 0 1-1-1V9a1 1 0 0 1 1-1h3.91L14 3.23zM17.5 12a5.5 5.5 0 0 0-2.03-4.25v8.5A5.5 5.5 0 0 0 17.5 12zm2.5 0a8 8 0 0 1-3.03 6.28v-2.02a6 6 0 0 0 0-8.52V5.72A8 8 0 0 1 20 12z"/>
</svg>
</button>



<!-- FALLING MATH -->
<div id="fallingMath"></div>

<div class="app">

  <!-- START -->
  <div class="start-screen" id="startScreen">

    <div class="logo">
      ⚡ HitungCepat
    </div>

    <div class="tagline">
      Latih fokus dan refleks matematikamu!
    </div>

    <div class="start-card glass">

      


<button class="start-btn"
      onclick="openMenu()">
      ▶ START
      </button>

    <div style="margin-top:24px;text-align:center;">

      <div style="
      font-size:12px;
      color:#d0d0d0;
      margin-bottom:10px;
      letter-spacing:1px;
      ">
      report bug
      </div>

      <a href="https://www.instagram.com/hitungcepat.id?igsh=azMyYjN0bWdneDN1"
      target="_blank"
      style="
      display:inline-flex;
      align-items:center;
      justify-content:center;
      width:64px;
      height:64px;
      border-radius:50%;
      text-decoration:none;
      background:linear-gradient(135deg,#feda75,#fa7e1e,#d62976,#962fbf,#4f5bd5);
      box-shadow:0 0 22px rgba(255,0,140,0.35);
      font-size:34px;
      ">
      <img src="2227.jpg" style="width:38px;height:38px;border-radius:10px;">
      </a>

    </div>


    <div class="glass" style="margin-top:20px;padding:18px;text-align:center;">
  <div style="font-size:18px;font-weight:800;color:#00e5ff;">
    🎮 FITUR BARU
  </div>

  <div style="margin-top:14px;font-size:14px;line-height:1.8;color:#ddd;">
    ⚡ Combo Mode<br>
    🔥 Streak Counter<br>
    🎁 Bonus Score<br>
    ⌨ Keyboard Control<br>
    🎨 Animasi Baru<br>
    🌈 Efek Glow<br>
    💥 Efek Jawaban Benar<br>
    📈 Progress Bar<br>
    🧠 Random Challenge<br>
    🎵 Sound Arcade
  </div>

</div>

  </div>

</div>


  <!-- MENU -->
  <div class="menu-screen" id="menuScreen">

    <div class="menu-card glass">

      

      
      <div class="section-title">
        ⏳ Mode Permainan
      </div>

      <div class="option-group">
        <button class="option-btn active" onclick="selectTimerMode(true,this)">
        ⏱ MENGGUNAKAN WAKTU
        </button>

        <button class="option-btn" onclick="selectTimerMode(false,this)">
        ♾ TANPA WAKTU
        </button>
      </div>


      <div class="section-title">
        🎯 Pilih Level
      </div>

      <div class="option-group">

        <button class="option-btn active"
        onclick="selectLevel('veryeasy',this)">
        VERY EASY • Pertambahan
        </button>

        <button class="option-btn"
        onclick="selectLevel('easy',this)">
        EASY • Tambah & Kurang
        </button>

        <button class="option-btn"
        onclick="selectLevel('normal',this)">
        NORMAL • Kali & Bagi
        </button>

        <button class="option-btn"
        onclick="selectLevel('hard',this)">
        HARD • Faktorial & Persen
        </button>


      </div>

      <div id="timeSection">
      <div class="section-title">
        ⏰ Pilih Waktu
      </div>

      <div class="option-group">

        <button class="option-btn active"
        onclick="selectTime(60,this)">
        1 MENIT
        </button>

        <button class="option-btn"
        onclick="selectTime(180,this)">
        3 MENIT
        </button>

        <button class="option-btn"
        onclick="selectTime(300,this)">
        5 MENIT
        </button>

        <button class="option-btn"
        onclick="selectTime(600,this)">
        10 MENIT
        </button>

      </div>
      </div>

      <button class="play-btn"
      onclick="startGame()">
      ▶ MULAI GAME
      </button>

<button class="theme-btn" onclick="changeTheme()">
🌈 GANTI TEMA
</button>



    </div>

  </div>

  <!-- GAME -->
  <div class="game-screen" id="gameScreen">

    <div class="top-bar">

      <div class="score-card glass">
        <div class="score-label">SKOR</div>
        <div class="score-value" id="score">0</div>
      </div>

      <div class="score-card glass">
        <div class="score-label">BEST</div>
        <div class="score-value" id="bestScore">0</div>
      </div>

    </div>

    <div class="board glass">

      <div class="level-badge"
      id="levelBadge">
      EASY
      </div>

      <div class="timer">
        ⏳ <span id="time">60</span>s
      </div>

      <div class="question"
      id="question">
      5 + 5
      </div>

      <div class="message" id="message"></div><div id="dynamicDifficulty" style="margin-top:8px;color:#ffe600;font-weight:700;">Difficulty Lv. 1</div>
      

      

      <div class="powerup" id="powerupText">
        
      </div>


      <div class="game-over"
      id="gameOver"></div>


    </div>

    <div class="answers">

      <button class="answer-btn"
      id="btn0"
      onclick="selectAnswer(0)">
      0
      </button>

      <button class="answer-btn"
      id="btn1"
      onclick="selectAnswer(1)">
      0
      </button>

      <button class="answer-btn"
      id="btn2"
      onclick="selectAnswer(2)">
      0
      </button>

    </div>

    <div class="bottom-buttons">

      <button class="bottom-btn restart-btn"
      id="restartBtn"
      onclick="restartGame()">
      🔄 Ulang
      </button>

      <button class="bottom-btn menu-btn"
      onclick="backMenu()">
      🏠 Menu
      </button>

    </div>

</div>

</div>


    </div>

</div>

<!-- FIREBASE -->
<script type="module">

import { initializeApp }
from "https://www.gstatic.com/firebasejs/10.12.2/firebase-app.js";

import {
  getFirestore,
  collection,
  addDoc,
  query,
  orderBy,
  limit,
  getDocs
}
from "https://www.gstatic.com/firebasejs/10.12.2/firebase-firestore.js";

/* GANTI DENGAN CONFIG FIREBASE KAMU */

const firebaseConfig = {

  apiKey: "ISI_API_KEY",
  authDomain: "ISI_AUTH_DOMAIN",
  projectId: "ISI_PROJECT_ID",
  storageBucket: "ISI_BUCKET",
  messagingSenderId: "ISI_SENDER_ID",
  appId: "ISI_APP_ID"

};

const app =
initializeApp(firebaseConfig);

const db =
getFirestore(app);

/* GAME VARIABLES */

let score = 0;
let correctCount = 0;
let wrongCount = 0;
let questionStartTime = 0;
let totalAnswerTime = 0;
let difficultyBoost = 0;


let bestScore = 0;

let selectedLevel = "veryeasy";
let selectedTime = 60;
let useTimer = true;

let correctAnswer = 0;

let timer = null;
let timeLeft = 60;
let gameActive = false;


function getBestKey(){
  return "hitungcepat_best_" + selectedLevel;
}

bestScore = parseInt(localStorage.getItem(getBestKey())) || 0;


document.getElementById("bestScore")
.innerText = bestScore;


/* FALLING FORMULAS */

const formulas = [

  "5 + 7 = 12",
  "12 × 8 = 96",
  "√144 = 12",
  "9² = 81",
  "π = 3.14",
  "7 × 6 = 42",
  "2πr",
  "Σ x",
  "a² + b²"

];

function createFallingFormula(){

  const formula =
  document.createElement("div");

  formula.classList.add("math-fall");

  formula.innerText =
  formulas[
    Math.floor(
      Math.random() * formulas.length
    )
  ];

  formula.style.left =
  Math.random() * 100 + "vw";

  formula.style.fontSize =
  (18 + Math.random() * 18) + "px";

  formula.style.animationDuration =
  (5 + Math.random() * 7) + "s";

  document.getElementById("fallingMath")
  .appendChild(formula);

  setTimeout(() => {
    formula.remove();
  },12000);
}

setInterval(() => {
  createFallingFormula();
},500);

/* MENU */

window.openMenu = function(){

  document.getElementById("startScreen")
  .style.display = "none";

  document.getElementById("menuScreen")
  .style.display = "block";

  document.querySelector(".timer").style.display = "block";
}

/* LEVEL */

window.selectLevel = function(level,btn){

  selectedLevel = level;

  const buttons =
  btn.parentElement.querySelectorAll(".option-btn");

  buttons.forEach(button =>
  button.classList.remove("active"));

  btn.classList.add("active");

  bestScore = parseInt(localStorage.getItem(getBestKey())) || 0;
  const bestEl=document.getElementById("bestScore");
  if(bestEl) bestEl.innerText = bestScore;
}

window.selectTimerMode = function(mode,btn){

  useTimer = mode;

  const buttons = btn.parentElement.querySelectorAll(".option-btn");
  buttons.forEach(b=>b.classList.remove("active"));

  btn.classList.add("active");

  const timeSection = document.getElementById("timeSection");
  if(timeSection){
    timeSection.style.display = useTimer ? "block" : "none";
  }
}

/* TIME */

window.selectTime = function(time,btn){

  selectedTime = time;

  const buttons =
  document.querySelector("#timeSection .option-group")
  .querySelectorAll(".option-btn");

  buttons.forEach(button =>
  button.classList.remove("active"));

  btn.classList.add("active");
}

/* RANDOM */

function random(min,max){

  return Math.floor(
    Math.random()*(max-min+1)
  ) + min;
}

/* START */

window.startGame = function(){

  initAudio();

  clearInterval(timer);

  score = 0;
  correctCount = 0;
  wrongCount = 0;
  totalAnswerTime = 0;
  difficultyBoost = 0;
  timeLeft = selectedTime;
  gameActive = true;

  document.getElementById("score")
  .innerText = score;

  document.getElementById("time")
  .innerText = timeLeft;

  document.getElementById("message")
  .innerText = "";

  document.getElementById("gameOver")
  .innerText = "";

  document.getElementById("restartBtn").disabled = true;
  document.getElementById("restartBtn").style.opacity = "0.5";

  document.getElementById("menuScreen")
  .style.display = "none";

  document.getElementById("gameScreen")
  .style.display = "flex";

  document.getElementById("levelBadge")
  .innerText =
  selectedLevel.toUpperCase();

  
    document.getElementById("question").classList.add("fade-in");
    generateQuestion();

  if(useTimer){
    document.querySelector(".timer").style.display = "block";
    startTimer();
  }else{
    document.querySelector(".timer").style.display = "none";
  }

}

/* QUESTION */

function generateQuestion(){

  if(!gameActive) return;

  let num1;
  let num2;
  let operator;

  if(selectedLevel === "veryeasy"){

    operator = "+";
    num1 = random(1,15 + difficultyBoost*5);
    num2 = random(1,15 + difficultyBoost*5);
    correctAnswer = num1 + num2;
  }

  else if(selectedLevel === "easy"){

    const ops = ["+","-"];
    operator = ops[random(0,1)];

    num1 = random(1,30 + difficultyBoost*8);
    num2 = random(1,30 + difficultyBoost*8);

    if(operator === "+"){
      correctAnswer = num1 + num2;
    }else{
      if(num2 > num1){
        [num1,num2] = [num2,num1];
      }
      correctAnswer = num1 - num2;
    }
  }

  else if(selectedLevel === "normal"){

    const ops = ["×","÷"];
    operator = ops[random(0,1)];

    if(operator === "×"){
      num1 = random(1,12 + difficultyBoost);
      num2 = random(1,12 + difficultyBoost);
      correctAnswer = num1 * num2;
    }else{
      num2 = random(1,12);
      correctAnswer = random(1,12);
      num1 = num2 * correctAnswer;
    }
  }

  else if(selectedLevel === "hard"){

    const mode = random(1,2);

    if(mode === 1){
      const n = random(3,6);
      correctAnswer = 1;
      for(let i=2;i<=n;i++) correctAnswer *= i;

      document.getElementById("question").innerText = `${n}!`;
      generateChoices();
  questionStartTime = Date.now();
      return;
    }else{
      const base = random(20,500);
      const percent = [10,20,25,50][random(0,3)];

      correctAnswer = (base * percent) / 100;

      document.getElementById("question").innerText =
      `${percent}% dari ${base}`;
      generateChoices();
      return;
    }
  }

  document.getElementById("question")
  .innerText =
  `${num1} ${operator} ${num2}`;

  generateChoices();
  questionStartTime = Date.now();
}

/* CHOICES */


function generateChoices(){

  for(let i=0;i<3;i++){
    document.getElementById("btn"+i)
    .classList.remove("correct-answer","wrong-answer");
  }

  let answers = [correctAnswer];

  let maxOffset;

  switch(selectedLevel){
    case "veryeasy":
      maxOffset = 2;
      break;
    case "easy":
      maxOffset = 4;
      break;
    case "normal":
      maxOffset = 8;
      break;
    case "hard":
      maxOffset = Math.max(10, Math.floor(correctAnswer * 0.15));
      break;
    default:
      maxOffset = 3;
  }

  while(answers.length < 3){

    let offset;

    do{
      offset =
      Math.floor(Math.random() * (maxOffset * 2 + 1))
      - maxOffset;
    }while(offset === 0);

    let fake = correctAnswer + offset;

    if(fake >= 0 && !answers.includes(fake)){
      answers.push(fake);
    }
  }

  answers.sort(() => Math.random() - 0.5);

  for(let i=0;i<3;i++){
    const btn = document.getElementById("btn"+i);
    btn.innerText = answers[i];
    btn.dataset.value = answers[i];
  }
}


/* ANSWER */

window.selectAnswer = async function(index){

  if(!gameActive) return;

  const selected =
  parseInt(
    document.getElementById("btn"+index)
    .dataset.value
  );

  const answerDuration = (Date.now() - questionStartTime)/1000;
  totalAnswerTime += answerDuration;

  const message =
  document.getElementById("message");

  if(selected === correctAnswer){

    
    playCorrectSound();
    flashEffect();
    
    

    
    score++;
    correctCount++;
    if(score % 5 === 0) difficultyBoost++;
    
    

    // bonus removed

    
    
    
    
    
    

    document.getElementById("score").innerText = score;
    document.getElementById("dynamicDifficulty").innerText = `Difficulty Lv. ${difficultyBoost+1}`;

    message.style.color = "#00ff9d";
    message.innerText = "🔥 BENAR +1 SCORE!";

    if(score > bestScore){

      bestScore = score;

      localStorage.setItem(
        getBestKey(),
        bestScore
      );

      document.getElementById("bestScore")
      .innerText = bestScore;
    }

    
    document.getElementById("question").classList.add("fade-in");
    generateQuestion();
    
  }

  else{

    clearInterval(timer);

    gameActive = false;

    message.style.color = "#ff5e7e";
    
    playWrongSound();

    document.querySelector(".board")
    .classList.add("shake");

    setTimeout(()=>{
      document.querySelector(".board")
      .classList.remove("shake");
    },400);
    

    
    
    

    
    
    
    
    
    
    
    
    

    message.innerText = "❌ JAWABAN SALAH!";

    document.getElementById("restartBtn").disabled = false;
    document.getElementById("restartBtn").style.opacity = "1";

    for(let i=0;i<3;i++){

      const btn =
      document.getElementById("btn"+i);

      const value =
      parseInt(btn.dataset.value);

      if(value === correctAnswer){
        btn.classList.add("correct-answer");
      }

      if(value === selected){
        btn.classList.add("wrong-answer");
      }
    }
    

    document.getElementById("question")
    .innerText = "GAME OVER";

    document.getElementById("gameOver")
    .innerText =
    `🏆 SKOR AKHIR: ${score}`;

      document.getElementById("restartBtn").disabled = false;
      document.getElementById("restartBtn").style.opacity = "1";

    const playerName = "Player";

    await saveScore(playerName,score);

    }
}





/* LEVEL SYSTEM REMOVED */

/* LEVEL UP SOUND */

function playLevelUpSound(){

  initAudio();

  const notes = [523,659,784,1046];

  notes.forEach((freq,i)=>{

    const osc = audioCtx.createOscillator();
    const gain = audioCtx.createGain();

    osc.type = "triangle";
    osc.frequency.value = freq;

    gain.gain.setValueAtTime(
      0.12,
      audioCtx.currentTime + i*0.1
    );

    gain.gain.exponentialRampToValueAtTime(
      0.001,
      audioCtx.currentTime + i*0.1 + 0.2
    );

    osc.connect(gain);
    gain.connect(audioCtx.destination);

    osc.start(audioCtx.currentTime + i*0.1);
    osc.stop(audioCtx.currentTime + i*0.1 + 0.2);
  });
}

/* SUPER GAME FEATURES */

let currentTheme = 0;

const themes = [
  "linear-gradient(135deg,#090814,#16102f,#0a0a16)",
  "linear-gradient(135deg,#00111f,#002d3a,#000814)",
  "linear-gradient(135deg,#2d0036,#12002f,#090014)",
  "linear-gradient(135deg,#052b1f,#041c32,#000000)"
];

window.changeTheme = function(){

  currentTheme++;

  if(currentTheme >= themes.length){
    currentTheme = 0;
  }

  document.body.style.background =
  themes[currentTheme];

}

/* PARTICLE EFFECT */

function flashEffect(){

  const board = document.querySelector(".board");

  board.classList.add("glow-correct");

  setTimeout(()=>{
    board.classList.remove("glow-correct");
  },500);
}


/* EXTRA FEATURES */

/* KEYBOARD SUPPORT */
document.addEventListener("keydown",(e)=>{

  if(!gameActive) return;

  if(e.key === "1") selectAnswer(0);
  if(e.key === "2") selectAnswer(1);
  if(e.key === "3") selectAnswer(2);

});


/* TIMER */

function startTimer(){

  timer = setInterval(() => {

    timeLeft--;

    document.getElementById("time")
    .innerText = timeLeft;

    updateProgressBar();

    if(timeLeft <= 0){

      clearInterval(timer);

      gameActive = false;

      document.getElementById("question")
      .innerText = "GAME OVER";

      document.getElementById("message").innerText = "⏰ WAKTU HABIS!";
      document.getElementById("gameOver").innerText = `🏆 SKOR AKHIR: ${score}`;

      document.getElementById("restartBtn").disabled = false;
      document.getElementById("restartBtn").style.opacity = "1";

      saveScore("Player", score);
    }

  },1000);
}

/* RESTART */

window.restartGame = function(){

  if(gameActive) return;

  startGame();
}

/* BACK MENU */

window.backMenu = function(){

  clearInterval(timer);

  gameActive = false;

  document.getElementById("gameScreen")
  .style.display = "none";

  document.getElementById("menuScreen")
  .style.display = "block";

  document.querySelector(".timer").style.display = "block";
}




/* SOUND SYSTEM */
let audioCtx;

document.addEventListener('click', ()=>{
  initAudio();
},{once:true});

function initAudio(){
  if(!audioCtx){
    audioCtx = new (window.AudioContext || window.webkitAudioContext)();
    startBackgroundMusic();
  }
}

function playCorrectSound(){
  initAudio();
  const osc = audioCtx.createOscillator();
  const gain = audioCtx.createGain();
  osc.type = "triangle";
  osc.frequency.setValueAtTime(700, audioCtx.currentTime);
  osc.frequency.exponentialRampToValueAtTime(1100, audioCtx.currentTime + 0.15);
  gain.gain.setValueAtTime(0.14, audioCtx.currentTime);
  gain.gain.exponentialRampToValueAtTime(0.001, audioCtx.currentTime + 0.2);
  osc.connect(gain);
  gain.connect(audioCtx.destination);
  osc.start();
  osc.stop(audioCtx.currentTime + 0.2);
}


function playWrongSound(){
  initAudio();

  // Arcade-style fail sound
  const notes = [420, 320, 220, 140];

  notes.forEach((freq, i) => {
    const osc = audioCtx.createOscillator();
    const gain = audioCtx.createGain();

    osc.type = "square";
    osc.frequency.value = freq;

    gain.gain.setValueAtTime(0.10, audioCtx.currentTime + i * 0.08);
    gain.gain.exponentialRampToValueAtTime(
      0.001,
      audioCtx.currentTime + i * 0.08 + 0.12
    );

    osc.connect(gain);
    gain.connect(audioCtx.destination);

    osc.start(audioCtx.currentTime + i * 0.08);
    osc.stop(audioCtx.currentTime + i * 0.08 + 0.12);
  });
}



let musicMuted = false;

window.toggleMusic = function(){
  musicMuted = !musicMuted;

  const btn = document.getElementById("muteBtn");
  btn.innerText = musicMuted ? "🔇" : "🔊";
}


window.toggleMusic = function(e){
  musicMuted = !musicMuted;
  const btn = document.getElementById('muteBtn');
  const icon = document.getElementById('soundIcon');

  btn.classList.toggle('muted', musicMuted);

  icon.innerHTML = musicMuted
  ? '<path d="M16.5 12c0-1.2-.34-2.32-.93-3.27l1.45-1.45A7.94 7.94 0 0 1 20 12c0 2.21-.9 4.21-2.35 5.66l-1.42-1.42A5.96 5.96 0 0 0 16.5 12zM3 4.27 4.28 3 21 19.72 19.73 21l-3.5-3.5L14 20.77V15.8l-4-4V16H7.91L4 12.09V9h3.91L14 3.23v3.49L19.73 12 3 4.27z"/>'
  : '<path d="M14 3.23v17.54L7.91 16H4a1 1 0 0 1-1-1V9a1 1 0 0 1 1-1h3.91L14 3.23zM17.5 12a5.5 5.5 0 0 0-2.03-4.25v8.5A5.5 5.5 0 0 0 17.5 12zm2.5 0a8 8 0 0 1-3.03 6.28v-2.02a6 6 0 0 0 0-8.52V5.72A8 8 0 0 1 20 12z"/>';

  const ripple=document.createElement('span');
  ripple.className='ripple';
  const rect=btn.getBoundingClientRect();
  ripple.style.width=ripple.style.height='20px';
  ripple.style.left=(e.offsetX-10)+'px';
  ripple.style.top=(e.offsetY-10)+'px';
  btn.appendChild(ripple);
  setTimeout(()=>ripple.remove(),600);
}

let bgmStarted = false;

function startBackgroundMusic(){

  if(bgmStarted) return;

  bgmStarted = true;

  const melody = [262,330,392,523,392,330,262,523];

  let noteIndex = 0;

  setInterval(()=>{

    if(!audioCtx || musicMuted) return;

    const osc = audioCtx.createOscillator();
    const gain = audioCtx.createGain();

    osc.type = "sawtooth";

    osc.frequency.value =
    melody[noteIndex % melody.length];

    gain.gain.setValueAtTime(
      0.04,
      audioCtx.currentTime
    );

    gain.gain.exponentialRampToValueAtTime(
      0.001,
      audioCtx.currentTime + 0.35
    );

    osc.connect(gain);
    gain.connect(audioCtx.destination);

    osc.start();
    osc.stop(audioCtx.currentTime + 0.35);

    noteIndex++;

  },320);
}

</script>

</body>
</html>
