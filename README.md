# Mexqrvr-is-the-best-youtuber
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>MexQRVR — VR Creator File</title>
<meta name="description" content="Unofficial fan page for MexQRVR — UG and Zombonk VR content creator.">
<link rel="icon" href="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'%3E%3Ctext y='.9em' font-size='90'%3E%F0%9F%A6%96%3C/text%3E%3C/svg%3E">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Bricolage+Grotesque:opsz,wght@12..96,400;12..96,600;12..96,700;12..96,800&family=Plus+Jakarta+Sans:wght@400;500;600;700&family=JetBrains+Mono:wght@400;500;700&display=swap" rel="stylesheet">
<style>
  :root{
    --bg:#17120e;
    --surface:#241c15;
    --surface-2:#2c2219;
    --amber:#e8a23d;
    --amber-bright:#f6c56a;
    --moss:#8ca85e;
    --bonk:#ff6152;
    --bone:#f3eadd;
    --bone-dim:#c9beac;
    --line: rgba(243,234,221,0.12);
    --radius: 18px;
    --maxw: 1080px;
  }

  *{ box-sizing:border-box; }
  html{ scroll-behavior:smooth; }

  body{
    margin:0;
    background:var(--bg);
    color:var(--bone);
    font-family:'Plus Jakarta Sans', sans-serif;
    line-height:1.55;
    -webkit-font-smoothing:antialiased;
    overflow-x:hidden;
  }

  h1,h2,h3{
    font-family:'Bricolage Grotesque', sans-serif;
    line-height:1.05;
    margin:0;
  }

  a{ color:inherit; text-decoration:none; }

  :focus-visible{
    outline: 2px solid var(--amber-bright);
    outline-offset: 3px;
  }

  .wrap{
    max-width:var(--maxw);
    margin:0 auto;
    padding:0 24px;
  }

  .mono{
    font-family:'JetBrains Mono', monospace;
  }

  .eyebrow{
    display:inline-flex;
    align-items:center;
    gap:8px;
    font-family:'JetBrains Mono', monospace;
    font-size:12.5px;
    letter-spacing:0.14em;
    text-transform:uppercase;
    color:var(--amber-bright);
    background:rgba(232,162,61,0.1);
    border:1px solid rgba(232,162,61,0.35);
    padding:6px 14px;
    border-radius:999px;
  }

  /* texture: faint fossil-crack grain, very subtle */
  .grain{
    position:fixed;
    inset:0;
    pointer-events:none;
    z-index:1;
    opacity:0.5;
    background-image:
      radial-gradient(circle at 20% 30%, rgba(243,234,221,0.025) 0, transparent 40%),
      radial-gradient(circle at 80% 10%, rgba(232,162,61,0.03) 0, transparent 45%),
      radial-gradient(circle at 60% 80%, rgba(140,168,94,0.03) 0, transparent 40%);
  }

  /* ---------- NAV ---------- */
  .nav{
    position:sticky;
    top:0;
    z-index:50;
    background:rgba(23,18,14,0.82);
    backdrop-filter:blur(10px);
    border-bottom:1px solid var(--line);
  }
  .nav-inner{
    display:flex;
    align-items:center;
    justify-content:space-between;
    padding:16px 24px;
    max-width:var(--maxw);
    margin:0 auto;
  }
  .logo{
    font-family:'Bricolage Grotesque', sans-serif;
    font-weight:800;
    font-size:19px;
    letter-spacing:-0.01em;
  }
  .logo span{ color:var(--amber-bright); }
  .nav-links{
    display:flex;
    gap:28px;
    font-size:14.5px;
    color:var(--bone-dim);
  }
  .nav-links a:hover{ color:var(--bone); }
  .btn{
    display:inline-flex;
    align-items:center;
    justify-content:center;
    gap:8px;
    font-family:'Plus Jakarta Sans', sans-serif;
    font-weight:700;
    font-size:14.5px;
    padding:12px 22px;
    border-radius:12px;
    border:1px solid transparent;
    cursor:pointer;
    transition:transform 0.18s ease, box-shadow 0.18s ease, background 0.18s ease;
  }
  .btn-primary{
    background:linear-gradient(180deg, var(--amber-bright), var(--amber));
    color:#231705;
    box-shadow:0 8px 22px rgba(232,162,61,0.25);
  }
  .btn-primary:hover{ transform:translateY(-2px); box-shadow:0 12px 28px rgba(232,162,61,0.35); }
  .btn-ghost{
    background:transparent;
    color:var(--bone);
    border-color:var(--line);
  }
  .btn-ghost:hover{ border-color:var(--amber); color:var(--amber-bright); }
  .btn-small{ padding:9px 16px; font-size:13.5px; }

  /* ---------- HERO ---------- */
  .hero{
    position:relative;
    padding:80px 24px 60px;
    max-width:var(--maxw);
    margin:0 auto;
    display:grid;
    grid-template-columns:1.1fr 0.9fr;
    gap:56px;
    align-items:center;
  }
  .hero-glow{
    position:absolute;
    top:-10%;
    right:-10%;
    width:600px;
    height:600px;
    background:radial-gradient(circle, rgba(232,162,61,0.16), transparent 65%);
    filter:blur(10px);
    z-index:0;
    pointer-events:none;
  }
  .hero-copy{ position:relative; z-index:2; }
  .hero h1{
    font-size:clamp(34px, 5.4vw, 54px);
    font-weight:800;
    margin:18px 0 16px;
    letter-spacing:-0.01em;
  }
  .hero h1 em{
    font-style:normal;
    color:var(--amber-bright);
  }
  .hero p.sub{
    font-size:clamp(15px,1.7vw,17.5px);
    color:var(--bone-dim);
    max-width:46ch;
    margin:0 0 28px;
  }
  .hero-actions{ display:flex; gap:14px; flex-wrap:wrap; }

  /* ---------- CREATOR CARD (signature element) ---------- */
  .card-stage{
    position:relative;
    z-index:2;
    display:flex;
    justify-content:center;
  }
  .creator-card{
    width:100%;
    max-width:320px;
    background:linear-gradient(155deg, var(--surface-2), var(--surface));
    border:1px solid rgba(232,162,61,0.3);
    border-radius:22px;
    padding:26px;
    box-shadow:0 30px 60px rgba(0,0,0,0.45), 0 0 0 1px rgba(243,234,221,0.03) inset;
    transform:rotate(-4deg);
    opacity:0;
    animation:dealIn 0.9s cubic-bezier(.16,.9,.35,1.05) 0.15s forwards;
  }
  @keyframes dealIn{
    0%{ opacity:0; transform:rotate(-14deg) translateY(40px) scale(0.9); }
    100%{ opacity:1; transform:rotate(-4deg) translateY(0) scale(1); }
  }
  .creator-card:hover{
    transform:rotate(-1deg) translateY(-4px);
    transition:transform 0.35s ease;
  }
  .card-top{
    display:flex;
    justify-content:space-between;
    align-items:flex-start;
    margin-bottom:18px;
  }
  .card-rank{
    font-family:'JetBrains Mono', monospace;
    font-size:11.5px;
    letter-spacing:0.08em;
    color:var(--amber-bright);
    background:rgba(232,162,61,0.12);
    border:1px solid rgba(232,162,61,0.4);
    padding:4px 10px;
    border-radius:8px;
  }
  .card-name{
    font-family:'Bricolage Grotesque', sans-serif;
    font-weight:800;
    font-size:26px;
    margin:14px 0 2px;
  }
  .card-role{
    font-size:13px;
    color:var(--bone-dim);
    margin-bottom:18px;
  }
  .card-divider{
    height:1px;
    background:var(--line);
    margin:16px 0;
  }
  .card-games{
    display:flex;
    gap:10px;
    margin-bottom:16px;
  }
  .game-chip{
    flex:1;
    background:rgba(243,234,221,0.04);
    border:1px solid var(--line);
    border-radius:10px;
    padding:10px;
    text-align:center;
    font-size:12.5px;
  }
  .game-chip .emoji{ font-size:20px; display:block; margin-bottom:4px; }
  .card-code{
    font-family:'JetBrains Mono', monospace;
    font-size:12px;
    color:var(--bone-dim);
    display:flex;
    justify-content:space-between;
  }
  .card-code b{ color:var(--bone); letter-spacing:0.05em; }

  /* ---------- SECTION shell ---------- */
  .section{
    padding:90px 24px;
    max-width:var(--maxw);
    margin:0 auto;
  }
  .section-head{
    max-width:640px;
    margin:0 0 44px;
  }
  .section-head h2{
    font-size:clamp(26px,3.6vw,36px);
    font-weight:800;
    margin-top:12px;
  }
  .section-head p{
    color:var(--bone-dim);
    font-size:15.5px;
    margin-top:12px;
  }

  /* ---------- WORLDS ---------- */
  .worlds-grid{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:20px;
  }
  .world-card{
    border-radius:var(--radius);
    padding:28px;
    border:1px solid var(--line);
    position:relative;
    overflow:hidden;
  }
  .world-card.ug{
    background:linear-gradient(160deg, rgba(140,168,94,0.14), var(--surface));
  }
  .world-card.zombonk{
    background:linear-gradient(160deg, rgba(255,97,82,0.14), var(--surface));
  }
  .world-glyph{ font-size:34px; margin-bottom:14px; display:block; }
  .world-card h3{
    font-size:21px;
    font-weight:700;
    margin-bottom:10px;
  }
  .world-card p{
    font-size:14.5px;
    color:var(--bone-dim);
    margin:0 0 18px;
  }
  .world-tag{
    display:inline-block;
    font-family:'JetBrains Mono', monospace;
    font-size:11.5px;
    letter-spacing:0.06em;
    padding:5px 10px;
    border-radius:7px;
    border:1px solid var(--line);
    color:var(--bone-dim);
  }

  /* ---------- PATCH NOTES ---------- */
  .patch-panel{
    background:var(--surface);
    border:1px solid var(--line);
    border-radius:var(--radius);
    overflow:hidden;
  }
  .patch-header{
    display:flex;
    justify-content:space-between;
    align-items:center;
    padding:16px 22px;
    border-bottom:1px solid var(--line);
    font-family:'JetBrains Mono', monospace;
    font-size:12.5px;
    color:var(--bone-dim);
    letter-spacing:0.05em;
  }
  .patch-list{
    list-style:none;
    margin:0;
    padding:6px 0;
  }
  .patch-list li{
    display:grid;
    grid-template-columns:120px 1fr;
    gap:16px;
    padding:16px 22px;
    border-bottom:1px solid var(--line);
    font-size:14.5px;
  }
  .patch-list li:last-child{ border-bottom:none; }
  .patch-tag{
    font-family:'JetBrains Mono', monospace;
    font-size:12px;
    font-weight:700;
    letter-spacing:0.04em;
    height:fit-content;
  }
  .tag-added{ color:var(--moss); }
  .tag-buffed{ color:var(--amber-bright); }
  .tag-fixed{ color:var(--bonk); }
  .patch-list p{ margin:0; color:var(--bone-dim); }
  .patch-list b{ color:var(--bone); font-weight:600; }

  /* ---------- RANK PROGRESS ---------- */
  .rank-box{
    background:var(--surface);
    border:1px solid var(--line);
    border-radius:var(--radius);
    padding:30px 28px;
  }
  .rank-top{
    display:flex;
    justify-content:space-between;
    align-items:baseline;
    margin-bottom:14px;
    flex-wrap:wrap;
    gap:8px;
  }
  .rank-top .label{
    font-family:'JetBrains Mono', monospace;
    font-size:12.5px;
    letter-spacing:0.06em;
    color:var(--bone-dim);
  }
  .rank-top .target{
    font-family:'Bricolage Grotesque', sans-serif;
    font-weight:800;
    font-size:22px;
    color:var(--amber-bright);
  }
  .xp-track{
    height:14px;
    border-radius:999px;
    background:rgba(243,234,221,0.06);
    border:1px solid var(--line);
    overflow:hidden;
    position:relative;
  }
  .xp-fill{
    height:100%;
    width:0%;
    border-radius:999px;
    background:linear-gradient(90deg, var(--moss), var(--amber-bright));
    box-shadow:0 0 18px rgba(232,162,61,0.5);
    transition:width 1.4s cubic-bezier(.16,.8,.3,1);
  }
  .rank-caption{
    margin-top:14px;
    font-size:14px;
    color:var(--bone-dim);
  }

  /* ---------- FAN CODE ---------- */
  .code-box{
    display:flex;
    justify-content:space-between;
    align-items:center;
    gap:20px;
    background:linear-gradient(160deg, rgba(232,162,61,0.1), var(--surface));
    border:1px dashed rgba(232,162,61,0.4);
    border-radius:var(--radius);
    padding:26px 28px;
    flex-wrap:wrap;
  }
  .code-box .code-label{
    font-family:'JetBrains Mono', monospace;
    font-size:12px;
    color:var(--bone-dim);
    letter-spacing:0.06em;
    margin-bottom:6px;
  }
  .code-box .code-value{
    font-family:'JetBrains Mono', monospace;
    font-size:28px;
    font-weight:700;
    color:var(--amber-bright);
    letter-spacing:0.05em;
  }
  .copy-btn{
    font-family:'JetBrains Mono', monospace;
    font-size:13px;
    font-weight:700;
    background:transparent;
    color:var(--bone);
    border:1px solid var(--line);
    padding:10px 18px;
    border-radius:10px;
    cursor:pointer;
    transition:all 0.15s ease;
  }
  .copy-btn:hover{ border-color:var(--amber); color:var(--amber-bright); }

  /* ---------- CTA ---------- */
  .cta{
    text-align:center;
    padding:100px 24px;
  }
  .cta h2{
    font-size:clamp(28px,4vw,42px);
    font-weight:800;
    max-width:640px;
    margin:0 auto 14px;
  }
  .cta p{ color:var(--bone-dim); margin-bottom:28px; }
  .cta-actions{ display:flex; justify-content:center; gap:14px; flex-wrap:wrap; }

  footer{
    border-top:1px solid var(--line);
    padding:28px 24px;
    text-align:center;
    font-size:13px;
    color:var(--bone-dim);
  }
  footer a{ color:var(--amber-bright); }

  /* reveal-on-scroll */
  .reveal{
    opacity:0;
    transform:translateY(22px);
    transition:opacity 0.7s ease, transform 0.7s ease;
  }
  .reveal.in{
    opacity:1;
    transform:translateY(0);
  }

  @media (prefers-reduced-motion: reduce){
    .creator-card{ animation:none; opacity:1; transform:rotate(-4deg); }
    .reveal{ opacity:1; transform:none; transition:none; }
    .xp-fill{ transition:none; }
  }

  @media (max-width: 860px){
    .hero{ grid-template-columns:1fr; padding-top:52px; gap:40px; }
    .worlds-grid{ grid-template-columns:1fr; }
    .nav-links{ display:none; }
    .patch-list li{ grid-template-columns:1fr; gap:6px; }
    .code-box{ justify-content:flex-start; }
  }
