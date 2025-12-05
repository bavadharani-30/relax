<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Relax & Chill, Pa</title>
<link href="https://fonts.googleapis.com/css2?family=Baloo+2&display=swap" rel="stylesheet">
<style>
  body {
    margin:0; padding:0;
    font-family: 'Baloo 2', cursive;
    overflow:hidden;
    background: linear-gradient(to bottom, #a1c4fd, #c2e9fb); /* soft sky blue gradient */
    perspective:1000px;
  }
  .overlay {
    position: absolute;
    width:100%;
    height:100%;
    background: rgba(0,0,0,0.1); 
    z-index:0;
  }
  .card-container {
    position: relative; width:400px; height:480px; margin:auto; z-index:1; top:50px;
  }
  .card {
    width:100%; height:100%;
    background: rgba(255,255,255,0.85);
    border-radius:25px;
    box-shadow:0 20px 60px rgba(0,0,0,0.3);
    position:absolute; top:0; left:0;
    display:flex; flex-direction:column;
    justify-content:center; align-items:center; text-align:center;
    padding:25px; transform-style: preserve-3d;
    backface-visibility:hidden;
    transition: transform 0.8s ease, opacity 0.8s ease;
    opacity:0; cursor:default;
  }
  .visible { opacity:1; transform: rotateY(0deg) translateZ(0px); z-index:10; }
  .hidden { opacity:0; transform: rotateY(90deg) translateZ(-100px); z-index:1; pointer-events:none; }

  h1 { font-size:2rem; cursor:pointer; color:#333; text-shadow: 1px 1px 5px rgba(255,255,255,0.7); transition:0.3s; }
  h1:hover { transform: scale(1.05); }

  button { margin-top:20px; padding:12px 28px; background:#4facfe; border:none; border-radius:15px; color:white; font-size:1rem; cursor:pointer; transition:0.3s;}
  button:hover { background:#00f2fe; transform:scale(1.05); box-shadow:0 0 12px rgba(0,252,255,0.5); }

  .poetic { font-style: italic; color: #0077b6; margin-top:10px; font-size: 1rem; text-shadow: 1px 1px 4px rgba(255,255,255,0.6); }
  .kannada { font-weight:bold; color:#e15a29; font-size:1.1rem; margin-top:10px; text-shadow: 1px 1px 4px rgba(0,0,0,0.5); }
  p { color:#023e8a; font-size:1rem; line-height:1.4; text-shadow:1px 1px 2px rgba(255,255,255,0.6);}

  .poetic-box {
    margin-top: 15px;
    background: rgba(255, 250, 240, 0.6);
    padding: 15px 18px;
    border-radius: 12px;
    font-style: italic;
    font-size: 0.95rem;
    color: #ff4500;
    text-shadow: 1px 1px 3px rgba(0,0,0,0.4);
    opacity:0;
    transition: opacity 2s ease-in;
  }
  .message-box {
    width: 90%;
    margin: 15px auto 0 auto;
    text-align: left;
    color: #023e8a;
    font-size: 0.95rem;
    line-height: 1.5;
    overflow-y: auto;
    max-height: 300px;
  }
</style>
</head>
<body>

<div class="overlay"></div>

<div class="card-container">
  <div id="card0" class="card visible">
    <h1>Hey Pa! Ready to relax?</h1>
    <p class="poetic">“Even the sun hides behind clouds, yet it still shines beyond.”</p>
    <button onclick="nextCard()">Start</button>
  </div>

  <div id="card1" class="card hidden">
    <p>Even strong minds need small breaks 😏. Chill da!</p>
    <p class="poetic">“Let the wind carry your worries far away.”</p>
    <button onclick="nextCard()">Next</button>
  </div>

  <div id="card2" class="card hidden">
    <p>Imagine floating through clouds ☁️… wind in your hair… just you and the sky 🌈.</p>
    <p class="poetic">“Clouds may drift, but your spirit can soar.”</p>
    <button onclick="nextCard()">Next</button>
  </div>

  <div id="card3" class="card hidden">
    <p>Breathe… nothing needs fixing now. You’re okay, pa. I got your back.</p>
    <p class="poetic">“The night is soft, and so can you be.”</p>
    <button onclick="nextCard()">Next</button>
  </div>

  <div id="card4" class="card hidden">
    <p class="kannada">"ನೀನು ತುಂಬ ಒಳ್ಳೆಯ ಹುಡುಗ. ಎಲ್ಲಾ ಕಷ್ಟಗಳನ್ನು ತಾಳುವುದು ಸುಲಭವಲ್ಲ… ಆದರೆ ನೀನು ಇದನ್ನು ನಿರ್ವಹಿಸಬಹುದು. ಮನಸ್ಸು ಸ್ವಲ್ಪ ವಿಶ್ರಾಂತಿಸು <break></break>


"Neenu thumba olle huduga. Yella kashtagalu tagedukollodu easy alla… aadre neenu handle maadbahudu. Ninna manasu swalpa relax maadiko.""</p>
    <p>Smile… let go of heaviness for a while.</p>
    <p class="poetic">“Even stars need darkness to shine.”</p>
    <button onclick="nextCard()">Next</button>
  </div>

  <!-- New card for poetic message box -->
    <div id="card5" class="card hidden">
    <div class="poetic-box" id="poeticBox">
      “Even when clouds hide the sun, remember: your light shines quietly, waiting to warm your day.”
    </div>

    <div class="message-box">
      Hey Pa,<br><br>
      Take a deep breath. 🌿 I know today feels heavy, but listen… you’re still bold, strong, and completely lovable. Don’t let anyone or anything steal your peace. Right now, your mind needs a break, not more worry.<br><br>
      Remember, exams don’t care about feelings; they just want your brain at its best. So focus on that, chill a little, and let the rest wait.<br><br>
      If things get too much, I’m here. Maybe I can’t fix everything, but I can be a listener—someone to let you breathe, laugh, or just rant. 😂 Life hits us with bad days sometimes, and that’s okay. Everyone needs one… even heroes like you.<br><br>
      So here’s the plan:<br>
      - Study well, without thinking too much.<br>
      - Take small breaks, laugh at something silly, and just relax.<br>
      - And… for a little vibe boost, play “Pick Up the Phone” by Henry Moodie—let the music remind you that it’s gonna be okay. 🎵<br><br>
      Lastly… just a little Kannada touch for you:<br>
      “Neenu iddira, matte ella sari agutte. Chill maadi, Pa!”
    </div>

    <button style="margin-top:25px;" onclick="nextCard()">Next</button>
  </div>

  <!-- Last card: YouTube redirect -->
  <div id="card6" class="card hidden">
    <p>Pa, do you want to hear something to lift your mood? 🎵</p>
    <button onclick="playSong()">Yes, play it!</button>
    <p style="margin-top:15px; font-size:0.9rem; color:#023e8a;">
      Focus on your exam. If it feels heavy, I’m here as a friend to listen. You can breathe and relax.
    </p>
  </div>
</div>

<script>
let current=0;
const total=7; // updated total number of cards

function nextCard(){
  document.getElementById('card'+current).classList.remove('visible');
  document.getElementById('card'+current).classList.add('hidden');
  current++;
  if(current<total){
    document.getElementById('card'+current).classList.remove('hidden');
    document.getElementById('card'+current).classList.add('visible');

    // Fade in poetic box only on card5
    if(current === 5){
      setTimeout(()=> {
        document.getElementById('poeticBox').style.opacity = 1;
      }, 500);
    }
  }
}

// Redirect to YouTube link when he clicks Yes
function playSong() {
  window.open('https://www.youtube.com/watch?v=gBOHWEgajP0', '_blank');
}

// 3D tilt effect for cards
const cards = document.querySelectorAll('.card');
cards.forEach(card=>{
  card.addEventListener('mousemove', (e)=>{
    const rect = card.getBoundingClientRect();
    const x = e.clientX - rect.left - rect.width/2;
    const y = e.clientY - rect.top - rect.height/2;
    card.style.transform = `rotateY(${x/15}deg) rotateX(${-y/15}deg) translateZ(0px)`;
  });
  card.addEventListener('mouseleave', ()=>{
    card.style.transform = 'rotateY(0deg) rotateX(0deg) translateZ(0px)';
  });
});
</script>
</body>
</html>

