<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Anne-Xiety · A Mental Wellness Space</title>
<link href="https://fonts.googleapis.com/css2?family=Lora:ital,wght@0,400;0,500;1,400;1,500&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet"/>
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --lavender-50: #F5F2FF;
    --lavender-100: #EDE7FF;
    --lavender-200: #D9CFFE;
    --lavender-300: #C4B8F0;
    --lavender-400: #9B84DC;
    --lavender-500: #7B5EC4;
    --lavender-600: #5B4A9F;
    --lavender-700: #3A2D72;
    --lavender-800: #26215C;
    --mint: #E3F8EE;
    --mint-text: #2D7A55;
    --blush: #FFF0F5;
    --blush-text: #B5427A;
    --sky: #E7F3FF;
    --sky-text: #3A7CC7;
  }

  html { scroll-behavior: smooth; }

  body {
    font-family: 'DM Sans', sans-serif;
    background: var(--lavender-50);
    color: var(--lavender-700);
    line-height: 1.7;
  }

  /* ── NAV ── */
  nav {
    position: sticky;
    top: 0;
    z-index: 100;
    background: rgba(245,242,255,0.95);
    backdrop-filter: blur(12px);
    border-bottom: 0.5px solid var(--lavender-200);
    padding: 0 48px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    height: 64px;
  }

  .logo {
    font-family: 'Lora', serif;
    font-size: 22px;
    color: var(--lavender-600);
    text-decoration: none;
  }
  .logo em { font-style: italic; color: var(--lavender-400); }

  .nav-links {
    display: flex;
    gap: 32px;
    list-style: none;
  }
  .nav-links a {
    text-decoration: none;
    font-size: 13px;
    font-weight: 400;
    color: var(--lavender-400);
    letter-spacing: 0.3px;
    transition: color 0.2s;
  }
  .nav-links a:hover { color: var(--lavender-600); }

  .nav-cta {
    background: var(--lavender-100);
    color: var(--lavender-600) !important;
    padding: 8px 18px;
    border-radius: 50px;
    font-weight: 500 !important;
    transition: background 0.2s !important;
  }
  .nav-cta:hover { background: var(--lavender-200) !important; }

  /* ── HERO ── */
  .hero {
    display: grid;
    grid-template-columns: 1fr 1fr;
    min-height: 520px;
  }

  .hero-left {
    background: linear-gradient(140deg, #EDE7FF 0%, #D9CFFE 100%);
    padding: 72px 64px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    position: relative;
    overflow: hidden;
  }

  .hero-left::before {
    content: '';
    position: absolute;
    width: 320px;
    height: 320px;
    border-radius: 50%;
    background: rgba(155,132,220,0.15);
    bottom: -80px;
    left: -60px;
  }

  .eyebrow {
    font-size: 11px;
    letter-spacing: 2.5px;
    text-transform: uppercase;
    color: var(--lavender-400);
    font-weight: 500;
    margin-bottom: 18px;
  }

  .hero-title {
    font-family: 'Lora', serif;
    font-size: 44px;
    line-height: 1.2;
    font-weight: 400;
    color: var(--lavender-800);
    margin-bottom: 20px;
  }
  .hero-title em { font-style: italic; color: var(--lavender-500); }

  .hero-sub {
    font-size: 15px;
    line-height: 1.75;
    color: var(--lavender-600);
    font-weight: 300;
    max-width: 380px;
    margin-bottom: 36px;
  }

  .btn-primary {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    background: var(--lavender-600);
    color: #fff;
    padding: 13px 28px;
    border-radius: 50px;
    text-decoration: none;
    font-size: 14px;
    font-weight: 500;
    transition: background 0.2s, transform 0.2s;
    width: fit-content;
  }
  .btn-primary:hover { background: var(--lavender-700); transform: translateY(-1px); }

  .hero-right {
    background: var(--lavender-100);
    display: flex;
    align-items: center;
    justify-content: center;
    position: relative;
    overflow: hidden;
    padding: 40px;
  }

  .hero-circle-1 {
    position: absolute;
    width: 220px; height: 220px;
    border-radius: 50%;
    background: rgba(196,184,240,0.3);
    top: -50px; right: -50px;
  }
  .hero-circle-2 {
    position: absolute;
    width: 100px; height: 100px;
    border-radius: 50%;
    background: rgba(155,132,220,0.2);
    bottom: 30px; left: 30px;
  }

  .featured-card {
    background: #fff;
    border-radius: 24px;
    padding: 32px;
    max-width: 340px;
    box-shadow: 0 12px 48px rgba(90,60,180,0.12);
    position: relative;
    z-index: 2;
    animation: floatCard 4s ease-in-out infinite;
  }

  @keyframes floatCard {
    0%, 100% { transform: translateY(0); }
    50% { transform: translateY(-8px); }
  }

  .feat-tag {
    display: inline-block;
    background: var(--lavender-100);
    color: var(--lavender-500);
    font-size: 10px;
    font-weight: 500;
    letter-spacing: 1px;
    text-transform: uppercase;
    padding: 4px 12px;
    border-radius: 50px;
    margin-bottom: 14px;
  }

  .feat-title {
    font-family: 'Lora', serif;
    font-size: 19px;
    font-weight: 400;
    color: var(--lavender-800);
    line-height: 1.4;
    margin-bottom: 12px;
  }

  .feat-excerpt {
    font-size: 13px;
    color: var(--lavender-400);
    line-height: 1.65;
    font-weight: 300;
    margin-bottom: 18px;
  }

  .read-link {
    font-size: 13px;
    color: var(--lavender-500);
    font-weight: 500;
    text-decoration: none;
  }
  .read-link:hover { color: var(--lavender-700); }

  /* ── MISSION STRIP ── */
  .mission-strip {
    background: var(--lavender-700);
    padding: 48px 80px;
    text-align: center;
  }

  .mission-strip p {
    font-family: 'Lora', serif;
    font-size: 22px;
    font-style: italic;
    color: var(--lavender-300);
    line-height: 1.6;
    max-width: 680px;
    margin: 0 auto 12px;
  }

  .mission-strip span {
    font-size: 12px;
    color: var(--lavender-400);
    letter-spacing: 1px;
  }

  /* ── MAIN LAYOUT ── */
  .main-layout {
    display: grid;
    grid-template-columns: 1fr 320px;
    gap: 0;
    max-width: 1200px;
    margin: 0 auto;
    padding: 0;
  }

  /* ── ARTICLES ── */
  .articles-section {
    padding: 56px 48px;
    border-right: 0.5px solid var(--lavender-200);
  }

  .section-label {
    font-size: 10px;
    letter-spacing: 2.5px;
    text-transform: uppercase;
    color: var(--lavender-400);
    font-weight: 500;
    display: flex;
    align-items: center;
    gap: 12px;
    margin-bottom: 28px;
  }
  .section-label::after {
    content: '';
    flex: 1;
    height: 0.5px;
    background: var(--lavender-200);
  }

  .articles-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 18px;
    margin-bottom: 48px;
  }

  .article-card {
    background: #fff;
    border-radius: 18px;
    padding: 24px;
    border: 0.5px solid var(--lavender-200);
    cursor: pointer;
    transition: transform 0.25s, box-shadow 0.25s;
    text-decoration: none;
    display: block;
    color: inherit;
  }
  .article-card:hover {
    transform: translateY(-4px);
    box-shadow: 0 8px 32px rgba(91,74,159,0.1);
  }

  .card-tag {
    display: inline-block;
    font-size: 10px;
    font-weight: 500;
    letter-spacing: 0.8px;
    text-transform: uppercase;
    padding: 3px 10px;
    border-radius: 50px;
    margin-bottom: 12px;
  }
  .tag-anxiety { background: var(--lavender-100); color: var(--lavender-500); }
  .tag-education { background: var(--sky); color: var(--sky-text); }
  .tag-tools { background: var(--mint); color: var(--mint-text); }
  .tag-reflect { background: var(--blush); color: var(--blush-text); }

  .card-title {
    font-family: 'Lora', serif;
    font-size: 16px;
    font-weight: 400;
    color: var(--lavender-800);
    line-height: 1.45;
    margin-bottom: 10px;
  }

  .card-desc {
    font-size: 12.5px;
    color: var(--lavender-400);
    line-height: 1.65;
    font-weight: 300;
  }

  /* ── GROUNDING TOOLS SECTION ── */
  .tools-section {
    padding: 0 48px 56px;
  }

  .tools-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 14px;
  }

  .tool-card {
    background: var(--lavender-100);
    border-radius: 16px;
    padding: 22px 20px;
    border: 0.5px solid var(--lavender-200);
    transition: transform 0.2s;
    cursor: pointer;
  }
  .tool-card:hover { transform: translateY(-3px); }

  .tool-icon {
    font-size: 24px;
    margin-bottom: 10px;
  }

  .tool-title {
    font-family: 'Lora', serif;
    font-size: 14px;
    color: var(--lavender-700);
    margin-bottom: 6px;
    font-weight: 400;
  }

  .tool-desc {
    font-size: 12px;
    color: var(--lavender-500);
    line-height: 1.5;
    font-weight: 300;
  }

  /* ── SIDEBAR ── */
  .sidebar {
    padding: 56px 28px;
    background: #EFEBFF;
  }

  .sidebar-block {
    background: #fff;
    border-radius: 18px;
    padding: 22px;
    margin-bottom: 18px;
    border: 0.5px solid var(--lavender-200);
  }

  .sidebar-title {
    font-family: 'Lora', serif;
    font-size: 15px;
    color: var(--lavender-700);
    margin-bottom: 14px;
    font-weight: 400;
  }

  .tool-item {
    display: flex;
    align-items: center;
    gap: 10px;
    padding: 9px 0;
    border-bottom: 0.5px solid var(--lavender-100);
    font-size: 13px;
    color: var(--lavender-500);
    font-weight: 300;
    cursor: pointer;
    transition: color 0.2s;
  }
  .tool-item:last-child { border-bottom: none; }
  .tool-item:hover { color: var(--lavender-700); }

  .tool-dot {
    width: 7px; height: 7px;
    border-radius: 50%;
    background: var(--lavender-300);
    flex-shrink: 0;
  }

  .quote-block {
    background: linear-gradient(135deg, var(--lavender-100), var(--lavender-200));
    border-radius: 0 18px 18px 0;
    border-left: 3px solid var(--lavender-400);
    padding: 22px 20px;
    margin-bottom: 18px;
  }

  .quote-text {
    font-family: 'Lora', serif;
    font-size: 14px;
    font-style: italic;
    color: var(--lavender-600);
    line-height: 1.65;
    margin-bottom: 10px;
  }

  .quote-attr {
    font-size: 11px;
    color: var(--lavender-400);
    font-weight: 500;
    letter-spacing: 0.5px;
  }

  .disclaimer {
    font-size: 11px;
    color: var(--lavender-400);
    line-height: 1.65;
    text-align: center;
    font-weight: 300;
    padding: 0 4px;
  }

  /* ── REFLECTION BANNER ── */
  .reflect-banner {
    background: linear-gradient(135deg, var(--lavender-100) 0%, #fff 50%, var(--blush) 100%);
    border-top: 0.5px solid var(--lavender-200);
    border-bottom: 0.5px solid var(--lavender-200);
    padding: 56px 80px;
    text-align: center;
  }

  .reflect-banner h2 {
    font-family: 'Lora', serif;
    font-size: 32px;
    font-weight: 400;
    color: var(--lavender-800);
    margin-bottom: 12px;
  }
  .reflect-banner h2 em { font-style: italic; color: var(--lavender-500); }

  .reflect-banner p {
    font-size: 15px;
    color: var(--lavender-500);
    font-weight: 300;
    max-width: 520px;
    margin: 0 auto 28px;
  }

  .reflect-posts {
    display: flex;
    gap: 16px;
    justify-content: center;
    flex-wrap: wrap;
    margin-top: 32px;
  }

  .reflect-pill {
    background: #fff;
    border: 0.5px solid var(--lavender-200);
    border-radius: 50px;
    padding: 10px 22px;
    font-size: 13px;
    color: var(--lavender-600);
    cursor: pointer;
    transition: all 0.2s;
    font-weight: 300;
  }
  .reflect-pill:hover {
    background: var(--lavender-100);
    border-color: var(--lavender-400);
    color: var(--lavender-700);
  }

  /* ── FOOTER ── */
  footer {
    background: var(--lavender-800);
    padding: 48px 80px 28px;
  }

  .footer-grid {
    display: grid;
    grid-template-columns: 2fr 1fr 1fr 1fr;
    gap: 48px;
    margin-bottom: 40px;
  }

  .footer-brand .logo { color: var(--lavender-300); display: block; margin-bottom: 12px; }
  .footer-brand p {
    font-size: 13px;
    color: var(--lavender-400);
    font-weight: 300;
    line-height: 1.7;
    max-width: 240px;
  }

  .footer-col h4 {
    font-size: 11px;
    letter-spacing: 1.5px;
    text-transform: uppercase;
    color: var(--lavender-300);
    font-weight: 500;
    margin-bottom: 14px;
  }

  .footer-col ul { list-style: none; }
  .footer-col ul li { margin-bottom: 9px; }
  .footer-col ul li a {
    text-decoration: none;
    font-size: 13px;
    color: var(--lavender-400);
    font-weight: 300;
    transition: color 0.2s;
  }
  .footer-col ul li a:hover { color: var(--lavender-300); }

  .footer-bottom {
    border-top: 0.5px solid rgba(196,184,240,0.2);
    padding-top: 20px;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .footer-bottom p {
    font-size: 12px;
    color: var(--lavender-400);
    font-weight: 300;
  }

  .not-therapy {
    font-size: 11px;
    color: rgba(196,184,240,0.5);
    font-weight: 300;
  }

  /* ── PAGE ANIMATIONS ── */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(20px); }
    to { opacity: 1; transform: translateY(0); }
  }

  .hero-left > * { animation: fadeUp 0.6s ease both; }
  .hero-left .eyebrow { animation-delay: 0.1s; }
  .hero-left .hero-title { animation-delay: 0.2s; }
  .hero-left .hero-sub { animation-delay: 0.3s; }
  .hero-left .btn-primary { animation-delay: 0.4s; }

  /* ── MODAL (Disclaimer) ── */
  .modal-overlay {
    display: none;
    position: fixed;
    inset: 0;
    background: rgba(58,45,114,0.5);
    z-index: 999;
    align-items: center;
    justify-content: center;
  }
  .modal-overlay.active { display: flex; }

  .modal {
    background: #fff;
    border-radius: 24px;
    padding: 40px;
    max-width: 420px;
    width: 90%;
    text-align: center;
  }

  .modal h2 {
    font-family: 'Lora', serif;
    font-size: 22px;
    color: var(--lavender-800);
    margin-bottom: 12px;
    font-weight: 400;
  }

  .modal p {
    font-size: 14px;
    color: var(--lavender-500);
    line-height: 1.7;
    font-weight: 300;
    margin-bottom: 24px;
  }

  .modal button {
    background: var(--lavender-600);
    color: #fff;
    border: none;
    padding: 12px 32px;
    border-radius: 50px;
    font-size: 14px;
    font-weight: 500;
    cursor: pointer;
    font-family: 'DM Sans', sans-serif;
  }

  /* ── ACTIVE NAV ── */
  .page { display: none; }
  .page.active { display: block; }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <a href="#" class="logo" onclick="showPage('home')">Anne<em>-Xiety</em></a>
  <ul class="nav-links">
    <li><a href="#" onclick="showPage('home')">Home</a></li>
    <li><a href="#" onclick="showPage('blog')">Blog</a></li>
    <li><a href="#" onclick="showPage('tools')">Coping Tools</a></li>
    <li><a href="#" onclick="showPage('education')">Education</a></li>
    <li><a href="#" onclick="showPage('reflections')">Reflections</a></li>
    <li><a href="#" onclick="showPage('resources')" class="nav-cta">Resources</a></li>
  </ul>
