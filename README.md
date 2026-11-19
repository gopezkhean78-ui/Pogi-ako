
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#090812">
<title>Domain Expansion | Khean Aislie S. Gopez</title>

<link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@500;600;700;800&family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet">

<style>
:root {
  --bg: #090812;
  --panel: #171429;
  --text: #f6f1ff;
  --muted: #b8b1ca;
  --purple: #a78bfa;
  --cyan: #72e5f4;
  --border: rgba(190,166,255,.22);
}

* { box-sizing: border-box; }

html { scroll-behavior: smooth; }

body {
  margin: 0;
  background:
    radial-gradient(ellipse at 80% 0%,rgba(103,65,168,.23),transparent 38%),
    radial-gradient(ellipse at 10% 35%,rgba(38,128,153,.12),transparent 35%),
    var(--bg);
  color: var(--text);
  font-family: Inter, sans-serif;
  line-height: 1.6;
  overflow-x: hidden;
}

body::before {
  content: "";
  position: fixed;
  inset: 0;
  pointer-events: none;
  opacity: .15;
  background-image:
    linear-gradient(rgba(255,255,255,.035) 1px,transparent 1px),
    linear-gradient(90deg,rgba(255,255,255,.035) 1px,transparent 1px);
  background-size: 48px 48px;
  z-index: -1;
}

a { color: inherit; text-decoration: none; }
button, input, textarea { font: inherit; }

.wrap {
  width: min(1120px,calc(100% - 40px));
  margin: auto;
}

nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 22px 0;
  gap: 20px;
}

.brand {
  font-family: Cinzel,serif;
  font-weight: 800;
  letter-spacing: .12em;
  font-size: 14px;
}

.brand span { color: var(--cyan); }

.navlinks {
  display: flex;
  gap: 22px;
  flex-wrap: wrap;
  color: var(--muted);
  font-size: 12px;
  text-transform: uppercase;
  letter-spacing: .12em;
}

.navlinks a:hover { color: var(--cyan); }

.profile-float {
  position: absolute;
  right: 0;
  top: 12px;
  width: 190px;
  padding: 13px;
  background: rgba(20,18,34,.85);
  border: 1px solid var(--border);
  backdrop-filter: blur(12px);
  border-radius: 8px;
  z-index: 2;
  box-shadow: 0 0 30px rgba(167,139,250,.18);
}

.profile-float .mini {
  font-size: 9px;
  letter-spacing: .2em;
  color: var(--cyan);
  text-transform: uppercase;
}

.profile-float strong {
  display: block;
  font-family: Cinzel,serif;
  font-size: 13px;
  margin: 4px 0;
}

.profile-float small {
  color: var(--muted);
  font-size: 10px;
}

.hero {
  min-height: 610px;
  display: grid;
  grid-template-columns: 1.15fr .85fr;
  align-items: center;
  gap: 45px;
  padding: 65px 0 80px;
  position: relative;
  border: 0;
}

.eyebrow {
  color: var(--cyan);
  font-size: 11px;
  font-weight: 800;
  letter-spacing: .28em;
  text-transform: uppercase;
}

.hero h1 {
  font-family: Cinzel,serif;
  font-size: clamp(42px,7vw,82px);
  line-height: 1.03;
  margin: 18px 0;
  letter-spacing: -.04em;
  text-shadow: 0 0 32px rgba(167,139,250,.24);
}

.hero h1 em {
  font-style: normal;
  color: var(--purple);
}

.hero p {
  max-width: 570px;
  color: var(--muted);
  font-size: 15px;
}

.actions {
  display: flex;
  gap: 12px;
  flex-wrap: wrap;
  margin-top: 28px;
}

.btn {
  border: 1px solid var(--border);
  background: linear-gradient(135deg,rgba(167,139,250,.2),rgba(114,229,244,.08));
  color: var(--text);
  padding: 12px 18px;
  border-radius: 5px;
  font-size: 11px;
  font-weight: 800;
  letter-spacing: .12em;
  text-transform: uppercase;
  cursor: pointer;
  transition: .25s;
}

