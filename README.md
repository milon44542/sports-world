
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Sports World</title>

<style>
*{box-sizing:border-box}

body{
  margin:0;
  font-family:Arial,sans-serif;
  color:#fff;
  background:#06111f;
}

header{
  background:#0b2038;
  padding:20px;
  display:flex;
  justify-content:space-between;
  align-items:center;
  border-bottom:2px solid #087cff;
}

header h1{
  margin:0;
  color:#22aaff;
  font-size:30px;
}

header p{
  margin:5px 0 0;
  color:#b9cee5;
}

.live{
  background:#ed2339;
  padding:10px 14px;
  border-radius:7px;
  font-weight:bold;
}

main{
  max-width:1250px;
  margin:auto;
  padding:20px;
}

/* TOP TV SCREEN */

.tv{
  background:#000;
  padding:8px;
  border:3px solid #29445e;
  border-radius:16px;
  box-shadow:0 10px 35px #0009;
}

.screen{
  position:relative;
  aspect-ratio:16/9;
  background:#000;
  overflow:hidden;
  border-radius:8px;
}

video{
  width:100%;
  height:100%;
  object-fit:contain;
  background:#000;
}

.welcome{
  position:absolute;
  inset:0;
  display:flex;
  flex-direction:column;
  justify-content:center;
  align-items:center;
  text-align:center;
  background:radial-gradient(circle,#123c66,#020711);
  pointer-events:none;
}

.welcome h2{
  font-size:clamp(28px,5vw,55px);
  margin:0 0 10px;
}

.welcome p{
  color:#b9cee5;
}

.tv-info{
  padding:12px 8px 5px;
}

.tv-info h3{
  margin:0 0 5px;
}

.tv-info p{
  color:#b9cee5;
  margin:0;
  font-size:13px;
}

/* SPORTS OPTIONS */

.section{
  margin-top:25px;
}

.section h2{
  margin-bottom:14px;
}

.sports{
  display:grid;
  grid-template-columns:repeat(6,1fr);
  gap:12px;
}

.sport{
  border:0;
  border-radius:12px;
  padding:18px 8px;
  color:white;
  font-weight:bold;
  font-size:15px;
  cursor:pointer;
  transition:.2s;
}

.sport:hover{
  transform:translateY(-3px);
  filter:brightness(1.15);
}

.sport span{
  display:block;
  font-size:30px;
  margin-bottom:9px;
}

.c1{background:#e63946}
.c2{background:#087f5b}
.c3{background:#6d28d9}
.c4{background:#d97706}
.c5{background:#087cff}
.c6{background:#0d9488}

/* DEMO VIDEOS */

.demo-area{
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:18px;
  margin-top:24px;
}

.panel{
  background:#0d2035;
  border:1px solid #29445e;
  border-radius:12px;
  padding:18px;
}

.panel h2{
  margin-top:0;
}

.demo-button{
  display:block;
  width:100%;
  text-align:left;
  background:#122e49;
  border:1px solid #315675;
  border-radius:9px;
  padding:15px;
  color:white;
  margin-bottom:10px;
  cursor:pointer;
  font-size:15px;
}

.demo-button:hover{
  background:#17436c;
}

input{
  width:100%;
  padding:12px;
  margin:7px 0 12px;
  background:#020b14;
  color:white;
  border:1px solid #315675;
  border-radius:7px;
}

.action{
  background:#087cff;
  color:white;
  border:0;
  border-radius:7px;
  padding:12px 17px;
  font-weight:bold;
  cursor:pointer;
}

.note{
  font-size:12px;
  line-height:1.6;
  color:#b9cee5;
}

footer{
  text-align:center;
  padding:25px;
  color:#829bb5;
}

@media(max-width:800px){
  .sports{grid-template-columns:repeat(3,1fr)}
  .demo-area{grid-template-columns:1fr}
}

@media(max-width:480px){
  header{padding:14px}
  header h1{font-size:22px}
  .live{font-size:11px;padding:8px}
  main{padding:12px}
  .sports{grid-template-columns:repeat(2,1fr)}
}
</style>
</head>

<body>

<header>
  <div>
    <h1>🏆 SPORTS WORLD</h1>
    <p>Your World of Sports | Play · Watch · Enjoy</p>
  </div>
  <div class="live">● SPORTS TV</div>
</header>

<main>

  <!-- TV SCREEN AT THE TOP -->

  <section class="tv">
    <div class="screen">

      <video id="player" controls playsinline></video>

      <div class="welcome" id="welcome">
        <h2>🏆 SPORTS WORLD</h2>
        <p>Choose a Demo Video Below</p>
      </div>

    </div>

    <div class="tv-info">
      <h3 id="videoTitle">Ready to Play</h3>
      <p id="videoStatus">Select a demo video to start watching.</p>
    </div>
  </section>

  <!-- SPORTS OPTIONS BELOW THE TV -->

  <section class="section">
    <h2>🎮 Sports Options</h2>

    <div class="sports">

      <button class="sport c1" data-sport="Cricket">
        <span>🏏</span>Cricket
      </button>

      <button class="sport c2" data-sport="Football">
        <span>⚽</span>Football
      </button>

      <button class="sport c3" data-sport="Badminton">
        <span>🏸</span>Badminton
      </button>

      <button class="sport c4" data-sport="Basketball">
        <span>🏀</span>Basketball
      </button>

      <button class="sport c5" data-sport="Tennis">
        <span>🎾</span>Tennis
      </button>

      <button class="sport c6" data-sport="Others">
        <span>🏆</span>Others
      </button>

    </div>
  </section>

  <!-- DEMO VIDEO AND CUSTOM VIDEO OPTIONS -->

  <section class="demo-area">

    <div class="panel">
      <h2>▶ Demo Videos</h2>

      <button class="demo-button" data-demo="flower">
        🌸 Demo Video — Flower
      </button>

      <button class="demo-button" data-demo="bunny">
        🎬 Demo Video — Big Buck Bunny
      </button>

      <p class="note">
        Demo ভিডিও চালাতে উপরের যেকোনো বাটনে ক্লিক করুন।
        ভিডিও TV Screen-এ চলবে।
      </p>
    </div>

    <div class="panel">
      <h2>📂 Play Your Own Video</h2>

      <input type="file" id="videoFile" accept="video/*">

      <h2>🌐 Video Stream URL</h2>

      <input
        type="url"
        id="streamUrl"
        placeholder="Paste direct video URL here"
      >

      <button class="action" id="playStream">
        ▶ Play Stream
      </button>

      <p class="note">
        নিজের ভিডিও অথবা অনুমোদিত সরাসরি ভিডিও URL ব্যবহার করুন।
        সাধারণ YouTube পেজের লিংক এখানে সরাসরি নাও চলতে পারে।
      </p>
    </div>

  </section>

</main>

<footer>
  © 2026 Sports World | Made for Sports Fans
</footer>

<script>
const player = document.getElementById("player");
const welcome = document.getElementById("welcome");
const title = document.getElementById("videoTitle");
const status = document.getElementById("videoStatus");

const demoVideos = {
  flower: {
    name: "Demo Video — Flower",
    url: "https://interactive-examples.mdn.mozilla.net/media/cc0-videos/flower.mp4"
  },
  bunny: {
    name: "Demo Video — Big Buck Bunny",
    url: "https://storage.googleapis.com/gtv-videos-bucket/sample/BigBuckBunny.mp4"
  }
};

function playVideo(url, name) {
  welcome.style.display = "none";
  player.src = url;
  title.textContent = name;
  status.textContent = "Loading video...";
  player.load();

  player.play()
    .then(() => {
      status.textContent = "Video is playing.";
    })
    .catch(() => {
      status.textContent =
        "Press the play button or check the video URL.";
    });
}

document.querySelectorAll("[data-demo]").forEach(button => {
  button.addEventListener("click", () => {
    const video = demoVideos[button.dataset.demo];
    playVideo(video.url, video.name);
  });
});

document.getElementById("videoFile").addEventListener("change", event => {
  const file = event.target.files[0];

  if (file) {
    const localUrl = URL.createObjectURL(file);
    playVideo(localUrl, file.name);
  }
});

document.getElementById("playStream").addEventListener("click", () => {
  const url = document.getElementById("streamUrl").value.trim();

  if (!url) {
    status.textContent = "Please enter a video URL.";
    return;
  }

  playVideo(url, "Custom Video Stream");
});

player.addEventListener("error", () => {
  status.textContent =
    "Video unavailable. Try another demo or compatible video URL.";
});

document.querySelectorAll("[data-sport]").forEach(button => {
  button.addEventListener("click", () => {
    document.querySelectorAll("[data-sport]").forEach(item => {
      item.style.outline = "none";
    });

    button.style.outline = "3px solid white";

    status.textContent =
      button.dataset.sport + " selected. Choose a video below.";
  });
});
</script>

</body>
</html>