</nav>

<!-- ===== HOME PAGE ===== -->
<div id="page-home" class="page active">

  <!-- HERO -->
  <section class="hero">
    <div class="hero-left">
      <div class="eyebrow">Mental Wellness · A Safe Space</div>
      <h1 class="hero-title">You are not <em>too much.</em><br>You are just feeling<br>a lot right now.</h1>
      <p class="hero-sub">A calm corner of the internet for gentle mental health education, grounding tools, and real talk about anxiety — without the clinical jargon.</p>
      <a href="#" class="btn-primary" onclick="showPage('blog')">Start Reading →</a>
    </div>
    <div class="hero-right">
      <div class="hero-circle-1"></div>
      <div class="hero-circle-2"></div>
      <div class="featured-card">
        <div class="feat-tag">Featured Read</div>
        <h2 class="feat-title">Why anxiety feels so much worse at night</h2>
        <p class="feat-excerpt">When the world goes quiet, your nervous system doesn't. Here's what's actually happening — and how to find your way back to calm.</p>
        <a href="#" class="read-link" onclick="showPage('blog')">Read article →</a>
      </div>
    </div>
  </section>

  <!-- MISSION STRIP -->
  <div class="mission-strip">
    <p>"Anxiety is not a character flaw. It's a nervous system doing its best with what it knows."</p>
    <span>— Anne-Xiety Mission</span>
  </div>

  <!-- MAIN LAYOUT -->
  <div style="max-width:1200px; margin:0 auto;">
    <div class="main-layout">
      <div>
        <!-- ARTICLES -->
        <section class="articles-section">
          <div class="section-label">Recent Articles</div>
          <div class="articles-grid">
            <a href="#" class="article-card" onclick="showPage('blog')">
              <div class="card-tag tag-anxiety">Anxiety</div>
              <h3 class="card-title">How to stop a thought spiral before it starts</h3>
              <p class="card-desc">Catching overthinking loops early — and what your brain is actually doing when it won't quiet down.</p>
            </a>
            <a href="#" class="article-card" onclick="showPage('reflections')">
              <div class="card-tag tag-reflect">Reflection</div>
              <h3 class="card-title">You're not lazy. You're overwhelmed.</h3>
              <p class="card-desc">A gentle reminder that rest isn't something you earn — it's something your nervous system needs.</p>
            </a>
            <a href="#" class="article-card" onclick="showPage('education')">
              <div class="card-tag tag-education">Education</div>
              <h3 class="card-title">Anxiety vs. stress vs. panic: what's the difference?</h3>
              <p class="card-desc">Simple, plain-language breakdowns without the clinical overwhelm.</p>
            </a>
            <a href="#" class="article-card" onclick="showPage('tools')">
              <div class="card-tag tag-tools">Coping Tools</div>
              <h3 class="card-title">A 1-minute grounding reset you can do anywhere</h3>
              <p class="card-desc">No apps, no setup. Just your breath and five things you can name around you right now.</p>
            </a>
          </div>
        </section>

        <!-- TOOLS PREVIEW -->
        <section class="tools-section">
          <div class="section-label">Coping Toolkit</div>
          <div class="tools-grid">
            <div class="tool-card">
              <div class="tool-icon">🌬️</div>
              <div class="tool-title">Breathing Reset</div>
              <div class="tool-desc">The 4-7-8 method to calm your nervous system in under a minute.</div>
            </div>
            <div class="tool-card">
              <div class="tool-icon">🌿</div>
              <div class="tool-title">Grounding Exercise</div>
              <div class="tool-desc">5 things you see, 4 you hear, 3 you feel — anchoring you to right now.</div>
            </div>
            <div class="tool-card">
              <div class="tool-icon">📓</div>
              <div class="tool-title">Journal Prompts</div>
              <div class="tool-desc">Gentle questions to help you understand what you're feeling and why.</div>
            </div>
          </div>
        </section>
      </div>

      <!-- SIDEBAR -->
      <aside class="sidebar">
        <div class="section-label" style="font-size:10px; margin-bottom:18px;">Quick Tools</div>
        <div class="sidebar-block">
          <div class="sidebar-title">Calm-down menu</div>
          <div class="tool-item"><div class="tool-dot"></div>Breathing reset (4-7-8)</div>
          <div class="tool-item"><div class="tool-dot"></div>5-4-3-2-1 grounding</div>
          <div class="tool-item"><div class="tool-dot"></div>Thought reframe prompts</div>
          <div class="tool-item"><div class="tool-dot"></div>Calm-down checklist</div>
          <div class="tool-item"><div class="tool-dot"></div>Journaling templates</div>
        </div>

        <div class="quote-block">
          <p class="quote-text">"You are allowed to rest without earning it first."</p>
          <div class="quote-attr">— Anne-Xiety</div>
        </div>

        <div class="sidebar-block">
          <div class="sidebar-title">What is Anne-Xiety?</div>
          <p class="disclaimer">A calming, stigma-free resource hub for understanding anxiety and emotional regulation — written in a warm, non-clinical voice.<br><br>This is <strong>not therapy or medical advice</strong>. It's a digital breathing room — for learning, reflection, and feeling less alone in your mind.</p>
        </div>
      </aside>
    </div>
  </div>

  <!-- REFLECTION BANNER -->
  <section class="reflect-banner">
    <h2>Things nobody tells you about <em>anxiety</em></h2>
    <p>Personal, relatable posts about what it actually feels like — not what the textbooks say.</p>
    <div class="reflect-posts">
      <div class="reflect-pill">Things I wish someone told me during a spiral</div>
      <div class="reflect-pill">What anxiety looks like on a normal Tuesday</div>
      <div class="reflect-pill">You are allowed to rest</div>
      <div class="reflect-pill">When overthinking feels like problem-solving</div>
    </div>
  </section>

  <!-- FOOTER -->
  <footer>
    <div class="footer-grid">
      <div class="footer-brand">
        <a href="#" class="logo" onclick="showPage('home')">Anne<em>-Xiety</em></a>
        <p>A calm, stigma-free mental health blog and resource hub. Not therapy. Not medical advice. Just a soft place to land.</p>
      </div>
      <div class="footer-col">
        <h4>Read</h4>
        <ul>
          <li><a href="#">Blog Articles</a></li>
          <li><a href="#">Reflections</a></li>
          <li><a href="#">Education</a></li>
          <li><a href="#">All Posts</a></li>
        </ul>
      </div>
      <div class="footer-col">
        <h4>Tools</h4>
        <ul>
          <li><a href="#">Breathing Resets</a></li>
          <li><a href="#">Grounding Tools</a></li>
          <li><a href="#">Journal Prompts</a></li>
          <li><a href="#">Checklists</a></li>
        </ul>
      </div>
      <div class="footer-col">
        <h4>Support</h4>
        <ul>
          <li><a href="#">Crisis Lines</a></li>
          <li><a href="#">Find a Therapist</a></li>
          <li><a href="#">Reading List</a></li>
          <li><a href="#">Community</a></li>
        </ul>
      </div>
    </div>
    <div class="footer-bottom">
      <p>© 2025 Anne-Xiety · Made with care 🌿</p>
      <p class="not-therapy">Not a medical service · Not therapy · Not clinical advice</p>
    </div>
  </footer>

