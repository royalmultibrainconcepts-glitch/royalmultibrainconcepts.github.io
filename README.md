# royalmultibrainconcepts.github.io
My professional portolio
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Emmanuel Bangbolu Oduroye | Digital Marketing Professional</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,600;0,700;1,300;1,400&family=Plus+Jakarta+Sans:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
  :root {
    --gold: #C9A84C;
    --gold-light: #E4C97A;
    --dark: #0E0E0E;
    --dark2: #161616;
    --dark3: #1E1E1E;
    --muted: #888;
    --text: #E8E3DA;
    --text-dim: #A89F92;
  }

  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  html { scroll-behavior: smooth; }

  body {
    background: var(--dark);
    color: var(--text);
    font-family: 'Plus Jakarta Sans', sans-serif;
    font-weight: 300;
    line-height: 1.7;
    overflow-x: hidden;
  }

  /* NAV */
  nav {
    position: fixed;
    top: 0; left: 0; right: 0;
    z-index: 100;
    padding: 1.2rem 4rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
    background: rgba(14,14,14,0.85);
    backdrop-filter: blur(12px);
    border-bottom: 1px solid rgba(201,168,76,0.12);
  }

  .nav-logo {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.3rem;
    font-weight: 600;
    letter-spacing: 0.06em;
    color: var(--gold);
    text-decoration: none;
  }

  .nav-links { display: flex; gap: 2.5rem; list-style: none; }
  .nav-links a {
    color: var(--text-dim);
    text-decoration: none;
    font-size: 0.78rem;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    transition: color 0.3s;
  }
  .nav-links a:hover { color: var(--gold); }

  /* HERO */
  .hero {
    min-height: 100vh;
    display: flex;
    align-items: center;
    padding: 8rem 4rem 4rem;
    position: relative;
    overflow: hidden;
  }

  .hero::before {
    content: '';
    position: absolute;
    top: -20%;
    right: -10%;
    width: 700px;
    height: 700px;
    background: radial-gradient(circle, rgba(201,168,76,0.07) 0%, transparent 70%);
    pointer-events: none;
  }

  .hero::after {
    content: '';
    position: absolute;
    bottom: 0; left: 0; right: 0;
    height: 1px;
    background: linear-gradient(90deg, transparent, var(--gold), transparent);
    opacity: 0.3;
  }

  .hero-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 4rem;
    align-items: center;
    max-width: 1200px;
    margin: 0 auto;
    width: 100%;
  }

  .hero-tag {
    display: inline-block;
    font-size: 0.7rem;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: var(--gold);
    border: 1px solid rgba(201,168,76,0.4);
    padding: 0.4rem 1rem;
    margin-bottom: 1.8rem;
    opacity: 0;
    animation: fadeUp 0.8s 0.2s forwards;
  }

  .hero h1 {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(3rem, 6vw, 5.5rem);
    font-weight: 300;
    line-height: 1.05;
    letter-spacing: -0.01em;
    margin-bottom: 1.5rem;
    opacity: 0;
    animation: fadeUp 0.8s 0.4s forwards;
  }

  .hero h1 em {
    font-style: italic;
    color: var(--gold);
  }

  .hero-desc {
    font-size: 1rem;
    color: var(--text-dim);
    max-width: 440px;
    margin-bottom: 2.5rem;
    line-height: 1.8;
    opacity: 0;
    animation: fadeUp 0.8s 0.6s forwards;
  }

  .hero-ctas {
    display: flex;
    gap: 1rem;
    flex-wrap: wrap;
    opacity: 0;
    animation: fadeUp 0.8s 0.8s forwards;
  }

  .btn-primary {
    background: var(--gold);
    color: #0E0E0E;
    padding: 0.85rem 2rem;
    font-size: 0.8rem;
    font-weight: 600;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    text-decoration: none;
    transition: background 0.3s, transform 0.2s;
  }
  .btn-primary:hover { background: var(--gold-light); transform: translateY(-2px); }

  .btn-outline {
    border: 1px solid rgba(201,168,76,0.5);
    color: var(--gold);
    padding: 0.85rem 2rem;
    font-size: 0.8rem;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    text-decoration: none;
    transition: all 0.3s;
  }
  .btn-outline:hover { border-color: var(--gold); background: rgba(201,168,76,0.05); }

  .hero-visual {
    opacity: 0;
    animation: fadeIn 1.2s 0.5s forwards;
  }

  .hero-card {
    background: var(--dark3);
    border: 1px solid rgba(201,168,76,0.15);
    padding: 2.5rem;
    position: relative;
  }

  .hero-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0;
    width: 60px; height: 3px;
    background: var(--gold);
  }

  .stat-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 1.5rem;
    margin-top: 1.5rem;
  }

  .stat-item {}
  .stat-number {
    font-family: 'Cormorant Garamond', serif;
    font-size: 2.8rem;
    font-weight: 600;
    color: var(--gold);
    line-height: 1;
  }
  .stat-label {
    font-size: 0.72rem;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--text-dim);
    margin-top: 0.3rem;
  }

  .roles-list {
    display: flex;
    flex-direction: column;
    gap: 0.6rem;
  }

  .role-badge {
    display: inline-flex;
    align-items: center;
    gap: 0.6rem;
    font-size: 0.82rem;
    color: var(--text-dim);
  }

  .role-badge::before {
    content: '';
    width: 6px; height: 6px;
    background: var(--gold);
    border-radius: 50%;
    flex-shrink: 0;
  }

  /* SECTIONS */
  section {
    padding: 6rem 4rem;
    max-width: 1200px;
    margin: 0 auto;
  }

  .section-label {
    font-size: 0.68rem;
    letter-spacing: 0.25em;
    text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 0.8rem;
  }

  .section-title {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(2rem, 4vw, 3rem);
    font-weight: 300;
    line-height: 1.2;
    margin-bottom: 1rem;
  }

  .section-title em { font-style: italic; color: var(--gold); }

  .divider {
    width: 60px;
    height: 2px;
    background: var(--gold);
    margin: 1.5rem 0 3rem;
    opacity: 0.6;
  }

  /* ABOUT */
  .about-section { background: var(--dark2); padding: 6rem 0; }
  .about-inner {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 4rem;
    display: grid;
    grid-template-columns: 1.1fr 0.9fr;
    gap: 5rem;
    align-items: start;
  }

  .about-text p {
    color: var(--text-dim);
    margin-bottom: 1.2rem;
    font-size: 1rem;
    line-height: 1.9;
  }

  .about-text p strong { color: var(--text); font-weight: 500; }

  .certs-block { margin-top: 0.5rem; }

  .cert-item {
    display: flex;
    align-items: flex-start;
    gap: 1rem;
    padding: 1rem 0;
    border-bottom: 1px solid rgba(255,255,255,0.06);
  }

  .cert-icon {
    width: 36px; height: 36px;
    border: 1px solid rgba(201,168,76,0.4);
    display: flex;
    align-items: center;
    justify-content: center;
    flex-shrink: 0;
    color: var(--gold);
    font-size: 0.9rem;
  }

  .cert-name {
    font-size: 0.88rem;
    color: var(--text);
    margin-bottom: 0.2rem;
    font-weight: 500;
  }

  .cert-issuer {
    font-size: 0.75rem;
    color: var(--text-dim);
    letter-spacing: 0.05em;
  }

  /* SKILLS */
  .skills-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(240px, 1fr));
    gap: 1.5rem;
  }

  .skill-card {
    background: var(--dark3);
    border: 1px solid rgba(255,255,255,0.06);
    padding: 1.8rem;
    transition: border-color 0.3s, transform 0.3s;
  }

  .skill-card:hover {
    border-color: rgba(201,168,76,0.3);
    transform: translateY(-4px);
  }

  .skill-icon {
    font-size: 1.6rem;
    margin-bottom: 1rem;
  }

  .skill-title {
    font-size: 0.9rem;
    font-weight: 500;
    margin-bottom: 0.5rem;
    color: var(--text);
  }

  .skill-desc {
    font-size: 0.78rem;
    color: var(--text-dim);
    line-height: 1.6;
  }

  /* EXPERIENCE */
  .exp-section { background: var(--dark2); padding: 6rem 0; }
  .exp-inner {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 4rem;
  }

  .timeline {
    position: relative;
    padding-left: 2rem;
  }

  .timeline::before {
    content: '';
    position: absolute;
    left: 0; top: 0; bottom: 0;
    width: 1px;
    background: linear-gradient(180deg, var(--gold) 0%, rgba(201,168,76,0.1) 100%);
  }

  .timeline-item {
    position: relative;
    padding: 0 0 3rem 2.5rem;
  }

  .timeline-item::before {
    content: '';
    position: absolute;
    left: -4px;
    top: 6px;
    width: 9px; height: 9px;
    background: var(--gold);
    border-radius: 50%;
    border: 2px solid var(--dark2);
    box-shadow: 0 0 0 2px rgba(201,168,76,0.3);
  }

  .timeline-period {
    font-size: 0.7rem;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 0.5rem;
  }

  .timeline-role {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.5rem;
    font-weight: 400;
    color: var(--text);
    margin-bottom: 0.3rem;
  }

  .timeline-company {
    font-size: 0.82rem;
    color: var(--text-dim);
    margin-bottom: 0.8rem;
    font-weight: 500;
    letter-spacing: 0.04em;
  }

  .timeline-company span {
    opacity: 0.6;
    font-weight: 300;
    padding-left: 0.4rem;
    margin-left: 0.4rem;
    border-left: 1px solid rgba(255,255,255,0.2);
  }

  .timeline-desc {
    font-size: 0.85rem;
    color: var(--text-dim);
    line-height: 1.7;
    max-width: 600px;
  }

  /* CONTACT */
  .contact-section {
    text-align: center;
    padding: 6rem 4rem;
    position: relative;
    overflow: hidden;
  }

  .contact-section::before {
    content: '';
    position: absolute;
    top: 50%; left: 50%;
    transform: translate(-50%, -50%);
    width: 600px; height: 600px;
    background: radial-gradient(circle, rgba(201,168,76,0.05) 0%, transparent 70%);
    pointer-events: none;
  }

  .contact-section .section-title { font-size: clamp(2.5rem, 5vw, 4rem); }

  .contact-email {
    display: inline-block;
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(1.2rem, 2.5vw, 1.8rem);
    color: var(--gold);
    text-decoration: none;
    border-bottom: 1px solid rgba(201,168,76,0.3);
    padding-bottom: 0.2rem;
    margin: 2rem 0;
    transition: border-color 0.3s;
  }

  .contact-email:hover { border-color: var(--gold); }

  .social-links {
    display: flex;
    gap: 1.5rem;
    justify-content: center;
    margin-top: 2rem;
    flex-wrap: wrap;
  }

  .social-link {
    display: inline-flex;
    align-items: center;
    gap: 0.5rem;
    font-size: 0.78rem;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: var(--text-dim);
    text-decoration: none;
    padding: 0.7rem 1.5rem;
    border: 1px solid rgba(255,255,255,0.1);
    transition: all 0.3s;
  }

  .social-link:hover {
    color: var(--gold);
    border-color: rgba(201,168,76,0.4);
  }

  /* FOOTER */
  footer {
    border-top: 1px solid rgba(255,255,255,0.06);
    padding: 2rem 4rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
    max-width: 100%;
    font-size: 0.75rem;
    color: var(--text-dim);
    letter-spacing: 0.05em;
  }

  footer .footer-name {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1rem;
    color: var(--gold);
  }

  /* ANIMATIONS */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(30px); }
    to { opacity: 1; transform: translateY(0); }
  }

  @keyframes fadeIn {
    from { opacity: 0; }
    to { opacity: 1; }
  }

  /* RESPONSIVE */
  @media (max-width: 900px) {
    nav { padding: 1.2rem 2rem; }
    .nav-links { gap: 1.5rem; }
    .hero, section { padding: 5rem 2rem; }
    .hero-grid { grid-template-columns: 1fr; }
    .hero-visual { display: none; }
    .about-inner { grid-template-columns: 1fr; padding: 0 2rem; gap: 3rem; }
    .exp-inner { padding: 0 2rem; }
    footer { padding: 1.5rem 2rem; flex-direction: column; gap: 0.5rem; text-align: center; }
    .contact-section { padding: 5rem 2rem; }
  }

  @media (max-width: 600px) {
    .nav-links { display: none; }
    .hero h1 { font-size: 2.5rem; }
    .stat-grid { grid-template-columns: 1fr 1fr; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <a class="nav-logo" href="#">E.B.O.</a>
  <ul class="nav-links">
    <li><a href="#about">About</a></li>
    <li><a href="#skills">Skills</a></li>
    <li><a href="#experience">Experience</a></li>
    <li><a href="#education">Education</a></li><li><a href="#interests">Interests</a></li><li><a href="#contact">Contact</a></li>
  </ul>
</nav>

<!-- HERO -->
<section class="hero" id="home" style="padding-top:8rem; max-width:100%;">
  <div class="hero-grid">
    <div class="hero-content">
      <span class="hero-tag">Digital Marketing Professional · Lagos, Nigeria</span>
      <h1>Emmanuel<br><em>Bangbolu</em><br>Oduroye</h1>
      <p class="hero-desc">
        A results-driven digital marketing strategist with over a decade of experience in social media management, SEO, web analytics, and brand growth across healthcare, real estate, and corporate sectors.
      </p>
      <div class="hero-ctas">
        <a href="#experience" class="btn-primary">View Experience</a>
        <a href="#contact" class="btn-outline">Get In Touch</a>
      </div>
    </div>

    <div class="hero-visual">
      <div class="hero-card" style="padding:0;overflow:hidden;">
        <div style="display:flex;align-items:stretch;gap:0;">
          <div style="flex-shrink:0;width:160px;">
            <img src="data:image/jpeg;base64,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H9iad/z7/wDj7f40UUAH9iad/wA+/wD4+3+NH9iad/z7/wDj7f40UUAH9iad/wA+/wD4+3+NH9iad/z7/wDj7f40UUAH9iad/wA+/wD4+3+NH9iad/z7/wDj7f40UUAH9iad/wA+/wD4+3+NH9iad/z7/wDj7f40UUAH9iad/wA+/wD4+3+NH9iad/z7/wDj7f40UUAH9iad/wA+/wD4+3+NH9iad/z7/wDj7f40UUAH9iad/wA+/wD4+3+NH9iad/z7/wDj7f40UUAH9iad/wA+/wD4+3+NH9iad/z7/wDj7f40UUAH9iad/wA+/wD4+3+NH9iad/z7/wDj7f40UUAH9iad/wA+/wD4+3+NH9iad/z7/wDj7f40UUAH9iad/wA+/wD4+3+NH9iad/z7/wDj7f40UUAH9iad/wA+/wD4+3+NH9iad/z7/wDj7f40UUAH9iad/wA+/wD4+3+NH9iad/z7/wDj7f40UUAH9iad/wA+/wD4+3+NH9iad/z7/wDj7f40UUAH9iad/wA+/wD4+3+NH9iad/z7/wDj7f40UUAH9iad/wA+/wD4+3+NH9iad/z7/wDj7f40UUAH9iad/wA+/wD4+3+NH9iad/z7/wDj7f40UUAH9iad/wA+/wD4+3+NbunadaxWEaJFhRnA3H1PvRRQB//Z" alt="Emmanuel Bangbolu Oduroye" style="width:160px;height:100%;object-fit:cover;object-position:top;display:block;min-height:340px;" />
          </div>
          <div style="padding:2rem 1.8rem;flex:1;">
            <p style="font-size:0.65rem;letter-spacing:0.18em;text-transform:uppercase;color:var(--gold);margin-bottom:1rem;">Professional Overview</p>
            <div class="roles-list" style="margin-bottom:1.4rem;">
              <span class="role-badge">Digital Marketer</span>
              <span class="role-badge">Social Media Manager</span>
              <span class="role-badge">Website Designer & Manager</span>
              <span class="role-badge">SEO Specialist</span>
              <span class="role-badge">Web Analytics Expert</span>
            </div>
            <div style="border-top:1px solid rgba(201,168,76,0.15);padding-top:1rem;">
              <p style="font-size:0.65rem;letter-spacing:0.18em;text-transform:uppercase;color:var(--gold);margin-bottom:0.8rem;">Contact</p>
              <div style="display:flex;flex-direction:column;gap:0.45rem;">
                <a href="tel:+2348036074999" style="color:var(--text-dim);text-decoration:none;font-size:0.78rem;display:flex;align-items:center;gap:0.5rem;">
                  <span style="color:var(--gold);">📞</span> +234 803 607 4999
                </a>
                <a href="tel:+2348091126935" style="color:var(--text-dim);text-decoration:none;font-size:0.78rem;display:flex;align-items:center;gap:0.5rem;">
                  <span style="color:var(--gold);">📞</span> +234 809 112 6935
                </a>
                <a href="https://wa.me/2348036074999" target="_blank" style="color:var(--text-dim);text-decoration:none;font-size:0.78rem;display:flex;align-items:center;gap:0.5rem;">
                  <span style="color:var(--gold);">💬</span> WhatsApp
                </a>
                <a href="/cdn-cgi/l/email-protection#0a6f24656e7f7865736f4a6d676b636624696567" style="color:var(--text-dim);text-decoration:none;font-size:0.78rem;display:flex;align-items:center;gap:0.5rem;">
                  <span style="color:var(--gold);">✉</span> <span class="__cf_email__" data-cfemail="60054e0f0415120f190520070d01090c4e030f0d">[email&#160;protected]</span>
                </a>
                <a href="https://www.linkedin.com/in/emmanuel-oduroye-30359887//" target="_blank" style="color:var(--text-dim);text-decoration:none;font-size:0.78rem;display:flex;align-items:center;gap:0.5rem;">
                  <span style="color:var(--gold);">🔗</span> LinkedIn Profile
                </a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ABOUT -->
<div class="about-section" id="about">
  <div class="about-inner">
    <div class="about-text">
      <p class="section-label">About Me</p>
      <h2 class="section-title">Marketing That <em>Moves</em> Businesses Forward</h2>
      <div class="divider"></div>
      <p>
        I am <strong>Emmanuel Bangbolu Oduroye</strong>, a dedicated and versatile digital marketing professional based in Lagos, Nigeria. With a career spanning over a decade, I have developed deep expertise in social media strategy, search engine optimisation, web analytics, and website management.
      </p>
      <p>
        My professional journey has taken me across diverse industries — from manufacturing and real estate to healthcare and corporate services — equipping me with an uncommon breadth of perspective on how brands communicate and grow in the digital space.
      </p>
      <p>
        I am passionate about crafting compelling digital narratives that connect with audiences and drive measurable results. Whether managing an organisation's online presence, optimising a website for search engines, or developing data-driven marketing strategies, I bring <strong>precision, creativity, and commitment</strong> to every engagement.
      </p>
    </div>

    <div class="certs-block">
      <p class="section-label" style="margin-bottom:1rem;">Certifications</p>
      <div class="cert-item">
        <div class="cert-icon">✦</div>
        <div>
          <div class="cert-name">Google Certified Digital Marketer</div>
          <div class="cert-issuer">Google — Professional Certification</div>
        </div>
      </div>
      <div class="cert-item">
        <div class="cert-icon">✦</div>
        <div>
          <div class="cert-name">Google Analytics Certification</div>
          <div class="cert-issuer">Google — Web Analytics</div>
        </div>
      </div>
      <div class="cert-item">
        <div class="cert-icon">✦</div>
        <div>
          <div class="cert-name">Google Adwords Certification</div>
          <div class="cert-issuer">Google — Search, Display, Mobile & Video Advertising</div>
        </div>
      </div>
      <div class="cert-item">
        <div class="cert-icon">✦</div>
        <div>
          <div class="cert-name">Social Media Marketing Certification</div>
          <div class="cert-issuer">Certified Professional</div>
        </div>
      </div>
      <div class="cert-item">
        <div class="cert-icon">✦</div>
        <div>
          <div class="cert-name">Cisco Certified Network Associate (CCNA)</div>
          <div class="cert-issuer">Cisco — In View</div>
        </div>
      </div>
    </div>
  </div>
</div>

<!-- SKILLS -->
<section id="skills">
  <p class="section-label">What I Do</p>
  <h2 class="section-title">Core <em>Skills</em> & Expertise</h2>
  <div class="divider"></div>

  <div class="skills-grid">
    <div class="skill-card">
      <div class="skill-icon">📈</div>
      <div class="skill-title">Digital Marketing Strategy</div>
      <div class="skill-desc">Formulation and execution of integrated digital marketing plans, online campaigns, and strategies aligned to business goals.</div>
    </div>
    <div class="skill-card">
      <div class="skill-icon">🔍</div>
      <div class="skill-title">Google SEO & Adwords</div>
      <div class="skill-desc">Google-certified expertise in Search, Display, Mobile and Video advertising campaigns, keyword strategy, and organic search optimisation.</div>
    </div>
    <div class="skill-card">
      <div class="skill-icon">📊</div>
      <div class="skill-title">Google Analytics & Web Analytics</div>
      <div class="skill-desc">Certified in Google Analytics — tracking website traffic, user behaviour, performance metrics, and converting data into actionable insights.</div>
    </div>
    <div class="skill-card">
      <div class="skill-icon">📱</div>
      <div class="skill-title">Social Media Management</div>
      <div class="skill-desc">Creating and managing multi-platform social media accounts, content calendars, community engagement, and paid social promotions.</div>
    </div>
    <div class="skill-card">
      <div class="skill-icon">🌐</div>
      <div class="skill-title">Website Design & Management</div>
      <div class="skill-desc">Proficient in WordPress and Joomla CMS for professional website design, content management, and ongoing site management.</div>
    </div>
    <div class="skill-card">
      <div class="skill-icon">💼</div>
      <div class="skill-title">Microsoft Office Suite</div>
      <div class="skill-desc">Over 8 years of expert-level proficiency in Word, Excel, PowerPoint, and Outlook for business reporting and communications.</div>
    </div>
    <div class="skill-card">
      <div class="skill-icon">📋</div>
      <div class="skill-title">Data Analysis</div>
      <div class="skill-desc">Compilation, sorting, and analysis of business data to support decision-making, reporting, and performance improvement.</div>
    </div>
    <div class="skill-card">
      <div class="skill-icon">🤝</div>
      <div class="skill-title">Client Relationship Management</div>
      <div class="skill-desc">Building strong client relationships, managing accounts, recovering lapsed clients, and growing customer bases across organisations.</div>
    </div>
    <div class="skill-card">
      <div class="skill-icon">🚗</div>
      <div class="skill-title">Operations & Administration</div>
      <div class="skill-desc">Insurance underwriting, office management, admin support, driving (10+ years), and organisational leadership experience.</div>
    </div>
  </div>
</section>

<!-- EXPERIENCE -->
<div class="exp-section" id="experience">
  <div class="exp-inner">
    <p class="section-label">Career Journey</p>
    <h2 class="section-title">Professional <em>Experience</em></h2>
    <div class="divider"></div>

    <div class="timeline">

      <div class="timeline-item">
        <div class="timeline-period">2025 – Present</div>
        <div class="timeline-role">Website Manager & Social Media Manager</div>
        <div class="timeline-company">Cityview Hospital <span>11a Nob-Oluwa Street, Ogba, Lagos</span></div>
        <div class="timeline-desc">Overseeing the hospital's digital presence through strategic website management and active social media engagement, enhancing brand visibility and patient communication in the healthcare sector.</div>
      </div>

      <div class="timeline-item">
        <div class="timeline-period">2021 – 2025</div>
        <div class="timeline-role">Social Media Marketer</div>
        <div class="timeline-company">Shineway Healthcare Limited <span>3/5 Owoduni Street, Allen Avenue, Ikeja, Lagos</span></div>
        <div class="timeline-desc">Drove healthcare brand awareness and audience engagement through targeted social media campaigns, content creation, and digital marketing strategies across multiple platforms.</div>
      </div>

      <div class="timeline-item">
        <div class="timeline-period">2019 – 2021</div>
        <div class="timeline-role">Country Representative</div>
        <div class="timeline-company">Swisderm International <span>3/5 Joseph Odunlami Street, Ogba, Lagos</span></div>
        <div class="timeline-desc">Served as the country representative, leading business development, brand promotion, and market expansion initiatives for the organisation within Nigeria.</div>
      </div>

      <div class="timeline-item">
        <div class="timeline-period">2018 – 2019</div>
        <div class="timeline-role">Administrative Assistant</div>
        <div class="timeline-company">Dapo Ransome-Kuti & Associates <span>Lagos</span></div>
        <div class="timeline-desc">Provided administrative and operational support while contributing to marketing communications and client relationship functions.</div>
      </div>

      <div class="timeline-item">
        <div class="timeline-period">Dec 2017 – 2018</div>
        <div class="timeline-role">Digital Marketing Manager</div>
        <div class="timeline-company">CareAfric Group of Companies Ltd. <span>Balogun Market, Trade Fair, Lagos</span></div>
        <div class="timeline-desc">Formulated digital marketing plans and strategies; promoted company products and services online; created and managed the company's social media accounts, website, and blogs across all digital platforms.</div>
      </div>

      <div class="timeline-item">
        <div class="timeline-period">Oct 2015 – Nov 2017</div>
        <div class="timeline-role">General Manager</div>
        <div class="timeline-company">Victory Concepts Enterprises <span>3, Oduroye Street, Aguda, Ogba, Ikeja, Lagos</span></div>
        <div class="timeline-desc">Managed the company's social media accounts, promoted products via Google and social media platforms, and ensured the achievement of all digital marketing goals.</div>
      </div>

      <div class="timeline-item">
        <div class="timeline-period">Apr 2014 – Aug 2015</div>
        <div class="timeline-role">Data Analyst</div>
        <div class="timeline-company">Kind David II Ltd. <span>Ogundele Avenue, Oke-Ira, Aguda-Ogba, Ikeja, Lagos</span></div>
        <div class="timeline-desc">Responsible for compilation, typing, sorting, and analysis of business data. Consistently exceeded monthly targets by processing more files than required and ensuring data accuracy.</div>
      </div>

      <div class="timeline-item">
        <div class="timeline-period">Feb 2013 – Apr 2014</div>
        <div class="timeline-role">Client Service Officer</div>
        <div class="timeline-company">MET Pneumatics Nigeria Ltd. <span>601, Agege Oshodi Expressway, Shogunle, Lagos</span></div>
        <div class="timeline-desc">Marketed and supplied company products, successfully convinced former clients to return, significantly increased territory revenue by growing the client base, and generated new leads for the company.</div>
      </div>

      <div class="timeline-item">
        <div class="timeline-period">2002 – 2012</div>
        <div class="timeline-role">Admin Manager</div>
        <div class="timeline-company">Lagoon Insurance Brokers Ltd. <span>12, Beach Road, Jos</span></div>
        <div class="timeline-desc">Managed insurance policy underwriting and day-to-day office operations; improved the company's filing system; grew the customer base; ensured prompt processing and delivery of policy documents and prompt settlement of customer claims.</div>
      </div>

      <div class="timeline-item">
        <div class="timeline-period">1998 – 1999</div>
        <div class="timeline-role">Marketing Executive</div>
        <div class="timeline-company">Richbol Cleaning Services Ltd. <span>Ojodu, Lagos</span></div>
        <div class="timeline-desc">Marketed the company's cleaning services across designated locations, successfully canvassing improved patronage and expanding the company's client base.</div>
      </div>

      <div class="timeline-item" style="padding-bottom:0;">
        <div class="timeline-period">1996 – 1998</div>
        <div class="timeline-role">Factory Worker / Supervisor</div>
        <div class="timeline-company">Western Metal Company Ltd. <span>Wemco Road, Industrial Estate, Ikeja, Lagos</span></div>
        <div class="timeline-desc">Supervised the sorting of veneer for the manufacturing of plywood, ensuring quality control and meeting production targets in a fast-paced manufacturing environment.</div>
      </div>

    </div>
  </div>
</div>

<!-- EDUCATION -->
<div class="about-section" id="education" style="padding:6rem 0;">
  <div class="about-inner" style="grid-template-columns:1fr;">
    <div>
      <p class="section-label">Academic Background</p>
      <h2 class="section-title">Education & <em>Qualifications</em></h2>
      <div class="divider"></div>
      <div style="display:grid;grid-template-columns:repeat(auto-fill,minmax(300px,1fr));gap:1.5rem;margin-top:1rem;">

        <div class="skill-card" style="padding:2rem;border-left:3px solid var(--gold);">
          <div style="font-size:0.68rem;letter-spacing:0.15em;text-transform:uppercase;color:var(--gold);margin-bottom:0.5rem;">2023</div>
          <div style="font-family:'Cormorant Garamond',serif;font-size:1.3rem;font-weight:400;color:var(--text);margin-bottom:0.4rem;">BSc Computer Science</div>
          <div style="font-size:0.82rem;font-weight:500;color:var(--text-dim);margin-bottom:0.3rem;">International University of Management and Administration</div>
          <div style="font-size:0.75rem;color:var(--muted);letter-spacing:0.04em;">Republic of Benin</div>
        </div>

        <div class="skill-card" style="padding:2rem;border-left:3px solid var(--gold);">
          <div style="font-size:0.68rem;letter-spacing:0.15em;text-transform:uppercase;color:var(--gold);margin-bottom:0.5rem;">2008</div>
          <div style="font-family:'Cormorant Garamond',serif;font-size:1.3rem;font-weight:400;color:var(--text);margin-bottom:0.4rem;">Higher National Diploma</div>
          <div style="font-size:0.82rem;font-weight:500;color:var(--text-dim);margin-bottom:0.3rem;">Business Administration and Management</div>
          <div style="font-size:0.75rem;color:var(--muted);letter-spacing:0.04em;">Rufus Giwa Polytechnic, Owo, Nigeria</div>
        </div>

        <div class="skill-card" style="padding:2rem;border-left:3px solid var(--gold);">
          <div style="font-size:0.68rem;letter-spacing:0.15em;text-transform:uppercase;color:var(--gold);margin-bottom:0.5rem;">2006</div>
          <div style="font-family:'Cormorant Garamond',serif;font-size:1.3rem;font-weight:400;color:var(--text);margin-bottom:0.4rem;">National Diploma</div>
          <div style="font-size:0.82rem;font-weight:500;color:var(--text-dim);margin-bottom:0.3rem;">Business Administration and Management</div>
          <div style="font-size:0.75rem;color:var(--muted);letter-spacing:0.04em;">Rufus Giwa Polytechnic, Owo, Nigeria</div>
        </div>

      </div>
    </div>
  </div>
</div>

<!-- INTERESTS -->
<section id="interests" style="padding-top:2rem; padding-bottom:2rem;">
  <p class="section-label">Beyond Work</p>
  <h2 class="section-title">Interests & <em>Activities</em></h2>
  <div class="divider"></div>
  <div style="display:flex;flex-wrap:wrap;gap:1rem;margin-bottom:2.5rem;">
    <span style="padding:0.6rem 1.4rem;border:1px solid rgba(201,168,76,0.3);font-size:0.8rem;color:var(--text-dim);">📚 Reading</span>
    <span style="padding:0.6rem 1.4rem;border:1px solid rgba(201,168,76,0.3);font-size:0.8rem;color:var(--text-dim);">⚽ Soccer</span>
    <span style="padding:0.6rem 1.4rem;border:1px solid rgba(201,168,76,0.3);font-size:0.8rem;color:var(--text-dim);">🏓 Table Tennis</span>
    <span style="padding:0.6rem 1.4rem;border:1px solid rgba(201,168,76,0.3);font-size:0.8rem;color:var(--text-dim);">🎬 Watching Movies</span>
    <span style="padding:0.6rem 1.4rem;border:1px solid rgba(201,168,76,0.3);font-size:0.8rem;color:var(--text-dim);">🎹 Music (Keyboard)</span>
    <span style="padding:0.6rem 1.4rem;border:1px solid rgba(201,168,76,0.3);font-size:0.8rem;color:var(--text-dim);">🏕️ Boys Scout of Nigeria — Cub Scout Leader</span>
    <span style="padding:0.6rem 1.4rem;border:1px solid rgba(201,168,76,0.3);font-size:0.8rem;color:var(--text-dim);">🎖️ Man O' War — Citizenship & Leadership Training</span>
  </div>
</section>

<!-- CONTACT -->
<section class="contact-section" id="contact" style="max-width:100%;">
  <p class="section-label">Let's Work Together</p>
  <h2 class="section-title">Ready to <em>Grow</em> Your Brand?</h2>
  <div class="divider" style="margin: 1.5rem auto 2rem;"></div>
  <p style="color:var(--text-dim); max-width:500px; margin: 0 auto; font-size:0.95rem;">
    Whether you need a digital marketing strategy, social media management, SEO, or a new website — I'm available to bring your vision to life.
  </p>

  <div class="social-links" style="margin-top: 3rem;">
    <a href="https://www.linkedin.com/in/emmanuel-bangbolu-oduroye" target="_blank" class="social-link">
      <svg width="14" height="14" viewBox="0 0 24 24" fill="currentColor"><path d="M19 3a2 2 0 0 1 2 2v14a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V5a2 2 0 0 1 2-2h14m-.5 15.5v-5.3a3.26 3.26 0 0 0-3.26-3.26c-.85 0-1.84.52-2.32 1.3v-1.11h-2.79v8.37h2.79v-4.93c0-.77.62-1.4 1.39-1.4a1.4 1.4 0 0 1 1.4 1.4v4.93h2.79M6.88 8.56a1.68 1.68 0 0 0 1.68-1.68c0-.93-.75-1.69-1.68-1.69a1.69 1.69 0 0 0-1.69 1.69c0 .93.76 1.68 1.69 1.68m1.39 9.94v-8.37H5.5v8.37h2.77z"/></svg>
      LinkedIn
    </a>
    <a href="https://www.indeed.com/r/Emmanuel-Bangbolu-Oduroye" target="_blank" class="social-link">
      <svg width="14" height="14" viewBox="0 0 24 24" fill="currentColor"><path d="M10.5 2a8.5 8.5 0 1 0 0 17A8.5 8.5 0 0 0 10.5 2zm0 15a6.5 6.5 0 1 1 0-13 6.5 6.5 0 0 1 0 13zm8.3 2.3l-3.7-3.7a1 1 0 1 0-1.4 1.4l3.7 3.7a1 1 0 1 0 1.4-1.4z"/></svg>
      Indeed Profile
    </a>
    <a href="/cdn-cgi/l/email-protection#ceaba3a3afa0bbaba2acafa0a9aca1a2bb8ea9a3afa7a2e0ada1a3" class="social-link">
      <svg width="14" height="14" viewBox="0 0 24 24" fill="currentColor"><path d="M20 4H4c-1.1 0-2 .9-2 2v12c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V6c0-1.1-.9-2-2-2zm0 4l-8 5-8-5V6l8 5 8-5v2z"/></svg>
      Email Me
    </a>
  </div>
  <p style="font-size:0.72rem; color:var(--muted); margin-top:1.5rem; letter-spacing:0.05em;">Lagos, Nigeria · Open to remote & hybrid opportunities</p
