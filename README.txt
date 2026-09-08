<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<title>DESIRE / 3020</title>
<style>
@import url('https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@400;500;600&family=DM+Mono:wght@300;400&family=Playfair+Display:ital,wght@0,400;0,500;1,400&display=swap');

:root{
  --ink:#242027;--muted:#756d77;--paper:#f5f0eb;--line:#ddd2d0;
  --card:#faf7f4;--night:#211d26;
}
*{box-sizing:border-box}
html{scroll-behavior:smooth}
body{margin:0;background:var(--paper);color:var(--ink);font-family:'Playfair Display',serif}
body:before{
  content:"";position:fixed;inset:0;pointer-events:none;opacity:.07;
  background-image:url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='160' height='160'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='.8' numOctaves='3'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)'/%3E%3C/svg%3E");
  z-index:50;
}
header{
  position:fixed;z-index:60;top:0;left:0;right:0;padding:22px 6vw;
  display:flex;justify-content:space-between;background:linear-gradient(var(--paper),transparent);
}
.logo{font:600 18px 'Cormorant Garamond';letter-spacing:.14em}
.nav{display:flex;gap:20px}
.nav a{font:9px 'DM Mono';letter-spacing:.1em;color:inherit;text-decoration:none;opacity:.7}

.hero{
  min-height:100vh;display:grid;place-items:center;text-align:center;
  padding:100px 7vw;position:relative;
}
.eyebrow{font:10px 'DM Mono';letter-spacing:.24em;color:var(--muted)}
h1{
  font:400 clamp(62px,13vw,155px) 'Cormorant Garamond';
  line-height:.72;letter-spacing:-.06em;margin:32px 0;
}
.hero h1 span{
  display:block;font:italic 400 clamp(21px,3vw,34px) 'Playfair Display';
  letter-spacing:0;line-height:1.3;margin-top:28px;
}
.hero p{font-size:19px;line-height:1.8;font-style:italic;color:#514952}
.open{
  display:inline-block;margin-top:30px;color:inherit;text-decoration:none;
  font:10px 'DM Mono';letter-spacing:.15em;border-bottom:1px solid;padding-bottom:7px;
}
.risk{position:absolute;bottom:28px;font:9px 'DM Mono';letter-spacing:.12em;color:var(--muted)}

section{max-width:1200px;margin:auto;padding:100px 7vw}
.head{
  display:flex;justify-content:space-between;align-items:end;border-bottom:1px solid var(--line);
  padding-bottom:14px;margin-bottom:35px;
}
.head h2{margin:0;font:500 clamp(38px,5vw,60px) 'Cormorant Garamond'}
.head span{font:9px 'DM Mono';color:var(--muted)}

.chick-title{display:flex;align-items:center;gap:16px}
.chick{
  width:54px;height:54px;display:block;overflow:visible;
}
.chick img{
  width:100%;height:100%;object-fit:contain;display:block;
}

.grid{display:grid;grid-template-columns:1fr 1fr;gap:22px}
.card{
  background:var(--card);border:1px solid var(--line);padding:30px;
  min-height:255px;transition:.3s;display:flex;flex-direction:column;
}
.card:hover{transform:translateY(-5px);box-shadow:0 14px 30px #51495212}
.card .icon{
  width:28px;height:28px;margin-bottom:20px;font:10px 'DM Mono';color:var(--muted);
  display:flex;align-items:center;
}
.code{font:9px 'DM Mono';letter-spacing:.14em;color:var(--muted)}
.card h3{font:500 31px 'Cormorant Garamond';margin:16px 0 10px}
.card p{font-size:16px;line-height:1.8;color:#554e55}
.read{
  margin-top:auto;align-self:flex-start;font:9px 'DM Mono';letter-spacing:.1em;
  color:inherit;text-decoration:none;border-bottom:1px solid;padding-bottom:4px;cursor:pointer;
}
.empty-card{
  justify-content:center;align-items:center;text-align:center;min-height:230px;
  background:rgba(250,247,244,.45);
}
.empty-card .entry-mark{font:10px 'DM Mono';letter-spacing:.16em;color:var(--muted);margin-bottom:12px}
.empty-card .coming{font:italic 25px 'Cormorant Garamond';color:#514952}
.empty-card .tiny{font:9px 'DM Mono';letter-spacing:.1em;color:var(--muted);margin-top:10px}

.voice{background:#eee8e4;max-width:none}
.voice-grid{max-width:1050px;margin:auto;display:grid;grid-template-columns:1fr 1fr;gap:24px}
.voice-card{background:var(--card);border:1px solid var(--line);padding:32px}
.voice-card h3{font:500 35px 'Cormorant Garamond';margin:14px 0}
.voice-card p{font-size:17px;line-height:1.85;font-style:italic}
.wave{height:30px;display:flex;align-items:center;gap:3px}
.wave i{width:2px;background:#777;height:var(--h);display:block;border-radius:2px}

.dark{max-width:none;background:var(--night);color:#eee8e4;padding-left:12vw;padding-right:12vw}
.dark .head{border-color:#4b444d}
.dark .head span{color:#aaa1aa}
.poem{max-width:720px;text-align:center;margin:45px auto}
.poem h3{font:400 43px 'Cormorant Garamond'}
.poem p{font-size:20px;line-height:2;font-style:italic;color:#d8d0d0}

.feeling{max-width:850px}
.intro{text-align:center;margin-bottom:40px}
.intro h2{font:500 48px 'Cormorant Garamond';margin:0}
.intro p{color:var(--muted);line-height:1.7}
.form,.secretbox{background:var(--card);border:1px solid var(--line);padding:30px}
.row{display:grid;grid-template-columns:1fr 1fr;gap:18px}
.field{margin-bottom:18px}
.field label{display:block;font:9px 'DM Mono';letter-spacing:.12em;color:var(--muted);margin-bottom:8px}
.field input,.field textarea{
  width:100%;border:0;border-bottom:1px solid var(--line);background:transparent;
  padding:10px 2px;outline:0;font:16px 'Playfair Display';
}
.field textarea{min-height:120px;resize:vertical}
.button{
  background:transparent;border:1px solid var(--ink);padding:12px 18px;
  font:9px 'DM Mono';letter-spacing:.12em;cursor:pointer;
}
.status{min-height:18px;margin-top:12px;font:12px 'Playfair Display';font-style:italic;color:var(--muted)}

.secret{max-width:none;background:#e8e0e5}
.secret-inner{max-width:800px;margin:auto;text-align:center}
.secret h2{font:500 53px 'Cormorant Garamond';margin:0}
.secret p{font-size:17px;line-height:1.7}
.secretbox{text-align:left;margin-top:30px}
.privacy{font:9px 'DM Mono';line-height:1.7;color:var(--muted);margin-top:16px}

footer{text-align:center;padding:80px 20px 105px;font:9px 'DM Mono';letter-spacing:.1em;color:var(--muted)}
footer b{display:block;font:25px 'Cormorant Garamond';color:var(--ink);margin-bottom:10px}

/* Reader template for multi-part entries */
.reader{
  display:none;position:fixed;inset:0;z-index:100;
  background:rgba(33,29,38,.96);overflow:auto;padding:70px 6vw;
}
.reader.opened{display:block}
.reader-inner{max-width:820px;margin:auto;color:#eee8e4}
.reader-top{display:flex;justify-content:space-between;align-items:center;margin-bottom:50px}
.reader-code{font:9px 'DM Mono';letter-spacing:.15em;color:#aaa1aa}
.close{
  color:#eee8e4;background:none;border:0;font:9px 'DM Mono';letter-spacing:.12em;
  cursor:pointer;border-bottom:1px solid #aaa1aa;padding-bottom:5px;
}
.reader-part{padding:45px 0;border-bottom:1px solid #4b444d}
.reader-part:last-child{border-bottom:0}
.part-label{font:9px 'DM Mono';letter-spacing:.18em;color:#aaa1aa;margin-bottom:18px}
.reader-part h3{font:500 43px 'Cormorant Garamond';margin:0 0 12px}
.reader-part h4{font:italic 400 20px 'Playfair Display';margin:0 0 28px;color:#d8d0d0}
.reader-part p{font:19px 'Playfair Display';line-height:2;color:#eee8e4;white-space:pre-line}
.quote{
  margin:30px 0;padding-left:22px;border-left:1px solid #8e828e;
  font:italic 24px 'Cormorant Garamond';line-height:1.6;color:#d8d0d0;
}
.release-note{
  text-align:center;padding:35px 0;font:9px 'DM Mono';letter-spacing:.1em;color:#aaa1aa;
}

@media(max-width:700px){
  .nav{gap:9px}.nav a{font-size:7px}
  .grid,.voice-grid,.row{grid-template-columns:1fr}
  .hero h1{font-size:85px}.hero p br{display:none}
  section{padding-top:75px;padding-bottom:75px}
  .dark{padding-left:7vw;padding-right:7vw}
  .head{gap:15px}.head span{display:none}
  .chick{width:48px;height:48px}
  .reader{padding:50px 7vw}
  .reader-part h3{font-size:37px}
  .reader-part p{font-size:17px}
}
</style>
</head>
<body>

<header>
  <div class="logo">DESIRE / 3020</div>
  <nav class="nav">
    <a href="#chicks">CHICKS</a>
    <a href="#whispers">WHISPERS</a>
    <a href="#glimpses">GLIMPSES</a>
    <a href="#secret">SECRET</a>
  </nav>
</header>

<main>
<section class="hero">
  <div>
    <div class="eyebrow">between the love</div>
    <h1>DESIRE / 3020<span>stay, if your heart allows.</span></h1>
    <p>an archive of thoughts, memories, strange little feelings,<br>and things that were never meant to be said out loud.</p>
    <a class="open" href="#chicks">open the archive</a>
  </div>
  <div class="risk">if you stay, read gently.</div>
</section>

<section id="chicks">
  <div class="head">
    <div class="chick-title">
      <span class="chick"><img src="chick-mono.png" alt="minimal line-drawn chick"></span>
      <h2>chicks.</h2>
    </div>
    <span>pieces from somewhere between then & now</span>
  </div>

  <div class="grid">
    <!-- ENTRY 01 -->
    <article class="card">
      <div class="code">FSJAD-K-0307 · ENTRY / 01</div>
      <h3>Curse to Ruin things</h3>
      <p>Today, a conversation turned into an argument. And somehow, somewhere between the words we threw at each other, I watched you cry because of me...</p>
      <a class="read" onclick="openEntry01()">read entry →</a>
    </article>

    <article class="card empty-card">
      <div class="entry-mark">ENTRY / 02</div>
      <div class="coming">not written yet.</div>
      <div class="tiny">reserved for a future release</div>
    </article>
    <article class="card empty-card">
      <div class="entry-mark">ENTRY / 03</div>
      <div class="coming">still folded away.</div>
      <div class="tiny">reserved for a future release</div>
    </article>
    <article class="card empty-card">
      <div class="entry-mark">ENTRY / 04</div>
      <div class="coming">leave this one unopened.</div>
      <div class="tiny">reserved for a future release</div>
    </article>
  </div>
</section>

<section id="whispers" class="voice">
  <div class="head"><h2>whispers of arrogance.</h2><span>unfiltered / transcribed</span></div>
  <div class="voice-grid">
    <article class="voice-card">
      <div class="code">3020 / V-04</div>
      <div class="wave"><i style="--h:8px"></i><i style="--h:18px"></i><i style="--h:27px"></i><i style="--h:12px"></i><i style="--h:29px"></i><i style="--h:20px"></i><i style="--h:9px"></i><i style="--h:23px"></i><i style="--h:31px"></i><i style="--h:15px"></i><i style="--h:25px"></i><i style="--h:11px"></i></div>
      <h3>your words will live here.</h3>
      <p>Voice-note transcriptions, unfinished thoughts, things said too honestly — whenever you're ready to send them.</p>
    </article>
    <article class="voice-card">
      <div class="code">3020 / V-11</div>
      <div class="wave"><i style="--h:18px"></i><i style="--h:10px"></i><i style="--h:25px"></i><i style="--h:31px"></i><i style="--h:14px"></i><i style="--h:22px"></i><i style="--h:8px"></i><i style="--h:28px"></i><i style="--h:17px"></i><i style="--h:30px"></i><i style="--h:12px"></i><i style="--h:21px"></i></div>
      <h3>another voice, another night.</h3>
      <p>This is only a shell for now. The real words will replace it when you send them.</p>
    </article>
  </div>
</section>

<section id="glimpses" class="dark">
  <div class="head"><h2>glimpses of elsewhere.</h2><span>strange / beautiful / unnecessary</span></div>
  <div class="poem">
    <h3>this room is still waiting.</h3>
    <p>Some things will arrive here without announcement.<br><br>A line. A page. A thought that stayed too long.<br><br>Nothing needs to be finished before it belongs.</p>
  </div>
</section>

<section id="feeling" class="feeling">
  <div class="intro">
    <h2>before you leave.</h2>
    <p>You don't have to tell me who you are. I just want to know what a piece of this little archive made you feel.</p>
  </div>
  <form class="form" id="feelForm">
    <div class="row">
      <div class="field"><label>FIRST NAME (OPTIONAL)</label><input id="name" maxlength="40" placeholder="a name, if you'd like"></div>
      <div class="field"><label>INITIAL (OPTIONAL)</label><input id="initial" maxlength="3" placeholder="♡"></div>
    </div>
    <div class="field"><label>WHAT DID YOU FEEL?</label><textarea id="feelingText" required maxlength="800" placeholder="leave a little piece of your thought here..."></textarea></div>
    <button class="button">LEAVE THIS BEHIND ♡</button>
    <div class="status" id="feelStatus"></div>
  </form>
</section>

<section id="secret" class="secret">
  <div class="secret-inner">
    <div style="font-size:22px">⌁</div>
    <h2>the secret room.</h2>
    <p>You can tell me something you've never told anyone.<br>No name. No identity. Just the secret.</p>
    <form class="secretbox" id="secretForm">
      <div class="field"><label>YOUR SECRET</label><textarea id="secretText" required maxlength="1500" placeholder="write it here, anonymously..."></textarea></div>
      <button class="button">LOCK IT AWAY</button>
      <div class="status" id="secretStatus"></div>
      <div class="privacy">This preview does not send submissions to a server. Before publishing, the secret room should be connected to a properly secured encryption/backend architecture.</div>
    </form>
  </div>
</section>
</main>

<footer>
  <b>DESIRE / 3020</b>
  between the love · stay, if your heart allows.<br><br>
  an archive, not a timeline.
</footer>

<!-- Multi-part reader popup -->
<div class="reader" id="reader">
  <div class="reader-inner">
    <div class="reader-top">
      <div class="reader-code" id="readerCode"></div>
      <button class="close" onclick="closeReader()">CLOSE ×</button>
    </div>
    <div id="readerContent"></div>
  </div>
</div>

<script>
const feelForm = document.getElementById('feelForm');
feelForm.onsubmit = e => {
  e.preventDefault();
  document.getElementById('feelStatus').textContent =
    'thank you. your note was saved only on this device in this preview.';
  localStorage.setItem('desire_feedback', document.getElementById('feelingText').value);
  e.target.reset();
};

document.getElementById('secretForm').onsubmit = e => {
  e.preventDefault();
  document.getElementById('secretStatus').textContent =
    'sealed for this preview — nothing was sent anywhere.';
  e.target.reset();
};

const entry01Parts = [
  {
    heading: "Curse to Ruin things",
    subheading: "Today, a conversation turned into an argument.",
    body: `And somehow, somewhere between the words we threw at each other, I watched you cry because of me.
I heard it through the phone.

idk why i m writing this.
Maybe because I can’t sleep.
Maybe because my mind keeps replaying your voice.
Or maybe because every time I close my eyes, I hear you crying again.
And I don’t know how to forgive myself for being the reason behind those tears.

Tonight, I hurt you.

I know I did.

And there are some things you can apologize for a hundred times and still feel like the apology isn’t big enough.

This is one of them.

I wish I could go back to that conversation.
Not to prove that I was right.
Not to explain my side.
Not to make you understand me.

Just to hold the moment still before everything became ugly and tell myself:
“Don’t say it. She’s already hurting.”

But I didn’t.
I made mistakes.
You made mistakes too.
We both know that.
It wasn’t entirely me.
It wasn’t entirely you.
Maybe that’s what makes this hurt even more.
Because somewhere between two people who cared about each other, we both became careless with each other’s hearts.

And then you cried.
And I heard every bit of it.

I wish I hadn’t.
Not because I don’t want to know how you feel.
But because now I know what my words sound like when they reach someone I love.
They sound like pain.`,
    quote: "And I never wanted my voice to become something you were afraid of."
  }
];

function openEntry01(){
  openReader("DESIRE / 3020 · FSJAD-K-0307", entry01Parts);
}

function openReader(code, parts){
  document.getElementById('readerCode').textContent = code;
  document.getElementById('readerContent').innerHTML = parts.map((part, i) => `
    <article class="reader-part">
      <div class="part-label">PART ${String(i+1).padStart(2,'0')}</div>
      ${part.heading ? `<h3>${part.heading}</h3>` : ''}
      ${part.subheading ? `<h4>${part.subheading}</h4>` : ''}
      ${part.body ? `<p>${part.body}</p>` : ''}
      ${part.quote ? `<div class="quote">“${part.quote}”</div>` : ''}
    </article>
  `).join('') + '<div class="release-note">more will appear here when the next part is released.</div>';
  document.getElementById('reader').classList.add('opened');
  document.body.style.overflow = 'hidden';
}

function closeReader(){
  document.getElementById('reader').classList.remove('opened');
  document.body.style.overflow = '';
}
</script>
</body>
</html>
