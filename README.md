<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>COLLAR — Men's Fashion</title>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,600;1,300;1,400&family=Montserrat:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
:root {
  --black: #0f0f0f;
  --white: #faf8f5;
  --gold: #b8975a;
  --gold-light: #d4b483;
  --gray: #888;
  --gray-light: #e8e4de;
}

*, *::before, *::after { margin: 0; padding: 0; box-sizing: border-box; }

html { scroll-behavior: smooth; }

body {
  background: var(--white);
  color: var(--black);
  font-family: 'Montserrat', sans-serif;
  overflow-x: hidden;
}

/* ── NAV ── */
nav {
  position: fixed;
  top: 0; left: 0; right: 0;
  z-index: 100;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 0 48px;
  height: 72px;
  background: rgba(250,248,245,0.95);
  border-bottom: 0.5px solid var(--gray-light);
  backdrop-filter: blur(8px);
}

.nav-logo {
  font-family: 'Cormorant Garamond', serif;
  font-size: 26px;
  font-weight: 300;
  letter-spacing: 0.35em;
  text-transform: uppercase;
  color: var(--black);
  text-decoration: none;
}

.nav-links {
  display: flex;
  gap: 36px;
  list-style: none;
}

.nav-links a {
  font-size: 10px;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  color: var(--gray);
  text-decoration: none;
  transition: color 0.2s;
}
.nav-links a:hover { color: var(--black); }

.nav-cart {
  font-size: 10px;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  color: var(--black);
  cursor: pointer;
  border: 0.5px solid var(--black);
  padding: 8px 20px;
  transition: all 0.2s;
}
.nav-cart:hover { background: var(--black); color: var(--white); }

/* ── HERO ── */
.hero {
  margin-top: 72px;
  height: calc(100vh - 72px);
  display: grid;
  grid-template-columns: 1fr 1fr;
  overflow: hidden;
}

.hero-left {
  background: var(--black);
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
  padding: 64px;
  position: relative;
  overflow: hidden;
}

.hero-left::before {
  content: 'COLLAR';
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  font-family: 'Cormorant Garamond', serif;
  font-size: 160px;
  font-weight: 300;
  color: rgba(255,255,255,0.03);
  letter-spacing: 0.2em;
  white-space: nowrap;
  pointer-events: none;
}

.hero-eyebrow {
  font-size: 10px;
  letter-spacing: 0.3em;
  text-transform: uppercase;
  color: var(--gold);
  margin-bottom: 20px;
}

.hero-title {
  font-family: 'Cormorant Garamond', serif;
  font-size: 72px;
  font-weight: 300;
  line-height: 1.05;
  color: var(--white);
  margin-bottom: 24px;
}

.hero-title em {
  font-style: italic;
  color: var(--gold-light);
}

.hero-desc {
  font-size: 13px;
  line-height: 1.8;
  color: rgba(255,255,255,0.5);
  max-width: 360px;
  margin-bottom: 40px;
}

.hero-cta {
  display: inline-block;
  font-size: 10px;
  letter-spacing: 0.25em;
  text-transform: uppercase;
  color: var(--white);
  border: 0.5px solid var(--gold);
  padding: 14px 36px;
  text-decoration: none;
  transition: all 0.3s;
}
.hero-cta:hover { background: var(--gold); color: var(--black); }

.hero-right {
  position: relative;
  overflow: hidden;
}

.hero-right img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: top center;
  transition: transform 6s ease;
}
.hero-right:hover img { transform: scale(1.04); }

.hero-badge {
  position: absolute;
  bottom: 40px;
  right: 40px;
  background: var(--white);
  padding: 16px 20px;
  text-align: center;
}
.hero-badge-num {
  font-family: 'Cormorant Garamond', serif;
  font-size: 36px;
  font-weight: 300;
  line-height: 1;
  color: var(--black);
}
.hero-badge-label {
  font-size: 9px;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  color: var(--gray);
  margin-top: 4px;
}

