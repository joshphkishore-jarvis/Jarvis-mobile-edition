Jarvis mobile edition 
MY JARVIS AI ASSISTANT 
Index.html
<!DOCTYPE html>

<html>

<head>

<meta charset="UTF-8">

<meta name="viewport" content="width=device-width, initial-scale=1">

<title>J.A.R.V.I.S</title>

<link rel="stylesheet" href="style.css">

</head>

<body>

<header><h1>J.A.R.V.I.S</h1><p>MOBILE EDITION</p></header>

<div class="core">

<div class="ring r1"></div>

<div class="ring r2"></div>

<div class="center"></div>

</div>

<p class="core-text">CORE ACTIVE</p>

<div class="status">

<h2>SYSTEM STATUS</h2>

<div class="row"><span>AI CORE</span><b class="on"> ONLINE</b></div>

<div class="row"><span>NETWORK</span><b class="on"> ONLINE</b></div>

<div class="row"><span>VOICE</span><b class="off"> LOCKED</b></div>

LOCKED</b></div> <div class="row"><span>MEMORY</span><b class="off">

</div>

<div class="chat" id="chat"></div>

<div class="input-area">

<input id="msg" placeholder="Ask J.A.R.V.I.S...">

<button id="send">SEND</button>

</div>

<script src="script.js"></script>

</body>

</html>




const chat = document.getElementById('chat');
const input = document.getElementById('msg');

document.getElementById('send').onclick = () => {
  const t = input.value.trim();
  if (!t) return;

  add('YOU: ' + t, 'user');
  input.value = '';

  add('J.A.R.V.I.S: Processing...', 'ai');

  setTimeout(() => {
    chat.lastChild.innerText = 'J.A.R.V.I.S: Systems online. How may I assist you?';
  }, 1000);
};

function add(text, who) {
  const d = document.createElement('div');
  d.className = 'msg ' + who;
  d.innerText = text;
  chat.appendChild(d);
  chat.scrollTop = chat.scrollHeight;
}