</style>
</head>
<body>

<div class="grain"></div>

<header class="nav">
  <div class="nav-inner">
    <a href="#top" class="logo">Mex<span>QRVR</span></a>
    <nav class="nav-links">
      <a href="#worlds">Worlds</a>
      <a href="#patchnotes">Patch Notes</a>
      <a href="#rank">Rank</a>
    </nav>
    <a href="https://www.youtube.com/@Mexqrvr" target="_blank" rel="noopener" class="btn btn-primary btn-small">Subscribe</a>
  </div>
</header>

<section class="hero" id="top">
  <div class="hero-glow"></div>
  <div class="hero-copy">
    <span class="eyebrow reveal in">VR CREATOR FILE — UG 🦖 · ZOMBONK 🧟</span>
    <h1 class="reveal in">MexQRVR is just <em>built different.</em></h1>
    <p class="sub reveal in">Every UG hatch and every Zombonk loot run turns into the funniest fifteen minutes on your feed. Nearly 50K people already hit subscribe — you're a little late, but you're right on time.</p>
    <div class="hero-actions reveal in">
      <a href="https://www.youtube.com/@Mexqrvr" target="_blank" rel="noopener" class="btn btn-primary">▶ Subscribe on YouTube</a>
      <a href="#patchnotes" class="btn btn-ghost">See why ↓</a>
    </div>
  </div>
  <div class="card-stage">
    <div class="creator-card">
      <div class="card-top">
        <div>
          <div class="card-name">MexQRVR</div>
          <div class="card-role">VR Content Creator</div>
        </div>
        <span class="card-rank">LV.5 · FIRESTARTER 🔥</span>
      </div>
      <div class="card-games">
        <div class="game-chip"><span class="emoji">🦖</span>UG</div>
        <div class="game-chip"><span class="emoji">🧟</span>Zombonk</div>
      </div>
      <div class="card-divider"></div>
      <div class="card-code">
        <span>FAN CODE</span>
        <b>49325</b>
      </div>
    </div>
  </div>
