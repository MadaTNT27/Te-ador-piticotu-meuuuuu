# Te-ador-piticotu-meuuuuu
<html lang="ro">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Pentru piticotu' meu 💖</title>

  <style>
    :root{
      --pink:#ffd4e6;
      --deep:#ff2f74;
      font-family:"Poppins", system-ui, Arial;
    }

    html,body{margin:0;padding:0;height:100%}
    body{
      background:linear-gradient(180deg,var(--pink),#ffe6f2,#fff);
      overflow:hidden;
    }

    .card{
      position:relative;
      z-index:2;
      max-width:900px;
      margin:40px auto;
      background:rgba(255,255,255,.95);
      border-radius:22px;
      box-shadow:0 20px 50px rgba(255,90,150,.25);
      padding:28px 22px 36px;
      text-align:center;
    }

    h1{font-size:22px;color:#6b1738}
    p{font-size:17px;color:#421427;line-height:1.55}
    .love-text{font-size:19px;font-weight:700;color:var(--deep)}
    .date{margin-top:10px;font-weight:600;color:#a01846}

    /* SMALL HEART NEAR DATE */
    .heart-wrap{display:flex;gap:8px;align-items:center;justify-content:center;margin-top:10px}
    .mini-heart{
      width:18px;height:18px;background:var(--deep);
      transform:rotate(-45deg);position:relative;
      animation:softbeat 1.4s infinite
    }
    .mini-heart:before,.mini-heart:after{
      content:"";position:absolute;width:18px;height:18px;background:var(--deep);border-radius:50%
    }
    .mini-heart:before{top:-9px}
    .mini-heart:after{left:9px}
    @keyframes softbeat{
      0%,100%{transform:rotate(-45deg) scale(1)}
      50%{transform:rotate(-45deg) scale(1.15)}
    }
      50%{transform:rotate(-45deg) scale(1.25)}
    }

    .question-btn{
      margin-top:26px;padding:14px 22px;border:none;border-radius:30px;
      background:var(--deep);color:#fff;font-size:16px;cursor:pointer
    }

    /* POPUP */
    .overlay{
      position:fixed;inset:0;
      background:rgba(0,0,0,.4);
      display:none;
      align-items:center;justify-content:center;
      animation:fade 1.2s ease forwards;
      z-index:10
    }
    @keyframes fade{from{opacity:0}to{opacity:1}}

    .popup{
      background:#fff;border-radius:22px;padding:26px 22px;
      text-align:center;max-width:340px;width:90%
    }
    .answers{display:flex;gap:12px;margin-top:16px}
    .answers button{flex:1;padding:12px;border:none;border-radius:20px;font-size:15px;cursor:pointer}
    .yes{background:var(--deep);color:#fff}
    .no{background:#ddd;color:#555;position:relative}

    /* FINAL */
    .final{
      position:fixed;inset:0;
      background:linear-gradient(180deg,#ffd4e6,#fff);
      display:none;align-items:center;justify-content:center;
      flex-direction:column;z-index:20;overflow:hidden
    }
    .final h1{font-size:42px;color:var(--deep);animation:beat 1.2s infinite}

    /* FALLING HEARTS */
    .hearts{position:absolute;inset:0;pointer-events:none}
    .fall-heart{
      position:absolute;width:26px;height:26px;background:var(--deep);
      transform:rotate(-45deg);animation:fall linear forwards
    }
    .fall-heart:before,.fall-heart:after{
      content:"";position:absolute;width:26px;height:26px;background:var(--deep);border-radius:50%
    }
    .fall-heart:before{top:-13px}
    .fall-heart:after{left:13px}
    @keyframes fall{from{top:-10%}to{top:110%}}

    /* PARTICLES */
    .particle{
      position:fixed;width:6px;height:6px;border-radius:50%;
      background:radial-gradient(circle,#fff,#ff69b4);
      pointer-events:none;animation:particle 1.2s ease-out forwards
    }
    @keyframes particle{to{transform:translateY(-30px) scale(2);opacity:0}}

    .signature{position:fixed;right:14px;bottom:12px;font-size:14px;color:#6b1738;z-index:30}
    .music-btn{position:fixed;left:14px;bottom:14px;background:var(--deep);color:#fff;border:none;border-radius:20px;padding:10px 16px;cursor:pointer;z-index:30}

    @media(max-width:600px){.final h1{font-size:32px}}
  </style>
</head>
<body>

<div class="card">
  <h1>Pentru piticotu' meu 💕</h1>
  <p>„Sunt cel mai norocos băiețel pentru că am o iubită atât de perfectă. Îi mulțumesc lui Dumnezeu că ai apărut în viața mea și că fiecare zi alături de tine e una de vis.”</p>
  <p class="love-text">Te ador și te iubesc cel mai mult, piticotu' meu 💖</p>

  <p id="promise" style="margin-top:14px;font-size:16px;color:#5a1532;min-height:120px"></p>

  <div class="heart-wrap">
  <div class="date">14 februarie</div>
  <div class="mini-heart"></div>
</div>

<p style="margin-top:16px;font-size:15px;color:#7a1d45;font-style:italic">
  Dacă m-ar întreba cineva unde e locul meu în lume…
  <br/>aș spune fără să clipesc: <strong>lângă tine</strong>.
</p>
  <button class="question-btn" onclick="openPopup()">Am o întrebare pentru tine 💌</button>
</div>

<div class="overlay" id="overlay">
  <div class="popup">
    <h2>Vrei să petreci Ziua Îndrăgostiților cu mine? 💘</h2>
    <div class="answers">
      <button class="yes" onclick="yesAnswer()">DA 💖</button>
      <button class="no" id="noBtn">Nu 🙈</button>
    </div>
  </div>
</div>

<div class="final" id="final">
  <div class="hearts" id="hearts"></div>
  <h1>TE IUBESC ❤️</h1>
<p style="margin-top:14px;font-size:18px;color:#7a1d45;text-align:center;max-width:320px">
  Și te-aș alege din nou.<br/>
  În fiecare zi.<br/>
  În fiecare viață.
</p>
<div class="mini-heart" style="margin-top:18px"></div>
</div>

<div class="signature">Cu drag, nebunu' tău</div>

<button class="music-btn" id="musicBtn">▶️ Play</button>

<!-- YouTube player (GitHub Pages compatible) -->
<script src="https://www.youtube.com/iframe_api"></script>
<div id="player"></div>

<script>
/* TYPEWRITER */
const textPromise = "Vreau să știi că voi fi mereu lângă tine, în zilele frumoase și în cele grele. Orice ar fi, eu sunt aici să te țin de mână, să te fac să zâmbești, să te fac să te simți iubită, apreciată și în siguranță. Fericirea ta e promisiunea mea și inima mea e acasă oriunde ești tu.";
let i=0;
(function type(){
  if(i<textPromise.length){
    promise.innerHTML+=textPromise.charAt(i++);
    setTimeout(type,45);
  }
})();

/* POPUP */
const overlay=document.getElementById('overlay');
const final=document.getElementById('final');
const hearts=document.getElementById('hearts');
function openPopup(){overlay.style.display='flex'}
function yesAnswer(){overlay.style.display='none';final.style.display='flex';startHearts()}

/* NO BUTTON ESCAPE */
const noBtn=document.getElementById('noBtn');
noBtn.addEventListener('mouseenter',()=>{
  noBtn.style.left=Math.random()*120+'px';
  noBtn.style.top=Math.random()*80+'px';
});

/* FALLING HEARTS */
function startHearts(){
  setInterval(()=>{
    const h=document.createElement('div');
    h.className='fall-heart';
    h.style.left=Math.random()*100+'%';
    h.style.animationDuration=(Math.random()*3+4)+'s';
    hearts.appendChild(h);
    setTimeout(()=>h.remove(),8000);
  },160);
}

/* PARTICLES */
function spawn(x,y){
  for(let i=0;i<3;i++){
    const p=document.createElement('div');
    p.className='particle';
    p.style.left=x+'px';
    p.style.top=y+'px';
    document.body.appendChild(p);
    setTimeout(()=>p.remove(),1200);
  }
}
document.addEventListener('mousemove',e=>spawn(e.clientX,e.clientY));
document.addEventListener('touchmove',e=>spawn(e.touches[0].clientX,e.touches[0].clientY));

/* YOUTUBE MUSIC */
let player,isPlaying=false;
function onYouTubeIframeAPIReady(){
  player=new YT.Player('player',{
    height:'0',width:'0',
    videoId:'SM-N4pmi73A',
    playerVars:{'playsinline':1,'loop':1,'playlist':'SM-N4pmi73A'}
  });
}

document.getElementById('musicBtn').onclick=()=>{
  if(player){
    if(!isPlaying){player.playVideo();musicBtn.textContent='⏸ Pauză'}
    else{player.pauseVideo();musicBtn.textContent='▶️ Play'}
    isPlaying=!isPlaying;
  }
};
</script>
</body>
</html>