/* ── MARQUEE ── */
.marquee-wrap {
  background: var(--black);
  padding: 14px 0;
  overflow: hidden;
  white-space: nowrap;
}
.marquee-track {
  display: inline-block;
  animation: marquee 20s linear infinite;
}
.marquee-item {
  display: inline-block;
  font-size: 10px;
  letter-spacing: 0.3em;
  text-transform: uppercase;
  color: var(--gold);
  margin: 0 32px;
}
.marquee-dot {
  display: inline-block;
  width: 4px;
  height: 4px;
  background: var(--gold);
  border-radius: 50%;
  vertical-align: middle;
  margin: 0 16px;
}
@keyframes marquee { from { transform: translateX(0); } to { transform: translateX(-50%); } }

/* ── SECTION HEADER ── */
.section-header {
  text-align: center;
  padding: 80px 48px 48px;
}
.section-eyebrow {
  font-size: 10px;
  letter-spacing: 0.3em;
  text-transform: uppercase;
  color: var(--gold);
  margin-bottom: 16px;
}
.section-title {
  font-family: 'Cormorant Garamond', serif;
  font-size: 48px;
  font-weight: 300;
  color: var(--black);
  line-height: 1.1;
}
.section-line {
  width: 40px;
  height: 1px;
  background: var(--gold);
  margin: 20px auto 0;
}

/* ── CATEGORIES ── */
.categories { padding: 0 48px 100px; }

/* ── CATEGORY: FEATURED (full width) ── */
.cat-featured {
  display: grid;
  grid-template-columns: 1fr 1fr;
  min-height: 580px;
  margin-bottom: 24px;
  overflow: hidden;
  border: 0.5px solid var(--gray-light);
}

.cat-featured.reverse { direction: rtl; }
.cat-featured.reverse > * { direction: ltr; }

.cat-image {
  position: relative;
  overflow: hidden;
  background: #1a1a1a;
}
.cat-image img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: top center;
  transition: transform 0.7s ease;
  display: block;
}
.cat-image:hover img { transform: scale(1.05); }

.cat-image-placeholder {
  width: 100%;
  height: 100%;
  min-height: 500px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  background: #1a1a1a;
  gap: 16px;
}

.cat-num {
  position: absolute;
  top: 24px;
  left: 24px;
  font-family: 'Cormorant Garamond', serif;
  font-size: 13px;
  color: rgba(255,255,255,0.4);
  letter-spacing: 0.1em;
}

.cat-content {
  background: var(--white);
  padding: 64px 56px;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.cat-tag {
  font-size: 9px;
  letter-spacing: 0.3em;
  text-transform: uppercase;
  color: var(--gold);
  margin-bottom: 16px;
}

.cat-title {
  font-family: 'Cormorant Garamond', serif;
  font-size: 52px;
  font-weight: 300;
  line-height: 1.05;
  color: var(--black);
  margin-bottom: 20px;
}

.cat-title em { font-style: italic; color: var(--gold-light); }

.cat-desc {
  font-size: 13px;
  line-height: 1.9;
  color: var(--gray);
  margin-bottom: 32px;
  max-width: 340px;
}

.cat-features {
  list-style: none;
  margin-bottom: 36px;
}
.cat-features li {
  font-size: 11px;
  letter-spacing: 0.12em;
  text-transform: uppercase;
  color: var(--black);
  padding: 8px 0;
  border-bottom: 0.5px solid var(--gray-light);
  display: flex;
  align-items: center;
  gap: 10px;
}
.cat-features li::before {
  content: '';
  display: inline-block;
  width: 16px;
  height: 0.5px;
  background: var(--gold);
}

.cat-btn {
  display: inline-block;
  font-size: 10px;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  color: var(--black);
  border: 0.5px solid var(--black);
  padding: 12px 28px;
  text-decoration: none;
  transition: all 0.3s;
  align-self: flex-start;
  cursor: pointer;
}
.cat-btn:hover { background: var(--black); color: var(--white); }

/* ── CATEGORY GRID (3 col) ── */
.cat-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 24px;
  margin-bottom: 24px;
}

.cat-card {
  border: 0.5px solid var(--gray-light);
  overflow: hidden;
  cursor: pointer;
}

.cat-card-image {
  position: relative;
  height: 420px;
  overflow: hidden;
  background: #1a1a1a;
}
.cat-card-image img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: top center;
  transition: transform 0.7s ease;
}
.cat-card:hover .cat-card-image img { transform: scale(1.06); }

.cat-card-placeholder {
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 12px;
}

.cat-card-num {
  position: absolute;
  top: 16px;
  left: 16px;
  font-family: 'Cormorant Garamond', serif;
  font-size: 12px;
  color: rgba(255,255,255,0.35);
}