</section>

<section class="section" id="worlds">
  <div class="section-head reveal">
    <span class="eyebrow">The worlds he plays in</span>
    <h2>Two games. Zero downtime.</h2>
    <p>MexQRVR splits his content between a prehistoric sandbox and a full-blown zombie apocalypse — and somehow makes both feel like the main event.</p>
  </div>
  <div class="worlds-grid">
    <div class="world-card ug reveal">
      <span class="world-glyph">🦖</span>
      <h3>UG</h3>
      <p>A free-to-play social VR game where players hatch, raise, ride, and trade dinosaurs across a prehistoric world — climbing, exploring, and fighting alongside friends in classic chaotic-UG fashion.</p>
      <span class="world-tag">MAIN GAME</span>
    </div>
    <div class="world-card zombonk reveal">
      <span class="world-glyph">🧟</span>
      <h3>Zombonk</h3>
      <p>A looter-shooter survival game where players explore, crack open loot, and fight through zombie-infested maps — from Bonktopia City to the Temple — to stack up gear and cosmetics.</p>
      <span class="world-tag">SIDE QUEST</span>
    </div>
  </div>
</section>

<section class="section" id="patchnotes">
  <div class="section-head reveal">
    <span class="eyebrow">Why he's the best, patch-note style</span>
    <h2>v50.0 — Patch Notes</h2>
    <p>If MexQRVR's channel got an update log, it would read something like this.</p>
  </div>
  <div class="patch-panel reveal">
    <div class="patch-header">
      <span>CHANGELOG.md</span>
      <span>MEXQRVR // ONGOING</span>
    </div>
    <ul class="patch-list">
      <li>
        <span class="patch-tag tag-buffed">+ BUFFED</span>
        <p><b>Comedic timing.</b> Every clip lands — no dead air, no forced bits.</p>
      </li>
      <li>
        <span class="patch-tag tag-added">+ ADDED</span>
        <p><b>Actual UG and Zombonk skill,</b> not just chaos for clicks. The gameplay backs up the laughs.</p>
      </li>
      <li>
        <span class="patch-tag tag-fixed">+ FIXED</span>
        <p><b>The "boring VR channel" bug.</b> Never patched in, never will be.</p>
      </li>
      <li>
        <span class="patch-tag tag-buffed">+ IMPROVED</span>
        <p><b>Community vibes.</b> Everyone in the comments feels like part of the crew.</p>
      </li>
      <li>
        <span class="patch-tag tag-added">+ NEW</span>
        <p><b>Content on schedule.</b> Same energy, every single upload.</p>
      </li>
      <li>
        <span class="patch-tag tag-fixed">+ BALANCED</span>
        <p><b>Big energy, zero ego.</b> He still thanks everyone who hits subscribe.</p>
      </li>
    </ul>
  </div>