</div><!-- end home page -->

<!-- ===== BLOG PAGE ===== -->
<div id="page-blog" class="page">
  <div style="max-width:900px; margin:0 auto; padding:56px 48px;">
    <div class="eyebrow" style="margin-bottom:12px;">The Blog</div>
    <h1 style="font-family:'Lora',serif; font-size:36px; font-weight:400; color:var(--lavender-800); margin-bottom:8px;">Articles & Reflections</h1>
    <p style="color:var(--lavender-400); font-weight:300; margin-bottom:40px; font-size:15px;">Short, honest reads about anxiety, overthinking, and your inner world.</p>

    <div style="display:flex; gap:10px; margin-bottom:36px; flex-wrap:wrap;">
      <button onclick="filterPosts('all')" class="filter-btn active" id="filter-all">All</button>
      <button onclick="filterPosts('anxiety')" class="filter-btn" id="filter-anxiety">Anxiety</button>
      <button onclick="filterPosts('tools')" class="filter-btn" id="filter-tools">Tools</button>
      <button onclick="filterPosts('education')" class="filter-btn" id="filter-education">Education</button>
      <button onclick="filterPosts('reflect')" class="filter-btn" id="filter-reflect">Reflections</button>
    </div>

    <div id="posts-grid" class="articles-grid" style="grid-template-columns:1fr 1fr; display:grid; gap:18px;">
      <div class="article-card" data-tag="anxiety">
        <div class="card-tag tag-anxiety">Anxiety</div>
        <h3 class="card-title">Why anxiety feels worse at night</h3>
        <p class="card-desc">When everything goes quiet, your nervous system doesn't. Here's what's happening and how to find calm.</p>
        <p style="font-size:11px; color:var(--lavender-300); margin-top:12px;">5 min read</p>
      </div>
      <div class="article-card" data-tag="reflect">
        <div class="card-tag tag-reflect">Reflection</div>
        <h3 class="card-title">You're not lazy. You're overwhelmed.</h3>
        <p class="card-desc">Rest isn't something you earn. It's something your nervous system genuinely needs to survive.</p>
        <p style="font-size:11px; color:var(--lavender-300); margin-top:12px;">4 min read</p>
      </div>
      <div class="article-card" data-tag="education">
        <div class="card-tag tag-education">Education</div>
        <h3 class="card-title">Anxiety vs. stress vs. panic</h3>
        <p class="card-desc">They're not the same thing — and knowing the difference can help you respond better in the moment.</p>
        <p style="font-size:11px; color:var(--lavender-300); margin-top:12px;">6 min read</p>
      </div>
      <div class="article-card" data-tag="tools">
        <div class="card-tag tag-tools">Coping Tools</div>
        <h3 class="card-title">A 1-minute grounding reset</h3>
        <p class="card-desc">No apps, no setup. Just your five senses and two minutes of your time.</p>
        <p style="font-size:11px; color:var(--lavender-300); margin-top:12px;">2 min read</p>
      </div>
      <div class="article-card" data-tag="anxiety">
        <div class="card-tag tag-anxiety">Anxiety</div>
        <h3 class="card-title">How to stop spiraling thoughts in real time</h3>
        <p class="card-desc">Catching overthinking loops before they take over — and what your brain is doing when it won't stop.</p>
        <p style="font-size:11px; color:var(--lavender-300); margin-top:12px;">7 min read</p>
      </div>
      <div class="article-card" data-tag="reflect">
        <div class="card-tag tag-reflect">Reflection</div>
        <h3 class="card-title">Things I wish someone told me during anxiety spirals</h3>
        <p class="card-desc">The stuff no one says out loud — but that would have helped so much to hear.</p>
        <p style="font-size:11px; color:var(--lavender-300); margin-top:12px;">5 min read</p>
      </div>
      <div class="article-card" data-tag="education">
        <div class="card-tag tag-education">Education</div>
        <h3 class="card-title">What the fight-or-flight response actually does</h3>
        <p class="card-desc">A plain-language breakdown of why your body reacts the way it does under stress.</p>
        <p style="font-size:11px; color:var(--lavender-300); margin-top:12px;">5 min read</p>
      </div>
      <div class="article-card" data-tag="tools">
        <div class="card-tag tag-tools">Coping Tools</div>
        <h3 class="card-title">Thought reframing prompts for anxious days</h3>
        <p class="card-desc">Gentle questions to shift perspective without toxic positivity or pressure.</p>
        <p style="font-size:11px; color:var(--lavender-300); margin-top:12px;">3 min read</p>
      </div>
    </div>
  </div>