.cat-card-body {
  padding: 28px 24px;
  background: var(--white);
}
.cat-card-tag {
  font-size: 9px;
  letter-spacing: 0.25em;
  text-transform: uppercase;
  color: var(--gold);
  margin-bottom: 8px;
}
.cat-card-title {
  font-family: 'Cormorant Garamond', serif;
  font-size: 30px;
  font-weight: 300;
  color: var(--black);
  margin-bottom: 10px;
  line-height: 1.1;
}
.cat-card-desc {
  font-size: 12px;
  line-height: 1.8;
  color: var(--gray);
  margin-bottom: 20px;
}
.cat-card-btn {
  font-size: 9px;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  color: var(--black);
  border-bottom: 0.5px solid var(--gold);
  padding-bottom: 2px;
  cursor: pointer;
  display: inline-block;
}

/* ── PANTS — full width editorial ── */
.cat-pants {
  display: grid;
  grid-template-columns: 2fr 1fr 1fr;
  min-height: 500px;
  border: 0.5px solid var(--gray-light);
  overflow: hidden;
}
.cat-pants-main {
  position: relative;
  overflow: hidden;
  background: #111;
}
.cat-pants-main img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: top center;
  transition: transform 0.7s;
}
.cat-pants-main:hover img { transform: scale(1.04); }
.cat-pants-main-placeholder {
  width: 100%;
  height: 100%;
  min-height: 500px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 16px;
}
.cat-pants-overlay {
  position: absolute;
  bottom: 0; left: 0; right: 0;
  background: linear-gradient(transparent, rgba(0,0,0,0.7));
  padding: 40px;
}
.cat-pants-overlay .cat-title {
  color: var(--white);
  font-size: 42px;
  margin-bottom: 8px;
}
.cat-pants-overlay .cat-tag { margin-bottom: 8px; }
.cat-pants-overlay .cat-desc { color: rgba(255,255,255,0.6); margin-bottom: 0; }

.cat-pants-side {
  border-left: 0.5px solid var(--gray-light);
  display: flex;
  flex-direction: column;
}
.cat-pants-side-top {
  flex: 1;
  background: var(--black);
  padding: 40px 32px;
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
  border-bottom: 0.5px solid #333;
}
.cat-pants-side-bottom {
  flex: 1;
  padding: 32px;
  display: flex;
  flex-direction: column;
  justify-content: center;
}
.stat-num {
  font-family: 'Cormorant Garamond', serif;
  font-size: 56px;
  font-weight: 300;
  color: var(--gold);
  line-height: 1;
  margin-bottom: 4px;
}
.stat-label {
  font-size: 10px;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  color: rgba(255,255,255,0.5);
}
.stat-label-dark {
  font-size: 10px;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  color: var(--gray);
}