</section>

<section class="section" id="rank">
  <div class="section-head reveal">
    <span class="eyebrow">Current rank progress</span>
    <h2>Next unlock: 50,000 subscribers</h2>
  </div>
  <div class="rank-box reveal">
    <div class="rank-top">
      <span class="label">SUBSCRIBER XP</span>
      <span class="target">🔥 NEARLY THERE</span>
    </div>
    <div class="xp-track"><div class="xp-fill" data-fill="96"></div></div>
    <p class="rank-caption">So close to the next milestone — every subscribe pushes the bar forward.</p>
  </div>
</section>

<section class="section">
  <div class="section-head reveal">
    <span class="eyebrow">Support the channel in-game</span>
    <h2>Drop his fan code</h2>
    <p>Use it in UG to show support while you play.</p>
  </div>
  <div class="code-box reveal">
    <div>
      <div class="code-label">MEXQRVR FAN CODE</div>
      <div class="code-value" id="fancode">49325</div>
    </div>
    <button class="copy-btn" onclick="copyCode()">Copy code</button>
  </div>
</section>

<section class="cta">
  <h2 class="reveal">Be there for the 50K moment.</h2>
  <p class="reveal">Subscribe, turn on notifications, and don't miss it.</p>
  <div class="cta-actions reveal">
    <a href="https://www.youtube.com/@Mexqrvr" target="_blank" rel="noopener" class="btn btn-primary">▶ Subscribe Now</a>
    <a href="https://www.tiktok.com/@tht_one_ugvr_editer" target="_blank" rel="noopener" class="btn btn-ghost">Also on TikTok</a>
  </div>