</div>

<!-- ===== TOOLS PAGE ===== -->
<div id="page-tools" class="page">
  <div style="max-width:860px; margin:0 auto; padding:56px 48px;">
    <div class="eyebrow" style="margin-bottom:12px;">Coping Tools</div>
    <h1 style="font-family:'Lora',serif; font-size:36px; font-weight:400; color:var(--lavender-800); margin-bottom:8px;">Your grounding toolkit</h1>
    <p style="color:var(--lavender-400); font-weight:300; margin-bottom:48px; font-size:15px;">Simple, practical tools for anxious moments. No overwhelm. No pressure.</p>

    <div style="display:grid; grid-template-columns:1fr 1fr; gap:20px; margin-bottom:32px;">
      <div style="background:#fff; border-radius:20px; padding:32px; border:0.5px solid var(--lavender-200);">
        <div style="font-size:32px; margin-bottom:16px;">🌬️</div>
        <h3 style="font-family:'Lora',serif; font-size:18px; font-weight:400; color:var(--lavender-800); margin-bottom:10px;">4-7-8 Breathing Reset</h3>
        <p style="font-size:13px; color:var(--lavender-400); line-height:1.7; font-weight:300; margin-bottom:20px;">Inhale for 4 counts, hold for 7, exhale for 8. Repeat 3–4 times. This activates your parasympathetic nervous system and signals safety to your body.</p>
        <div style="background:var(--lavender-100); border-radius:12px; padding:16px; font-size:13px; color:var(--lavender-600);">
          Best for: Panic moments, racing heart, falling asleep
        </div>
      </div>
      <div style="background:#fff; border-radius:20px; padding:32px; border:0.5px solid var(--lavender-200);">
        <div style="font-size:32px; margin-bottom:16px;">🌿</div>
        <h3 style="font-family:'Lora',serif; font-size:18px; font-weight:400; color:var(--lavender-800); margin-bottom:10px;">5-4-3-2-1 Grounding</h3>
        <p style="font-size:13px; color:var(--lavender-400); line-height:1.7; font-weight:300; margin-bottom:20px;">Name 5 things you see, 4 you can touch, 3 you hear, 2 you smell, 1 you taste. This interrupts the anxiety loop by anchoring you to the present.</p>
        <div style="background:var(--mint); border-radius:12px; padding:16px; font-size:13px; color:var(--mint-text);">
          Best for: Spiraling thoughts, dissociation, overwhelm
        </div>
      </div>
      <div style="background:#fff; border-radius:20px; padding:32px; border:0.5px solid var(--lavender-200);">
        <div style="font-size:32px; margin-bottom:16px;">📓</div>
        <h3 style="font-family:'Lora',serif; font-size:18px; font-weight:400; color:var(--lavender-800); margin-bottom:10px;">Journal Prompts</h3>
        <p style="font-size:13px; color:var(--lavender-400); line-height:1.7; font-weight:300; margin-bottom:16px;">Gentle prompts to help you process what you're feeling without judgment.</p>
        <ul style="list-style:none; font-size:13px; color:var(--lavender-500); font-weight:300;">
          <li style="padding:6px 0; border-bottom:0.5px solid var(--lavender-100);">What am I actually afraid of right now?</li>
          <li style="padding:6px 0; border-bottom:0.5px solid var(--lavender-100);">What would I say to a friend feeling this way?</li>
          <li style="padding:6px 0; border-bottom:0.5px solid var(--lavender-100);">What do I need most in this moment?</li>
          <li style="padding:6px 0;">What is in my control right now?</li>
        </ul>
      </div>
      <div style="background:#fff; border-radius:20px; padding:32px; border:0.5px solid var(--lavender-200);">
        <div style="font-size:32px; margin-bottom:16px;">✅</div>
        <h3 style="font-family:'Lora',serif; font-size:18px; font-weight:400; color:var(--lavender-800); margin-bottom:10px;">Calm-Down Checklist</h3>
        <p style="font-size:13px; color:var(--lavender-400); line-height:1.7; font-weight:300; margin-bottom:16px;">When anxiety strikes and you don't know where to start:</p>
        <ul style="list-style:none; font-size:13px; color:var(--lavender-500); font-weight:300;">
          <li style="padding:6px 0; border-bottom:0.5px solid var(--lavender-100);">☐ Take 3 slow deep breaths</li>
          <li style="padding:6px 0; border-bottom:0.5px solid var(--lavender-100);">☐ Drink a glass of water</li>
          <li style="padding:6px 0; border-bottom:0.5px solid var(--lavender-100);">☐ Name 3 things you can see</li>
          <li style="padding:6px 0; border-bottom:0.5px solid var(--lavender-100);">☐ Unclench your jaw and shoulders</li>
          <li style="padding:6px 0;">☐ Give yourself permission to feel this</li>
        </ul>
      </div>
    </div>

    <div style="background:var(--lavender-100); border-radius:20px; padding:28px 32px; text-align:center;">
      <p style="font-family:'Lora',serif; font-style:italic; font-size:16px; color:var(--lavender-600); margin-bottom:6px;">"You don't have to feel better immediately. You just have to make it to the next moment."</p>
      <span style="font-size:12px; color:var(--lavender-400);">— Anne-Xiety</span>
    </div>
  </div>