/* ── FOOTER ── */
footer {
  background: var(--black);
  padding: 64px 48px 32px;
}
.footer-top {
  display: grid;
  grid-template-columns: 2fr 1fr 1fr 1fr;
  gap: 48px;
  padding-bottom: 48px;
  border-bottom: 0.5px solid #222;
  margin-bottom: 32px;
}
.footer-brand {
  font-family: 'Cormorant Garamond', serif;
  font-size: 36px;
  font-weight: 300;
  letter-spacing: 0.3em;
  color: var(--white);
  margin-bottom: 16px;
}
.footer-tagline {
  font-size: 12px;
  line-height: 1.8;
  color: rgba(255,255,255,0.4);
  max-width: 260px;
}
.footer-col-title {
  font-size: 10px;
  letter-spacing: 0.25em;
  text-transform: uppercase;
  color: var(--gold);
  margin-bottom: 20px;
}
.footer-links { list-style: none; }
.footer-links li {
  margin-bottom: 10px;
}
.footer-links a {
  font-size: 12px;
  color: rgba(255,255,255,0.4);
  text-decoration: none;
  transition: color 0.2s;
}
.footer-links a:hover { color: var(--white); }
.footer-bottom {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.footer-copy {
  font-size: 11px;
  color: rgba(255,255,255,0.2);
}

/* ── SVG ICON PLACEHOLDERS (for images) ── */
.img-icon {
  opacity: 0.15;
}

/* ── RESPONSIVE ── */
@media (max-width: 900px) {
  nav { padding: 0 24px; }
  .nav-links { display: none; }
  .hero { grid-template-columns: 1fr; }
  .hero-right { display: none; }
  .hero-title { font-size: 48px; }
  .cat-featured { grid-template-columns: 1fr; }
  .cat-featured .cat-image { min-height: 300px; }
  .cat-grid { grid-template-columns: 1fr; }
  .cat-pants { grid-template-columns: 1fr; }
  .categories { padding: 0 20px 60px; }
  .section-header { padding: 48px 20px 32px; }
  .footer-top { grid-template-columns: 1fr 1fr; }
}

/* ── ANIMATIONS ── */
@keyframes fadeUp {
  from { opacity: 0; transform: translateY(30px); }
  to { opacity: 1; transform: translateY(0); }
}

.hero-eyebrow { animation: fadeUp 0.8s ease 0.1s both; }
.hero-title { animation: fadeUp 0.8s ease 0.25s both; }
.hero-desc { animation: fadeUp 0.8s ease 0.4s both; }
.hero-cta { animation: fadeUp 0.8s ease 0.55s both; }
</style>
</head>
<body>

<!-- ── NAV ── -->
<nav>
  <a href="#" class="nav-logo">Collar</a>
  <ul class="nav-links">
    <li><a href="#categories">Collections</a></li>
    <li><a href="#">About</a></li>
    <li><a href="#">Lookbook</a></li>
    <li><a href="#">Contact</a></li>
  </ul>
  <div class="nav-cart">Shop Now</div>
</nav>

<!-- ── HERO ── -->
<section class="hero">
  <div class="hero-left">
    <div class="hero-eyebrow">New Collection — 2025</div>
    <h1 class="hero-title">Dress Like<br>a <em>Gentleman.</em><br>Feel Like a King.</h1>
    <p class="hero-desc">Premium men's fashion crafted for the modern Bengali man. From boardroom to boulevard — COLLAR has you covered.</p>
    <a href="#categories" class="hero-cta">Explore Collection</a>
  </div>
  <div class="hero-right">
    <img src="https://images.unsplash.com/photo-1617137968427-85924c800a22?w=900&q=85&fit=crop" alt="COLLAR formal men's fashion" onerror="this.style.display='none'"/>
    <div class="hero-badge">
      <div class="hero-badge-num">6</div>
      <div class="hero-badge-label">Collections</div>
    </div>
  </div>
</section>

<!-- ── MARQUEE ── -->
<div class="marquee-wrap">
  <div class="marquee-track">
    <span class="marquee-item">Formal Shirts</span><span class="marquee-dot"></span>
    <span class="marquee-item">Old Money</span><span class="marquee-dot"></span>
    <span class="marquee-item">Polo</span><span class="marquee-dot"></span>
    <span class="marquee-item">Drop Shoulder</span><span class="marquee-dot"></span>
    <span class="marquee-item">T-Shirts</span><span class="marquee-dot"></span>
    <span class="marquee-item">Trousers</span><span class="marquee-dot"></span>
    <span class="marquee-item">Premium Quality</span><span class="marquee-dot"></span>
    <span class="marquee-item">Made in Bangladesh</span><span class="marquee-dot"></span>
    <span class="marquee-item">Formal Shirts</span><span class="marquee-dot"></span>
    <span class="marquee-item">Old Money</span><span class="marquee-dot"></span>
    <span class="marquee-item">Polo</span><span class="marquee-dot"></span>
    <span class="marquee-item">Drop Shoulder</span><span class="marquee-dot"></span>
    <span class="marquee-item">T-Shirts</span><span class="marquee-dot"></span>
    <span class="marquee-item">Trousers</span><span class="marquee-dot"></span>
    <span class="marquee-item">Premium Quality</span><span class="marquee-dot"></span>
    <span class="marquee-item">Made in Bangladesh</span><span class="marquee-dot"></span>
  </div>
</div>

<!-- ── CATEGORIES ── -->
<div id="categories">
  <div class="section-header">
    <div class="section-eyebrow">Shop by Category</div>
    <h2 class="section-title">Our Collections</h2>
    <div class="section-line"></div>
  </div>

  <div class="categories">

    <!-- 01 FORMAL SHIRT — featured left image -->
    <div class="cat-featured" style="margin-bottom:24px;">
      <div class="cat-image">
        <span class="cat-num">01</span>
        <img src="https://images.unsplash.com/photo-1602810318383-e386cc2a3ccf?w=900&q=85&fit=crop&crop=top" alt="Formal Shirt" onerror="this.parentElement.style.background='#1a1a1a'"/>
      </div>
      <div class="cat-content">
        <div class="cat-tag">Category 01</div>
        <h2 class="cat-title">Formal<br><em>Shirts</em></h2>
        <p class="cat-desc">Sharp lines, premium cotton, and impeccable tailoring. Our formal shirts are engineered for the man who means business — whether it's a boardroom meeting or a formal occasion that demands excellence.</p>
        <ul class="cat-features">
          <li>100% Premium Cotton Poplin</li>
          <li>Slim & Regular Fit Available</li>
          <li>French Cuff & Button-Down Options</li>
          <li>Office · Event · Ceremony</li>
        </ul>
        <a class="cat-btn">Shop Formal →</a>
      </div>
    </div>

    <!-- 02 OLD MONEY — featured right image -->
    <div class="cat-featured reverse" style="margin-bottom:24px;">
      <div class="cat-image">
        <span class="cat-num">02</span>
        <img src="https://images.unsplash.com/photo-1550246140-29f40b909e5a?w=900&q=85&fit=crop&crop=top" alt="Old Money Shirt" onerror="this.parentElement.style.background='#1a1a1a'"/>
      </div>
      <div class="cat-content">
        <div class="cat-tag">Category 02</div>
        <h2 class="cat-title">Old<br><em>Money</em></h2>
        <p class="cat-desc">Understated luxury. Quiet confidence. The Old Money collection draws from timeless aristocratic heritage — refined fabrics, muted palettes, and silhouettes that whisper wealth rather than shout it.</p>
        <ul class="cat-features">
          <li>Linen & Oxford Blends</li>
          <li>Earthy, Muted Tones</li>
          <li>Relaxed Elegant Fit</li>
          <li>Heritage · Class · Refinement</li>
        </ul>
        <a class="cat-btn">Shop Old Money →</a>
      </div>
    </div>

    <!-- 03, 04, 05 — 3-column grid -->
    <div class="cat-grid">

      <!-- POLO -->
      <div class="cat-card">
        <div class="cat-card-image">
          <span class="cat-card-num">03</span>
          <img src="https://images.unsplash.com/photo-1589902860314-e910697dea18?w=700&q=85&fit=crop&crop=top" alt="Polo Shirt" onerror="this.parentElement.style.background='#1a1a1a'"/>
        </div>
        <div class="cat-card-body">
          <div class="cat-card-tag">Category 03</div>
          <h3 class="cat-card-title">Polo<br>Shirts</h3>
          <p class="cat-card-desc">The perfect bridge between casual and smart. Our polo shirts are crafted from breathable piqué cotton — effortlessly stylish from morning to evening. Weekend outings, family gatherings, or a casual Friday at work.</p>
          <span class="cat-card-btn">Shop Polo →</span>
        </div>
      </div>

      <!-- DROP SHOULDER -->
      <div class="cat-card">
        <div class="cat-card-image">
          <span class="cat-card-num">04</span>
          <img src="https://images.unsplash.com/photo-1503341455253-b2e723bb3dbb?w=700&q=85&fit=crop&crop=top" alt="Drop Shoulder" onerror="this.parentElement.style.background='#1a1a1a'"/>
        </div>
        <div class="cat-card-body">
          <div class="cat-card-tag">Category 04</div>
          <h3 class="cat-card-title">Drop<br>Shoulder</h3>
          <p class="cat-card-desc">Street-meets-luxury. The drop shoulder silhouette redefines modern Bengali street style — oversized, confident, and undeniably cool. Built for those who set the trend, not follow it.</p>
          <span class="cat-card-btn">Shop Drop Shoulder →</span>
        </div>
      </div>

      <!-- T-SHIRT -->
      <div class="cat-card">
        <div class="cat-card-image">
          <span class="cat-card-num">05</span>
          <img src="https://images.unsplash.com/photo-1521572163474-6864f9cf17ab?w=700&q=85&fit=crop&crop=top" alt="T-Shirt" onerror="this.parentElement.style.background='#1a1a1a'"/>
        </div>
        <div class="cat-card-body">
          <div class="cat-card-tag">Category 05</div>
          <h3 class="cat-card-title">Premium<br>T-Shirts</h3>
          <p class="cat-card-desc">Simplicity perfected. Our premium tees are made from heavyweight cotton with a structured fit that holds shape all day. The foundation of every great wardrobe — done right.</p>
          <span class="cat-card-btn">Shop T-Shirts →</span>
        </div>
      </div>

    </div>

    <!-- 06 PANTS — editorial wide -->
    <div class="cat-pants">
      <div class="cat-pants-main">
        <img src="https://images.unsplash.com/photo-1473966968600-fa801b869a1a?w=1000&q=85&fit=crop&crop=top" alt="Premium Trousers" onerror="this.parentElement.style.background='#1a1a1a'"/>
        <div class="cat-pants-overlay">
          <div class="cat-tag">Category 06</div>
          <h2 class="cat-title" style="color:var(--white);font-size:48px;">Premium<br><em>Trousers</em></h2>
          <p class="cat-desc" style="color:rgba(255,255,255,0.6);margin-bottom:20px;">Tailored trousers that complete the look. From slim-cut formals to relaxed chinos — every pair is crafted to move with you through your day.</p>
          <a class="cat-btn" style="color:var(--white);border-color:var(--gold);">Shop Trousers →</a>
        </div>
        <span class="cat-num">06</span>
      </div>
      <div class="cat-pants-side">
        <div class="cat-pants-side-top">
          <div class="stat-num">6</div>
          <div class="stat-label">Collections Available</div>
        </div>
        <div class="cat-pants-side-bottom">
          <div class="stat-num" style="color:var(--black);">৳</div>
          <div class="stat-label-dark" style="margin-bottom:16px;">Affordable Premium Pricing</div>
          <p style="font-size:12px;color:var(--gray);line-height:1.7;">Slim Fit · Regular Fit<br>Chinos · Formal Trousers<br>Cargo · Jogger</p>
        </div>
      </div>
      <div class="cat-pants-side" style="border-left:0.5px solid var(--gray-light);">
        <div class="cat-pants-side-top" style="background:var(--gold);">
          <div class="stat-num" style="color:var(--black);">100%</div>
          <div class="stat-label" style="color:rgba(0,0,0,0.6);">Quality Guaranteed</div>
        </div>
        <div class="cat-pants-side-bottom">
          <p style="font-size:11px;letter-spacing:0.15em;text-transform:uppercase;color:var(--black);margin-bottom:12px;">Why Collar?</p>
          <p style="font-size:12px;color:var(--gray);line-height:1.8;">Premium fabric. Precise cut. Fair price. Built for the modern Bengali gentleman.</p>
        </div>
      </div>
    </div>

  </div>
</div>

<!-- ── FOOTER ── -->
<footer>
  <div class="footer-top">
    <div>
      <div class="footer-brand">COLLAR</div>
      <p class="footer-tagline">Premium men's fashion for the modern Bengali gentleman. Quality you can feel. Style you can own.</p>
    </div>
    <div>
      <div class="footer-col-title">Collections</div>
      <ul class="footer-links">
        <li><a href="#">Formal Shirts</a></li>
        <li><a href="#">Old Money</a></li>
        <li><a href="#">Polo Shirts</a></li>
        <li><a href="#">Drop Shoulder</a></li>
        <li><a href="#">T-Shirts</a></li>
        <li><a href="#">Trousers</a></li>
      </ul>
    </div>
    <div>
      <div class="footer-col-title">Company</div>
      <ul class="footer-links">
        <li><a href="#">About Us</a></li>
        <li><a href="#">Our Story</a></li>
        <li><a href="#">Lookbook</a></li>
        <li><a href="#">Contact</a></li>
      </ul>
    </div>
    <div>
      <div class="footer-col-title">Connect</div>
      <ul class="footer-links">
        <li><a href="#">Facebook</a></li>
        <li><a href="#">Instagram</a></li>
        <li><a href="#">WhatsApp</a></li>
      </ul>
    </div>
  </div>
  <div class="footer-bottom">
    <span class="footer-copy">© 2025 COLLAR. All rights reserved. Made in Bangladesh.</span>
    <span class="footer-copy">Tanjim · Bappi · Sadik</span>
  </div>
</footer>

</body>
</html>