</section>

<footer>
  Unofficial fan page for MexQRVR. Not affiliated with UG, Zombonk, or Meta.
</footer>

<script>
  // scroll reveal
  const revealEls = document.querySelectorAll('.reveal');
  const io = new IntersectionObserver((entries) => {
    entries.forEach(e => {
      if (e.isIntersecting) {
        e.target.classList.add('in');
        io.unobserve(e.target);
      }
    });
  }, { threshold: 0.15 });
  revealEls.forEach(el => io.observe(el));

  // xp bar fill animates in when visible
  const xpFill = document.querySelector('.xp-fill');
  if (xpFill) {
    const xpIo = new IntersectionObserver((entries) => {
      entries.forEach(e => {
        if (e.isIntersecting) {
          xpFill.style.width = xpFill.dataset.fill + '%';
          xpIo.unobserve(e.target);
        }
      });
    }, { threshold: 0.3 });
    xpIo.observe(xpFill);
  }

  // copy fan code
  function copyCode(){
    const code = document.getElementById('fancode').innerText;
    navigator.clipboard.writeText(code).then(() => {
      const btn = document.querySelector('.copy-btn');
      const original = btn.innerText;
      btn.innerText = 'Copied!';
      setTimeout(() => btn.innerText = original, 1500);
    });
  }
</script>

</body>
</html>