</div>

<!-- ===== EDUCATION PAGE ===== -->
<div id="page-education" class="page">
  <div style="max-width:760px; margin:0 auto; padding:56px 48px;">
    <div class="eyebrow" style="margin-bottom:12px;">Mental Health Education</div>
    <h1 style="font-family:'Lora',serif; font-size:36px; font-weight:400; color:var(--lavender-800); margin-bottom:8px;">Understanding your mind</h1>
    <p style="color:var(--lavender-400); font-weight:300; margin-bottom:48px; font-size:15px;">Simple explanations. No jargon. No clinical overwhelm.</p>

    <div style="display:flex; flex-direction:column; gap:20px;">
      <div style="background:#fff; border-radius:18px; padding:28px 32px; border:0.5px solid var(--lavender-200);">
        <div class="card-tag tag-education" style="margin-bottom:12px;">Education</div>
        <h3 style="font-family:'Lora',serif; font-size:20px; font-weight:400; color:var(--lavender-800); margin-bottom:12px;">What is anxiety, really?</h3>
        <p style="font-size:14px; color:var(--lavender-500); line-height:1.75; font-weight:300;">Anxiety is your brain's alarm system. It's designed to protect you from danger — but sometimes it misfires, treating everyday situations like threats. This isn't weakness. It's biology. And it can be worked with.</p>
      </div>
      <div style="background:#fff; border-radius:18px; padding:28px 32px; border:0.5px solid var(--lavender-200);">
        <div class="card-tag tag-education" style="margin-bottom:12px;">Education</div>
        <h3 style="font-family:'Lora',serif; font-size:20px; font-weight:400; color:var(--lavender-800); margin-bottom:12px;">The fight-or-flight response explained</h3>
        <p style="font-size:14px; color:var(--lavender-500); line-height:1.75; font-weight:300;">When your brain perceives threat, it floods your body with adrenaline and cortisol. Your heart races. Your muscles tighten. Your thoughts speed up. This is your nervous system doing its job — the problem is it can't always tell real danger from social anxiety or work stress.</p>
      </div>
      <div style="background:#fff; border-radius:18px; padding:28px 32px; border:0.5px solid var(--lavender-200);">
        <div class="card-tag tag-education" style="margin-bottom:12px;">Education</div>
        <h3 style="font-family:'Lora',serif; font-size:20px; font-weight:400; color:var(--lavender-800); margin-bottom:12px;">Anxiety vs. stress vs. panic — what's different?</h3>
        <p style="font-size:14px; color:var(--lavender-500); line-height:1.75; font-weight:300;"><strong style="color:var(--lavender-600);">Stress</strong> is usually tied to a specific situation and fades when it resolves. <strong style="color:var(--lavender-600);">Anxiety</strong> persists even when no direct threat is present — it's more of a background hum of "what if." <strong style="color:var(--lavender-600);">Panic</strong> is an acute, intense episode that peaks and passes — often terrifying but not dangerous.</p>
      </div>
      <div style="background:#fff; border-radius:18px; padding:28px 32px; border:0.5px solid var(--lavender-200);">
        <div class="card-tag tag-education" style="margin-bottom:12px;">Education</div>
        <h3 style="font-family:'Lora',serif; font-size:20px; font-weight:400; color:var(--lavender-800); margin-bottom:12px;">What are overthinking loops?</h3>
        <p style="font-size:14px; color:var(--lavender-500); line-height:1.75; font-weight:300;">Overthinking isn't a personality trait — it's a thought pattern where your brain gets stuck in repetitive "what if" cycles. It can feel like problem-solving, but often isn't. Learning to interrupt the loop (not eliminate the thoughts) is the key.</p>
      </div>
    </div>
  </div>
