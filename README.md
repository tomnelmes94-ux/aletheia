[index.html](https://github.com/user-attachments/files/26286996/index.html)
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Aletheia — Intelligence Grounded in Truth</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,600;1,300;1,400&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet">
<style>
  :root {
    --navy: #0B1628;
    --navy-mid: #112240;
    --navy-light: #1A3258;
    --gold: #C9A84C;
    --gold-light: #E8C97A;
    --gold-pale: #F5E6C0;
    --cream: #F8F5EE;
    --white: #FFFFFF;
    --text-muted: #8A9BB5;
    --border: rgba(201, 168, 76, 0.18);
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  html { scroll-behavior: smooth; }

  body {
    background: var(--navy);
    color: var(--cream);
    font-family: 'DM Sans', sans-serif;
    font-weight: 300;
    line-height: 1.7;
    -webkit-font-smoothing: antialiased;
  }

  /* ─── HEADER ─── */
  header {
    position: fixed;
    top: 0; left: 0; right: 0;
    z-index: 100;
    padding: 24px 48px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    background: rgba(11, 22, 40, 0.92);
    backdrop-filter: blur(12px);
    border-bottom: 1px solid var(--border);
  }

  .logo {
    font-family: 'Cormorant Garamond', serif;
    font-size: 22px;
    font-weight: 600;
    letter-spacing: 0.12em;
    color: var(--cream);
    text-decoration: none;
    text-transform: uppercase;
  }

  .logo span {
    color: var(--gold);
  }

  nav {
    display: flex;
    gap: 40px;
    align-items: center;
  }

  nav a {
    font-size: 13px;
    font-weight: 400;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    color: var(--text-muted);
    text-decoration: none;
    transition: color 0.2s;
  }

  nav a:hover { color: var(--gold-light); }

  .nav-cta {
    padding: 9px 22px;
    border: 1px solid var(--gold);
    color: var(--gold) !important;
    border-radius: 2px;
    font-size: 12px !important;
    letter-spacing: 0.1em;
    transition: all 0.2s !important;
  }

  .nav-cta:hover {
    background: var(--gold) !important;
    color: var(--navy) !important;
  }

  /* ─── HERO ─── */
  .hero {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding: 140px 48px 100px;
    position: relative;
    overflow: hidden;
  }

  .hero::before {
    content: '';
    position: absolute;
    top: -200px; right: -200px;
    width: 700px; height: 700px;
    background: radial-gradient(circle, rgba(201, 168, 76, 0.06) 0%, transparent 70%);
    pointer-events: none;
  }

  .hero::after {
    content: '';
    position: absolute;
    bottom: -100px; left: -100px;
    width: 500px; height: 500px;
    background: radial-gradient(circle, rgba(26, 50, 88, 0.8) 0%, transparent 70%);
    pointer-events: none;
  }

  .hero-label {
    font-size: 11px;
    font-weight: 500;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 32px;
    opacity: 0;
    animation: fadeUp 0.8s ease 0.2s forwards;
  }

  .hero-headline {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(48px, 8vw, 96px);
    font-weight: 300;
    line-height: 1.05;
    letter-spacing: -0.01em;
    color: var(--cream);
    max-width: 900px;
    margin-bottom: 40px;
    opacity: 0;
    animation: fadeUp 0.8s ease 0.4s forwards;
  }

  .hero-headline em {
    font-style: italic;
    color: var(--gold-light);
  }

  .hero-sub {
    font-size: 18px;
    font-weight: 300;
    color: var(--text-muted);
    max-width: 580px;
    line-height: 1.75;
    margin-bottom: 56px;
    opacity: 0;
    animation: fadeUp 0.8s ease 0.6s forwards;
  }

  .hero-actions {
    display: flex;
    gap: 20px;
    align-items: center;
    opacity: 0;
    animation: fadeUp 0.8s ease 0.8s forwards;
  }

  .btn-primary {
    padding: 14px 32px;
    background: var(--gold);
    color: var(--navy);
    font-size: 13px;
    font-weight: 500;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    text-decoration: none;
    border-radius: 2px;
    transition: all 0.2s;
  }

  .btn-primary:hover {
    background: var(--gold-light);
    transform: translateY(-1px);
  }

  .btn-ghost {
    padding: 14px 32px;
    border: 1px solid rgba(201, 168, 76, 0.3);
    color: var(--cream);
    font-size: 13px;
    font-weight: 400;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    text-decoration: none;
    border-radius: 2px;
    transition: all 0.2s;
  }

  .btn-ghost:hover {
    border-color: var(--gold);
    color: var(--gold-light);
  }

  /* ─── DIVIDER ─── */
  .gold-line {
    width: 100%;
    height: 1px;
    background: linear-gradient(90deg, transparent, var(--gold), transparent);
    opacity: 0.3;
    margin: 0 48px;
    width: calc(100% - 96px);
  }

  /* ─── MISSION ─── */
  .mission {
    padding: 100px 48px;
    max-width: 1100px;
    margin: 0 auto;
  }

  .section-label {
    font-size: 11px;
    font-weight: 500;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 24px;
  }

  .mission-statement {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(28px, 4vw, 48px);
    font-weight: 300;
    line-height: 1.35;
    color: var(--cream);
    max-width: 860px;
    margin-bottom: 48px;
  }

  .mission-statement em {
    font-style: italic;
    color: var(--gold-light);
  }

  .mission-body {
    font-size: 16px;
    color: var(--text-muted);
    max-width: 640px;
    line-height: 1.8;
  }

  /* ─── PILLARS ─── */
  .pillars {
    padding: 80px 48px;
    background: var(--navy-mid);
    border-top: 1px solid var(--border);
    border-bottom: 1px solid var(--border);
  }

  .pillars-inner {
    max-width: 1100px;
    margin: 0 auto;
  }

  .pillars-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 2px;
    margin-top: 56px;
  }

  .pillar {
    padding: 48px 40px;
    background: var(--navy);
    border: 1px solid var(--border);
    transition: border-color 0.3s;
    position: relative;
    overflow: hidden;
  }

  .pillar::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 2px;
    background: var(--gold);
    transform: scaleX(0);
    transition: transform 0.3s;
    transform-origin: left;
  }

  .pillar:hover::before { transform: scaleX(1); }
  .pillar:hover { border-color: rgba(201, 168, 76, 0.35); }

  .pillar-number {
    font-family: 'Cormorant Garamond', serif;
    font-size: 48px;
    font-weight: 300;
    color: rgba(201, 168, 76, 0.2);
    line-height: 1;
    margin-bottom: 20px;
  }

  .pillar h3 {
    font-family: 'Cormorant Garamond', serif;
    font-size: 24px;
    font-weight: 400;
    color: var(--cream);
    margin-bottom: 14px;
    letter-spacing: 0.02em;
  }

  .pillar p {
    font-size: 14px;
    color: var(--text-muted);
    line-height: 1.75;
  }

  /* ─── WORK ─── */
  .work {
    padding: 100px 48px;
    max-width: 1100px;
    margin: 0 auto;
  }

  .work-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 2px;
    margin-top: 56px;
  }

  .work-item {
    padding: 48px;
    border: 1px solid var(--border);
    background: var(--navy-mid);
    transition: all 0.3s;
    position: relative;
  }

  .work-item:hover {
    background: var(--navy-light);
    border-color: rgba(201, 168, 76, 0.35);
  }

  .work-tag {
    display: inline-block;
    font-size: 10px;
    font-weight: 500;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: var(--gold);
    border: 1px solid rgba(201, 168, 76, 0.3);
    padding: 4px 10px;
    border-radius: 2px;
    margin-bottom: 24px;
  }

  .work-tag.coming-soon {
    color: var(--text-muted);
    border-color: rgba(138, 155, 181, 0.2);
  }

  .work-item h3 {
    font-family: 'Cormorant Garamond', serif;
    font-size: 28px;
    font-weight: 400;
    color: var(--cream);
    margin-bottom: 16px;
    line-height: 1.2;
  }

  .work-item p {
    font-size: 14px;
    color: var(--text-muted);
    line-height: 1.75;
    margin-bottom: 28px;
  }

  .work-link {
    font-size: 12px;
    font-weight: 500;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--gold);
    text-decoration: none;
    display: inline-flex;
    align-items: center;
    gap: 8px;
    transition: gap 0.2s;
  }

  .work-link:hover { gap: 14px; }

  .work-link-muted {
    font-size: 12px;
    font-weight: 400;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    color: var(--text-muted);
    display: inline-flex;
    align-items: center;
    gap: 8px;
  }

  /* ─── HUMANITARIAN ─── */
  .humanitarian {
    padding: 100px 48px;
    background: linear-gradient(135deg, var(--navy-mid) 0%, var(--navy) 100%);
    border-top: 1px solid var(--border);
    border-bottom: 1px solid var(--border);
    position: relative;
    overflow: hidden;
  }

  .humanitarian::before {
    content: '';
    position: absolute;
    top: 50%; right: -100px;
    transform: translateY(-50%);
    width: 400px; height: 400px;
    background: radial-gradient(circle, rgba(201, 168, 76, 0.05) 0%, transparent 70%);
  }

  .humanitarian-inner {
    max-width: 1100px;
    margin: 0 auto;
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 80px;
    align-items: center;
  }

  .humanitarian h2 {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(32px, 4vw, 52px);
    font-weight: 300;
    line-height: 1.2;
    color: var(--cream);
    margin-bottom: 28px;
  }

  .humanitarian h2 em {
    font-style: italic;
    color: var(--gold-light);
  }

  .humanitarian p {
    font-size: 15px;
    color: var(--text-muted);
    line-height: 1.85;
    margin-bottom: 20px;
  }

  .humanitarian-commitments {
    display: flex;
    flex-direction: column;
    gap: 20px;
  }

  .commitment {
    padding: 24px 28px;
    border: 1px solid var(--border);
    border-left: 3px solid var(--gold);
    background: rgba(11, 22, 40, 0.6);
  }

  .commitment h4 {
    font-size: 14px;
    font-weight: 500;
    color: var(--cream);
    margin-bottom: 8px;
    letter-spacing: 0.03em;
  }

  .commitment p {
    font-size: 13px;
    color: var(--text-muted);
    line-height: 1.65;
    margin-bottom: 0;
  }

  /* ─── CONTACT ─── */
  .contact {
    padding: 100px 48px;
    max-width: 1100px;
    margin: 0 auto;
    text-align: center;
  }

  .contact h2 {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(36px, 5vw, 64px);
    font-weight: 300;
    color: var(--cream);
    margin-bottom: 20px;
  }

  .contact h2 em {
    font-style: italic;
    color: var(--gold-light);
  }

  .contact p {
    font-size: 16px;
    color: var(--text-muted);
    max-width: 520px;
    margin: 0 auto 48px;
    line-height: 1.8;
  }

  .contact-email {
    font-family: 'Cormorant Garamond', serif;
    font-size: 24px;
    font-weight: 400;
    color: var(--gold-light);
    text-decoration: none;
    letter-spacing: 0.04em;
    border-bottom: 1px solid rgba(201, 168, 76, 0.3);
    padding-bottom: 4px;
    transition: border-color 0.2s;
  }

  .contact-email:hover {
    border-color: var(--gold);
  }

  /* ─── FOOTER ─── */
  footer {
    padding: 48px;
    border-top: 1px solid var(--border);
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .footer-logo {
    font-family: 'Cormorant Garamond', serif;
    font-size: 18px;
    font-weight: 600;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: var(--text-muted);
  }

  .footer-logo span { color: var(--gold); }

  .footer-copy {
    font-size: 12px;
    color: var(--text-muted);
    letter-spacing: 0.05em;
  }

  .footer-links {
    display: flex;
    gap: 32px;
  }

  .footer-links a {
    font-size: 12px;
    color: var(--text-muted);
    text-decoration: none;
    letter-spacing: 0.06em;
    text-transform: uppercase;
    transition: color 0.2s;
  }

  .footer-links a:hover { color: var(--gold-light); }

  /* ─── ANIMATIONS ─── */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(24px); }
    to { opacity: 1; transform: translateY(0); }
  }

  .fade-in {
    opacity: 0;
    transform: translateY(20px);
    transition: opacity 0.7s ease, transform 0.7s ease;
  }

  .fade-in.visible {
    opacity: 1;
    transform: translateY(0);
  }

  /* ─── MOBILE ─── */
  @media (max-width: 768px) {
    header { padding: 20px 24px; }
    nav { display: none; }
    .hero { padding: 120px 24px 80px; }
    .mission, .work, .contact { padding: 64px 24px; }
    .pillars { padding: 64px 24px; }
    .humanitarian { padding: 64px 24px; }
    .humanitarian-inner { grid-template-columns: 1fr; gap: 48px; }
    .work-grid { grid-template-columns: 1fr; }
    footer { padding: 32px 24px; flex-direction: column; gap: 20px; text-align: center; }
    .footer-links { display: none; }
  }