.btn:hover {
  transform: translateY(-3px);
  border-color: var(--cyan);
  box-shadow: 0 0 25px rgba(167,139,250,.2);
}

.btn.primary {
  background: linear-gradient(100deg,#7454bb,#347f91);
  border: 0;
}

.domain-art {
  height: 410px;
  display: grid;
  place-items: center;
  position: relative;
}

.orb {
  width: min(330px,75vw);
  aspect-ratio: 1;
  border-radius: 50%;
  position: relative;
  background:
    radial-gradient(circle at 50% 50%,#17142c 0 27%,transparent 28%),
    conic-gradient(from 10deg,transparent,#a78bfa,transparent,#72e5f4,transparent,#a78bfa,transparent);
  filter: drop-shadow(0 0 28px rgba(167,139,250,.25));
  animation: rotate 22s linear infinite;
}

.orb::before,.orb::after {
  content: "";
  position: absolute;
  inset: 12%;
  border: 1px solid rgba(114,229,244,.6);
  border-radius: 50%;
  transform: rotateX(68deg) rotate(30deg);
}

.orb::after {
  inset: 22%;
  border-color: rgba(199,172,255,.7);
  transform: rotateY(68deg) rotate(-30deg);
}

.orbcore {
  position: absolute;
  inset: 35%;
  border-radius: 50%;
  background: radial-gradient(circle,#d9d0ff 0,#9874ef 18%,#211a3e 60%,transparent 72%);
  box-shadow: 0 0 50px #8b6bdc;
  animation: pulse 3s ease-in-out infinite;
}

.seal {
  position: absolute;
  font-family: Cinzel,serif;
  letter-spacing: .3em;
  font-size: 10px;
  color: #d8ccff;
  top: 50%;
  left: 50%;
  transform: translate(-50%,-50%);
  white-space: nowrap;
  text-shadow: 0 0 12px var(--purple);
}

section {
  padding: 72px 0;
  border-top: 1px solid rgba(190,166,255,.1);
}

.section-head {
  display: flex;
  align-items: end;
  justify-content: space-between;
  gap: 20px;
  margin-bottom: 30px;
}

.section-head h2 {
  font-family: Cinzel,serif;
  font-size: clamp(25px,4vw,38px);
  margin: 7px 0 0;
}

.section-head p {
  color: var(--muted);
  font-size: 12px;
  max-width: 350px;
  margin: 0;
}

.panel {
  background: linear-gradient(145deg,rgba(27,24,48,.94),rgba(16,14,27,.94));
  border: 1px solid var(--border);
  border-radius: 10px;
  padding: 26px;
  box-shadow: 0 0 30px rgba(167,139,250,.12);
}

.about-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 18px;
}

.about-grid h3,.card h3 {
  font-family: Cinzel,serif;
  margin: 0 0 10px;
}

.muted { color: var(--muted); }

.editable {
  outline: none;
  border-radius: 3px;
  transition: background .2s;
}

.editable[contenteditable="true"]:hover,
.editable[contenteditable="true"]:focus {
  background: rgba(167,139,250,.09);
  box-shadow: 0 0 0 5px rgba(167,139,250,.09);
}

.edit-hint {
  font-size: 10px;
  color: #9b91b5;
  margin-top: 14px;
}

.edit-tools {
  display: flex;
  gap: 8px;
  flex-wrap: wrap;
  margin-top: 16px;
}

.tiny {
  font-size: 10px;
  padding: 8px 11px;
}

.learning-list {
  display: grid;
  gap: 10px;
}

.learning-row {
  display: flex;
  gap: 12px;
  align-items: center;
  background: rgba(255,255,255,.025);
  border: 1px solid rgba(190,166,255,.12);
  padding: 12px;
  border-radius: 6px;
}

.learning-row .num {
  font-family: Cinzel,serif;
  color: var(--cyan);
  font-size: 12px;
}

.learning-row .line {
  flex: 1;
  min-width: 0;
  color: #e8e2f5;
  font-size: 13px;
}

.learning-row button {
  background: transparent;
  border: 0;
  color: #a99fbd;
  cursor: pointer;
  font-size: 16px;
}

.learning-row button:hover { color: #ff9aaf; }

.cards {
  display: grid;
  grid-template-columns: repeat(3,1fr);
  gap: 16px;
}

.card {
  position: relative;
  min-height: 190px;
  background: linear-gradient(150deg,rgba(31,26,53,.96),rgba(15,14,25,.96));
  border: 1px solid var(--border);
  border-radius: 9px;
  padding: 20px;
  overflow: hidden;
  transition: transform .25s,border-color .25s,box-shadow .25s;
}

.card::after {
  content: "";
  position: absolute;
  width: 150px;
  height: 150px;
  border: 1px solid rgba(114,229,244,.16);
  border-radius: 50%;
  right: -80px;
  bottom: -90px;
  box-shadow: 0 0 0 15px rgba(167,139,250,.035),0 0 0 30px rgba(167,139,250,.025);
  pointer-events: none;
}

.card:hover {
  transform: translateY(-7px);
  border-color: var(--cyan);
  box-shadow: 0 12px 35px rgba(0,0,0,.28),0 0 24px rgba(114,229,244,.1);
}

.card .tag {
  font-size: 9px;
  letter-spacing: .2em;
  color: var(--cyan);
  text-transform: uppercase;
  font-weight: 800;
}

.card h3 {
  font-size: 17px;
  margin: 12px 0 8px;
}

.card p {
  font-size: 12px;
  color: var(--muted);
  margin: 0 0 15px;
  max-width: 90%;
}

.card .placeholder {
  display: inline-block;
  color: #c5b5f7;
  font-size: 10px;
  border-bottom: 1px dashed rgba(197,181,247,.5);
  padding-bottom: 2px;
}

.card .card-actions {
  position: absolute;
  right: 13px;
  top: 12px;
  display: flex;
  gap: 4px;
  z-index: 2;
}

.card-actions button {
  background: rgba(9,8,18,.8);
  color: #c7bddb;
  border: 1px solid var(--border);
  border-radius: 4px;
  width: 25px;
  height: 25px;
  cursor: pointer;
}

.card-actions button:hover {
  color: var(--cyan);
  border-color: var(--cyan);
}

footer {
  padding: 30px 0 45px;
  color: #8d849f;
  font-size: 10px;
  letter-spacing: .12em;
  text-align: center;
}

.modal {
  position: fixed;
  inset: 0;
  background: rgba(3,2,8,.8);
  display: none;
  place-items: center;
  padding: 20px;
  z-index: 20;
}

.modal.open { display: grid; }

.modal-box {
  width: min(480px,100%);
  background: #171429;
  border: 1px solid var(--purple);
  border-radius: 10px;
  padding: 24px;
  box-shadow: 0 0 60px rgba(130,90,220,.25);
}

.modal-box h3 {
  font-family: Cinzel,serif;
  margin-top: 0;
}

.modal-box label {
  display: block;
  font-size: 10px;
  letter-spacing: .13em;
  text-transform: uppercase;
  color: var(--cyan);
  margin: 12px 0 5px;
}

.modal-box input,.modal-box textarea {
  width: 100%;
  background: #0b0915;
  color: var(--text);
  border: 1px solid var(--border);
  border-radius: 4px;
  padding: 10px;
  font-size: 12px;
}

.modal-box textarea {
  min-height: 85px;
  resize: vertical;
}

.modal-actions {
  display: flex;
  justify-content: flex-end;
  gap: 8px;
  margin-top: 18px;
}

@keyframes rotate {
  to { transform: rotate(360deg); }
}

@keyframes pulse {
  50% { transform: scale(1.12); filter: brightness(1.4); }
}

@keyframes rise {
  from { opacity: 0; transform: translateY(22px); }
  to { opacity: 1; transform: translateY(0); }
}

.reveal { animation: rise .8s both; }
.delay { animation-delay: .15s; }

@media(max-width:760px) {
  .hero {
    grid-template-columns: 1fr;
    padding-top: 95px;
    gap: 0;
  }

  .domain-art {
    height: 300px;
    grid-row: 1;
  }

  .hero-copy { grid-row: 2; }
  .profile-float { top: 8px; right: 0; width: 170px; }
  .about-grid { grid-template-columns: 1fr; }
  .cards { grid-template-columns: repeat(2,1fr); }
  .navlinks { gap: 12px; }
  .section-head {
    align-items: start;
    flex-direction: column;
  }
}

@media(max-width:480px) {
  .wrap { width: min(100% - 28px,1120px); }

  nav {
    align-items: flex-start;
    flex-direction: column;
  }

  .hero {
    min-height: auto;
    padding: 105px 0 60px;
  }

  .domain-art { height: 250px; }
  .cards { grid-template-columns: 1fr; }
  .panel { padding: 19px; }
  .profile-float { width: 155px; }
  .profile-float strong { font-size: 11px; }
}

@media(prefers-reduced-motion:reduce) {
  *,*::before,*::after {
    animation-duration: .01ms !important;
    animation-iteration-count: 1 !important;
    scroll-behavior: auto !important;
    transition: none !important;
  }
}
</style>
</head>

<body>

<header class="wrap">
  <nav>
    <a class="brand" href="#">DOMAIN <span>EXPANSION</span></a>

    <div class="navlinks">
      <a href="#about">Profile</a>
      <a href="#learning">Learning</a>
      <a href="#midterm">Midterm</a>
      <a href="#final">Final</a>
    </div>
  </nav>
</header>

<main>
<div class="wrap">

  <!-- EDITABLE PROFILE AT THE UPPER RIGHT -->
  <div class="profile-float">
    <div class="mini">Sorcerer Profile · Editable</div>
    <strong class="editable" contenteditable="true" data-save="quick-name">Gopez, Khean Aislie S.</strong>
    <small class="editable" contenteditable="true" data-save="quick-role">Student · Portfolio</small>
  </div>

  <!-- HERO SECTION -->
  <section class="hero" style="border:0;padding-top:35px">

    <div class="hero-copy reveal">
      <div class="eyebrow">A record of growth • skills • technique</div>

      <h1>Enter my<br><em>Domain.</em></h1>

      <p class="editable" contenteditable="true" data-save="hero-intro">
        Welcome to my portfolio. This is where I document my learning journey,
        showcase my laboratory activities, and reflect on the skills I develop
        along the way.
      </p>

      <div class="actions">
        <a class="btn primary" href="#midterm">Explore My Work ↘</a>
        <a class="btn" href="#about">Meet the Sorcerer</a>
      </div>
    </div>

    <div class="domain-art reveal delay">
      <div class="orb">
        <div class="orbcore"></div>
        <div class="seal">DOMAIN EXPANSION</div>
      </div>
    </div>

  </section>

  <!-- ABOUT ME -->
  <section id="about">

    <div class="section-head">
      <div>
        <div class="eyebrow">01 / Identity</div>
        <h2>Profile & About Me</h2>
      </div>
      <p>Your story is your technique. Click the text to edit it.</p>
    </div>

    <div class="about-grid">

      <article class="panel">
        <h3>About the Sorcerer</h3>

        <p class="muted editable" contenteditable="true" data-save="about">
          Hello! I’m Khean Aislie S. Gopez. I am a student who is eager to learn,
          explore new ideas, and improve through hands-on activities. I value
          creativity, perseverance, and continuous growth. This portfolio is
          a collection of my experiences, outputs, and progress.
        </p>

        <div class="edit-hint">
          ✦ Click this paragraph to personalize your introduction.
        </div>
      </article>

      <article class="panel">
        <h3>Personal Details</h3>

        <p>
          <span class="eyebrow">Name</span><br>
          <span class="editable" contenteditable="true" data-save="full-name">
            Gopez, Khean Aislie S.
          </span>
        </p>

        <p>
          <span class="eyebrow">Course / Section</span><br>
          <span class="editable" contenteditable="true" data-save="course">
            Add your course and section here
          </span>
        </p>

        <p>
          <span class="eyebrow">My Goal</span><br>
          <span class="editable" contenteditable="true" data-save="goal">
            To turn every challenge into an opportunity to learn and improve.
          </span>
        </p>
      </article>

    </div>
  </section>

  <!-- LEARNING SECTION -->
  <section id="learning">

    <div class="section-head">
      <div>
        <div class="eyebrow">02 / Progress Log</div>
        <h2>What I'm Learning</h2>
      </div>
      <p>Add reflections one line at a time. Each entry is saved in this browser.</p>
    </div>

    <div class="panel">

      <div class="learning-list" id="learningList">

        <div class="learning-row">
          <span class="num">01</span>
          <span class="line editable" contenteditable="true">
            I am learning to apply concepts through practical laboratory activities.
          </span>
          <button title="Delete line" onclick="this.parentElement.remove();saveAll()">×</button>
        </div>

        <div class="learning-row">
          <span class="num">02</span>
          <span class="line editable" contenteditable="true">
            I am improving my problem-solving, creativity, and technical skills.
          </span>
          <button title="Delete line" onclick="this.parentElement.remove();saveAll()">×</button>
        </div>

      </div>

      <div class="edit-tools">
        <button class="btn tiny" onclick="addLearning()">
          ＋ Add Learning Line
        </button>
      </div>

    </div>
  </section>

  <!-- MIDTERM TASKS -->
  <section id="midterm">

    <div class="section-head">
      <div>
        <div class="eyebrow">03 / First Checkpoint</div>
        <h2>Midterm Lab Tasks</h2>
      </div>
      <p>Replace each placeholder with your laboratory title, description, and file or image link.</p>
    </div>

    <div class="cards" id="midtermCards">

      <article class="card">
        <div class="card-actions">
          <button onclick="editCard(this)" title="Edit">✎</button>
          <button onclick="deleteCard(this)" title="Delete">×</button>
        </div>
        <div class="tag">Midterm · Lab 01</div>
        <h3 class="editable" contenteditable="true">Laboratory Task 01</h3>
        <p class="editable" contenteditable="true">Add a short summary of the activity, process, or skills practiced.</p>
        <span class="placeholder editable" contenteditable="true">[ Add task link / image ]</span>
      </article>

      <article class="card">
        <div class="card-actions">
          <button onclick="editCard(this)" title="Edit">✎</button>
          <button onclick="deleteCard(this)" title="Delete">×</button>
        </div>
        <div class="tag">Midterm · Lab 02</div>
        <h3 class="editable" contenteditable="true">Laboratory Task 02</h3>
        <p class="editable" contenteditable="true">Add a short summary of the activity, process, or skills practiced.</p>
        <span class="placeholder editable" contenteditable="true">[ Add task link / image ]</span>
      </article>

      <article class="card">
        <div class="card-actions">
          <button onclick="editCard(this)" title="Edit">✎</button>
          <button onclick="deleteCard(this)" title="Delete">×</button>
        </div>
        <div class="tag">Midterm · Lab 03</div>
        <h3 class="editable" contenteditable="true">Laboratory Task 03</h3>
        <p class="editable" contenteditable="true">Add a short summary of the activity, process, or skills practiced.</p>
        <span class="placeholder editable" contenteditable="true">[ Add task link / image ]</span>
      </article>

    </div>

    <div class="edit-tools">
      <button class="btn tiny" onclick="addCard('midtermCards','Midterm')">
        ＋ Add Midterm Task
      </button>
    </div>

  </section>

  <!-- FINAL TASKS -->
  <section id="final">

    <div class="section-head">
      <div>
        <div class="eyebrow">04 / Final Checkpoint</div>
        <h2>Final Lab Tasks</h2>
      </div>
      <p>Keep building your archive. You can add, edit, or remove task cards.</p>
    </div>

    <div class="cards" id="finalCards">

      <article class="card">
        <div class="card-actions">
          <button onclick="editCard(this)" title="Edit">✎</button>
          <button onclick="deleteCard(this)" title="Delete">×</button>
        </div>
        <div class="tag">Final · Lab 01</div>
        <h3 class="editable" contenteditable="true">Final Laboratory Task 01</h3>
        <p class="editable" contenteditable="true">Add a short summary of the activity, process, or skills practiced.</p>
        <span class="placeholder editable" contenteditable="true">[ Add task link / image ]</span>
      </article>

      <article class="card">
        <div class="card-actions">
          <button onclick="editCard(this)" title="Edit">✎</button>
          <button onclick="deleteCard(this)" title="Delete">×</button>
        </div>
        <div class="tag">Final · Lab 02</div>
        <h3 class="editable" contenteditable="true">Final Laboratory Task 02</h3>
        <p class="editable" contenteditable="true">Add a short summary of the activity, process, or skills practiced.</p>
        <span class="placeholder editable" contenteditable="true">[ Add task link / image ]</span>
      </article>

      <article class="card">
        <div class="card-actions">
          <button onclick="editCard(this)" title="Edit">✎</button>
          <button onclick="deleteCard(this)" title="Delete">×</button>
        </div>
        <div class="tag">Final · Lab 03</div>
        <h3 class="editable" contenteditable="true">Final Laboratory Task 03</h3>
        <p class="editable" contenteditable="true">Add a short summary of the activity, process, or skills practiced.</p>
        <span class="placeholder editable" contenteditable="true">[ Add task link / image ]</span>
      </article>

    </div>

    <div class="edit-tools">
      <button class="btn tiny" onclick="addCard('finalCards','Final')">
        ＋ Add Final Task
      </button>
    </div>

  </section>

</div>
</main>

<footer>
  <div class="wrap">
    GOPEZ, KHEAN AISLIE S. · DOMAIN EXPANSION PORTFOLIO
  </div>
</footer>

<!-- EDIT TASK POPUP -->
<div class="modal" id="cardModal" role="dialog" aria-modal="true">

  <div class="modal-box">
    <h3>Edit Laboratory Task</h3>

    <label for="taskTitle">Task Title</label>
    <input id="taskTitle">

    <label for="taskDesc">Description</label>
    <textarea id="taskDesc"></textarea>

    <label for="taskLink">Link / File Reference (Optional)</label>
    <input id="taskLink" placeholder="Paste a URL or write a file name">

    <div class="modal-actions">
      <button class="btn tiny" onclick="closeModal()">Cancel</button>
      <button class="btn primary tiny" onclick="saveModal()">Save Task</button>
    </div>
  </div>

</div>

<script>
const STORE = "domainExpansionPortfolio_v2";

/* SAVE PORTFOLIO CONTENT */
function saveAll() {
  const data = {};

  document.querySelectorAll("[data-save]").forEach(el => {
    data[el.dataset.save] = el.innerHTML;
  });

  data.learning = document.getElementById("learningList").innerHTML;
  data.midterm = document.getElementById("midtermCards").innerHTML;
  data.final = document.getElementById("finalCards").innerHTML;

  try {
    localStorage.setItem(STORE, JSON.stringify(data));
  } catch(e) {
    console.log("Unable to save portfolio.");
  }
}

/* RESTORE SAVED CONTENT */
function restore() {
  try {
    const data = JSON.parse(localStorage.getItem(STORE) || "{}");

    Object.entries(data).forEach(([key,value]) => {
      if (key === "learning") {
        document.getElementById("learningList").innerHTML = value;
      } else if (key === "midterm") {
        document.getElementById("midtermCards").innerHTML = value;
      } else if (key === "final") {
        document.getElementById("finalCards").innerHTML = value;
      } else {
        const el = document.querySelector(
          `[data-save="${CSS.escape(key)}"]`
        );
        if (el) el.innerHTML = value;
      }
    });

  } catch(e) {
    console.log("Unable to restore saved content.");
  }
}

/* AUTOMATICALLY SAVE EDITABLE TEXT */
document.addEventListener("input", function(e) {
  if (e.target.matches('[contenteditable="true"]')) {
    saveAll();
  }
});

/* ADD LEARNING LINE */
function addLearning() {
  const list = document.getElementById("learningList");
  const number = list.children.length + 1;

  const row = document.createElement("div");
  row.className = "learning-row";

  row.innerHTML = `
    <span class="num">${String(number).padStart(2,"0")}</span>
    <span class="line editable" contenteditable="true">
      Write one thing you learned...
    </span>
    <button title="Delete line"
      onclick="this.parentElement.remove();saveAll()">×</button>
  `;

  list.appendChild(row);
  row.querySelector(".line").focus();
  saveAll();
}

/* EDIT TASK CARD */
let activeCard = null;

function editCard(button) {
  activeCard = button.closest(".card");

  document.getElementById("taskTitle").value =
    activeCard.querySelector("h3").innerText;

  document.getElementById("taskDesc").value =
    activeCard.querySelector("p").innerText;

  document.getElementById("taskLink").value =
    activeCard.querySelector(".placeholder").innerText;

  document.getElementById("cardModal").classList.add("open");
}

/* CLOSE TASK EDITOR */
function closeModal() {
  document.getElementById("cardModal").classList.remove("open");
  activeCard = null;
}

/* SAVE TASK CARD */
function saveModal() {
  if (!activeCard) return;

  activeCard.querySelector("h3").innerText =
    document.getElementById("taskTitle").value || "Untitled Laboratory Task";

  activeCard.querySelector("p").innerText =
    document.getElementById("taskDesc").value;

  activeCard.querySelector(".placeholder").innerText =
    document.getElementById("taskLink").value || "[ Add task link / image ]";

  saveAll();
  closeModal();
}

/* DELETE TASK CARD */
function deleteCard(button) {
  if (confirm("Remove this laboratory task card?")) {
    button.closest(".card").remove();
    saveAll();
  }
}

/* ADD NEW TASK CARD */
function addCard(target,label) {
  const container = document.getElementById(target);
  const number = container.querySelectorAll(".card").length + 1;

  const card = document.createElement("article");
  card.className = "card";

  card.innerHTML = `
    <div class="card-actions">
      <button onclick="editCard(this)" title="Edit">✎</button>
      <button onclick="deleteCard(this)" title="Delete">×</button>
    </div>

    <div class="tag">
      ${label} · Lab ${String(number).padStart(2,"0")}
    </div>

    <h3 class="editable" contenteditable="true">
      New ${label} Task
    </h3>

    <p class="editable" contenteditable="true">
      Add a short summary of the activity, process, or skills practiced.
    </p>

    <span class="placeholder editable" contenteditable="true">
      [ Add task link / image ]
    </span>
  `;

  container.appendChild(card);
  saveAll();

  card.scrollIntoView({
    behavior: "smooth",
    block: "center"
  });
}

/* LOAD SAVED PORTFOLIO */
restore();
</script>

</body>
</html>