</div>

<!-- ===== REFLECTIONS PAGE ===== -->
<div id="page-reflections" class="page">
  <div style="max-width:760px; margin:0 auto; padding:56px 48px;">
    <div class="eyebrow" style="margin-bottom:12px;">Reflections</div>
    <h1 style="font-family:'Lora',serif; font-size:36px; font-weight:400; color:var(--lavender-800); margin-bottom:8px;">Personal, honest, real</h1>
    <p style="color:var(--lavender-400); font-weight:300; margin-bottom:48px; font-size:15px;">Not what the textbooks say. What it actually feels like.</p>

    <div style="display:flex; flex-direction:column; gap:24px;">
      <div style="background:#fff; border-radius:20px; padding:32px; border:0.5px solid var(--lavender-200);">
        <div class="card-tag tag-reflect" style="margin-bottom:14px;">Reflection</div>
        <h3 style="font-family:'Lora',serif; font-size:22px; font-weight:400; color:var(--lavender-800); margin-bottom:14px; font-style:italic;">You are allowed to rest without earning it.</h3>
        <p style="font-size:14px; color:var(--lavender-500); line-height:1.8; font-weight:300;">There's this quiet belief a lot of us carry — that rest has to be deserved. That you can only stop when everything is done, when you've been productive enough, when you've earned the right to breathe. That belief isn't true. And it's exhausting you.</p>
      </div>
      <div style="background:#fff; border-radius:20px; padding:32px; border:0.5px solid var(--lavender-200);">
        <div class="card-tag tag-reflect" style="margin-bottom:14px;">Reflection</div>
        <h3 style="font-family:'Lora',serif; font-size:22px; font-weight:400; color:var(--lavender-800); margin-bottom:14px; font-style:italic;">Things I wish someone told me during an anxiety spiral.</h3>
        <p style="font-size:14px; color:var(--lavender-500); line-height:1.8; font-weight:300;">That it would pass. That I wasn't broken. That the thoughts, as loud as they were, were just thoughts — not facts. That I didn't have to solve anything right now. That I just had to get to the next moment, and then the one after that.</p>
      </div>
      <div style="background:#fff; border-radius:20px; padding:32px; border:0.5px solid var(--lavender-200);">
        <div class="card-tag tag-reflect" style="margin-bottom:14px;">Reflection</div>
        <h3 style="font-family:'Lora',serif; font-size:22px; font-weight:400; color:var(--lavender-800); margin-bottom:14px; font-style:italic;">What anxiety looks like on a regular Tuesday.</h3>
        <p style="font-size:14px; color:var(--lavender-500); line-height:1.8; font-weight:300;">It's not always a dramatic spiral. Sometimes it's just re-reading a text four times. Feeling a little off but not knowing why. Rehearsing conversations that haven't happened. Anxiety lives in the mundane, too — and that's okay to acknowledge.</p>
      </div>
    </div>
  </div>