</style>
</head>
<body>

<!-- HEADER -->
<header>
  <a href="#" class="logo">Aletheia<span>FI</span></a>
  <nav>
    <a href="#mission">Mission</a>
    <a href="#work">Work</a>
    <a href="#humanitarian">Purpose</a>
    <a href="#contact" class="nav-cta">Contact</a>
  </nav>
</header>

<!-- HERO -->
<section class="hero">
  <div class="hero-label">Intelligence Grounded in Truth</div>
  <h1 class="hero-headline">
    Technology for a <em>prosperous,<br>healthy,</em> and equal future.
  </h1>
  <p class="hero-sub">
    We believe technology — applied safely and with purpose — can lift every person. Aletheia builds intelligence systems that are verified, trustworthy, and built to serve humanity, not exploit it.
  </p>
  <div class="hero-actions">
    <a href="#work" class="btn-primary">Our Work</a>
    <a href="#contact" class="btn-ghost">Get in Touch</a>
  </div>
</section>

<div class="gold-line"></div>

<!-- MISSION -->
<section class="mission" id="mission">
  <div class="fade-in">
    <div class="section-label">Our Foundation</div>
    <p class="mission-statement">
      Aletheia means <em>truth</em> — the unconcealedness of reality. We named our company after it because everything we build rests on a single principle: intelligence that cannot be trusted is intelligence that cannot help.
    </p>
    <p class="mission-body">
      We are building across three domains — behavioral signal intelligence and cybersecurity, AI-powered business tools, and the foundational architecture for verified artificial intelligence. Each is connected by the same philosophy: verified, honest, and built to make the world more equal.
    </p>
  </div>