</div>

<!-- ===== RESOURCES PAGE ===== -->
<div id="page-resources" class="page">
  <div style="max-width:800px; margin:0 auto; padding:56px 48px;">
    <div class="eyebrow" style="margin-bottom:12px;">Resource Library</div>
    <h1 style="font-family:'Lora',serif; font-size:36px; font-weight:400; color:var(--lavender-800); margin-bottom:8px;">Support & Resources</h1>
    <p style="color:var(--lavender-400); font-weight:300; margin-bottom:12px; font-size:15px;">Curated links to trustworthy mental health support. Always here if you need them.</p>

    <div style="background:var(--blush); border-radius:16px; padding:18px 22px; margin-bottom:40px; border:0.5px solid #F4C0D1;">
      <p style="font-size:13px; color:var(--blush-text); font-weight:400;">If you are in crisis or need immediate support, please reach out to a crisis line in your area. You are not alone.</p>
    </div>

    <div style="display:flex; flex-direction:column; gap:16px;">
      <div style="background:#fff; border-radius:16px; padding:22px 26px; border:0.5px solid var(--lavender-200); display:flex; align-items:center; gap:20px;">
        <div style="width:48px; height:48px; background:var(--lavender-100); border-radius:12px; display:flex; align-items:center; justify-content:center; font-size:22px; flex-shrink:0;">📞</div>
        <div>
          <h4 style="font-family:'Lora',serif; font-size:16px; font-weight:400; color:var(--lavender-800); margin-bottom:4px;">Crisis Text Line</h4>
          <p style="font-size:13px; color:var(--lavender-400); font-weight:300;">Text HOME to 741741 — free, 24/7, confidential support via text.</p>
        </div>
      </div>
      <div style="background:#fff; border-radius:16px; padding:22px 26px; border:0.5px solid var(--lavender-200); display:flex; align-items:center; gap:20px;">
        <div style="width:48px; height:48px; background:var(--lavender-100); border-radius:12px; display:flex; align-items:center; justify-content:center; font-size:22px; flex-shrink:0;">🧠</div>
        <div>
          <h4 style="font-family:'Lora',serif; font-size:16px; font-weight:400; color:var(--lavender-800); margin-bottom:4px;">NAMI (National Alliance on Mental Illness)</h4>
          <p style="font-size:13px; color:var(--lavender-400); font-weight:300;">Education, support groups, and helplines for anyone affected by mental illness.</p>
        </div>
      </div>
      <div style="background:#fff; border-radius:16px; padding:22px 26px; border:0.5px solid var(--lavender-200); display:flex; align-items:center; gap:20px;">
        <div style="width:48px; height:48px; background:var(--mint); border-radius:12px; display:flex; align-items:center; justify-content:center; font-size:22px; flex-shrink:0;">💬</div>
        <div>
          <h4 style="font-family:'Lora',serif; font-size:16px; font-weight:400; color:var(--lavender-800); margin-bottom:4px;">Psychology Today Therapist Finder</h4>
          <p style="font-size:13px; color:var(--lavender-400); font-weight:300;">Search for licensed therapists near you by specialty, insurance, and availability.</p>
        </div>
      </div>
      <div style="background:#fff; border-radius:16px; padding:22px 26px; border:0.5px solid var(--lavender-200); display:flex; align-items:center; gap:20px;">
        <div style="width:48px; height:48px; background:var(--sky); border-radius:12px; display:flex; align-items:center; justify-content:center; font-size:22px; flex-shrink:0;">📚</div>
        <div>
          <h4 style="font-family:'Lora',serif; font-size:16px; font-weight:400; color:var(--lavender-800); margin-bottom:4px;">Recommended Reading</h4>
          <p style="font-size:13px; color:var(--lavender-400); font-weight:300;"><em>The Anxiety & Worry Workbook</em> · <em>Dare</em> by Barry McDonagh · <em>First, We Make the Beast Beautiful</em></p>
        </div>
      </div>
    </div>

    <div style="margin-top:40px; background:var(--lavender-100); border-radius:20px; padding:28px 32px; text-align:center;">
      <p style="font-size:13px; color:var(--lavender-500); font-weight:300; line-height:1.7;">Anne-Xiety is not a medical service, therapy, or crisis line. If you are in immediate danger, please call emergency services (911 in the US) or your local equivalent.</p>
    </div>
  </div>
</div>

<!-- FILTER BUTTONS STYLE -->
<style>
  .filter-btn {
    background: #fff;
    border: 0.5px solid var(--lavender-200);
    color: var(--lavender-500);
    padding: 8px 18px;
    border-radius: 50px;
    font-size: 12px;
    font-family: 'DM Sans', sans-serif;
    cursor: pointer;
    transition: all 0.2s;
    font-weight: 400;
  }
  .filter-btn:hover, .filter-btn.active {
    background: var(--lavender-100);
    border-color: var(--lavender-400);
    color: var(--lavender-700);
  }
</style>

<script>
  function showPage(name) {
    document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));
    document.getElementById('page-' + name).classList.add('active');
    window.scrollTo({ top: 0, behavior: 'smooth' });
  }

  function filterPosts(tag) {
    document.querySelectorAll('.filter-btn').forEach(b => b.classList.remove('active'));
    document.getElementById('filter-' + tag).classList.add('active');
    document.querySelectorAll('#posts-grid .article-card').forEach(card => {
      if (tag === 'all' || card.dataset.tag === tag) {
        card.style.display = 'block';
      } else {
        card.style.display = 'none';
      }
    });
  }
</script>
</body>
</html>