</section>

<!-- PILLARS -->
<section class="pillars">
  <div class="pillars-inner">
    <div class="section-label fade-in">What We Stand On</div>
    <div class="pillars-grid">
      <div class="pillar fade-in">
        <div class="pillar-number">01</div>
        <h3>Verified Truth</h3>
        <p>We do not build systems that simulate understanding and call it knowledge. Every claim our systems make should be traceable to a source that reality itself has confirmed.</p>
      </div>
      <div class="pillar fade-in">
        <div class="pillar-number">02</div>
        <h3>Safety by Design</h3>
        <p>Safety is not a feature added at the end. It is the architecture. We refuse applications we believe cause harm — regardless of what they pay.</p>
      </div>
      <div class="pillar fade-in">
        <div class="pillar-number">03</div>
        <h3>Equal Access</h3>
        <p>The most powerful tools in existence should not belong only to those who can afford them. Humanitarian organizations will always have access to our technology at no cost.</p>
      </div>
      <div class="pillar fade-in">
        <div class="pillar-number">04</div>
        <h3>Transparent Intent</h3>
        <p>We say what we are building and why. We do not use language designed to obscure our direction from those who fund us or those who depend on us.</p>
      </div>
    </div>
  </div>
</section>

<!-- WORK -->
<section class="work" id="work">
  <div class="fade-in">
    <div class="section-label">Our Work</div>
  </div>
  <div class="work-grid">
    <div class="work-item fade-in">
      <span class="work-tag">Available Now</span>
      <h3>ASGI White Paper</h3>
      <p>From Simulation to Verification — a philosophical and technical argument for reclassifying current AI systems and defining the path toward genuinely verified machine intelligence.</p>
      <a href="#contact" class="work-link">Request Paper →</a>
    </div>
    <div class="work-item fade-in">
      <span class="work-tag coming-soon">Coming Soon</span>
      <h3>Aletheia Fusion Intelligence</h3>
      <p>Behavioral detection and signal intelligence platform. On-premises, oracle-only architecture. Turns behavioral signal noise into verified incident intelligence for enterprise and law enforcement.</p>
      <span class="work-link-muted">In Development →</span>
    </div>
    <div class="work-item fade-in">
      <span class="work-tag coming-soon">Coming Soon</span>
      <h3>Sparta Business Suite</h3>
      <p>An AI-native business operating system. Your company's CFO, COO, accountant, project manager, and HR — in one proactive intelligence layer built for founders and enterprises alike.</p>
      <span class="work-link-muted">In Development →</span>
    </div>
    <div class="work-item fade-in">
      <span class="work-tag coming-soon">Coming Soon</span>
      <h3>Genesis Intelligence Ledger</h3>
      <p>The bridge from simulated to verified intelligence. A framework for grounding AI knowledge in physical confirmation — the architecture for genuine AGI.</p>
      <span class="work-link-muted">In Development →</span>
    </div>
  </div>
</section>

<!-- HUMANITARIAN -->
<section class="humanitarian" id="humanitarian">
  <div class="humanitarian-inner">
    <div class="fade-in">
      <div class="section-label">Our Purpose</div>
      <h2>Built to <em>protect</em><br>the most vulnerable.</h2>
      <p>Every commercial product we build subsidizes free access for the organizations that need these tools most. This is not a pledge. It is written into how we operate.</p>
      <p>All programs we create can be deployed by law enforcement and prosecutors to combat digital sexual exploitation of children and adults. Our signal intelligence and fusion incident architecture exist, in part, for exactly this purpose.</p>
    </div>
    <div class="humanitarian-commitments fade-in">
      <div class="commitment">
        <h4>Child Protection</h4>
        <p>Free access to all Aletheia tools for organizations working to combat child exploitation and trafficking. No cost. No conditions.</p>
      </div>
      <div class="commitment">
        <h4>Law Enforcement Support</h4>
        <p>Our Fusion Incident Intelligence and Phoenix Signal Network are designed to help investigators identify and prosecute perpetrators of digital exploitation.</p>
      </div>
      <div class="commitment">
        <h4>Humanitarian Research</h4>
        <p>Non-profit scientific research institutions and humanitarian medical operations receive access to our intelligence infrastructure at no cost.</p>
      </div>
      <div class="commitment">
        <h4>Equal Epistemology</h4>
        <p>Verified intelligence should not belong only to those who can afford the largest training runs. The ground truth is physical reality — accessible to everyone.</p>
      </div>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section class="contact" id="contact">
  <div class="fade-in">
    <div class="section-label">Get In Touch</div>
    <h2>Let's build something <em>true.</em></h2>
    <p>We are open to partnerships, research collaborations, and conversations with organizations who share our belief that intelligence should be verified, safe, and equal.</p>
    <a href="mailto:tom@aletheiafi.com" class="contact-email">tom@aletheiafi.com</a>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-logo">Aletheia<span>FI</span></div>
  <div class="footer-copy">© 2026 AletheiaFI LLC. All rights reserved.</div>
  <div class="footer-links">
    <a href="#mission">Mission</a>
    <a href="#work">Work</a>
    <a href="#humanitarian">Purpose</a>
    <a href="#contact">Contact</a>
  </div>
</footer>

<script>
  // Scroll-triggered fade-in
  const observer = new IntersectionObserver((entries) => {
    entries.forEach((entry, i) => {
      if (entry.isIntersecting) {
        setTimeout(() => {
          entry.target.classList.add('visible');
        }, i * 100);
        observer.unobserve(entry.target);
      }
    });
  }, { threshold: 0.1, rootMargin: '0px 0px -60px 0px' });

  document.querySelectorAll('.fade-in').forEach(el => observer.observe(el));

  // Smooth scroll for nav links
  document.querySelectorAll('a[href^="#"]').forEach(anchor => {
    anchor.addEventListener('click', function(e) {
      e.preventDefault();
      const target = document.querySelector(this.getAttribute('href'));
      if (target) target.scrollIntoView({ behavior: 'smooth', block: 'start' });
    });
  });
</script>

</body>
</html>
