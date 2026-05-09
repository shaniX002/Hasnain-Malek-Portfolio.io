<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Hasnain Ali — Flutter Developer</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Clash+Display:wght@400;500;600;700&family=Cabinet+Grotesk:wght@300;400;500;700&display=swap" rel="stylesheet">
<style>
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0}
:root{
  --white:#ffffff;
  --off:#f7f6f3;
  --ink:#0d0d0d;
  --ink2:#4a4a4a;
  --ink3:#9a9a9a;
  --line:#e8e6e0;
  --accent:#5b4cff;
  --accent-light:#ede9ff;
}
html{scroll-behavior:smooth}
body{
  background:var(--white);
  color:var(--ink);
  font-family:'Cabinet Grotesk',sans-serif;
  font-size:16px;
  line-height:1.6;
  -webkit-font-smoothing:antialiased;
}
nav{
  display:flex;align-items:center;justify-content:space-between;
  padding:1.5rem 4rem;
  border-bottom:1px solid var(--line);
  position:sticky;top:0;background:rgba(255,255,255,0.95);
  backdrop-filter:blur(12px);z-index:100;
}
.logo{font-family:'Clash Display',sans-serif;font-size:1.25rem;font-weight:700;color:var(--ink);text-decoration:none}
.logo span{color:var(--accent)}
.nav-links{display:flex;gap:2.5rem;list-style:none}
.nav-links a{font-size:0.875rem;font-weight:500;color:var(--ink2);text-decoration:none;transition:color 0.2s}
.nav-links a:hover{color:var(--ink)}
.nav-btn{background:var(--ink);color:#fff;padding:0.5rem 1.5rem;border-radius:100px;font-size:0.875rem;font-weight:500;text-decoration:none;transition:background 0.2s}
.nav-btn:hover{background:var(--accent)}
.hero{padding:6rem 4rem 5rem;max-width:1200px;margin:0 auto}
.hero-badge{display:inline-flex;align-items:center;gap:0.4rem;background:var(--accent-light);color:var(--accent);font-size:0.78rem;font-weight:600;letter-spacing:0.06em;padding:0.3rem 1rem;border-radius:100px;margin-bottom:1.75rem;text-transform:uppercase}
.hero-badge::before{content:'';width:6px;height:6px;border-radius:50%;background:var(--accent)}
.hero h1{font-family:'Clash Display',sans-serif;font-size:clamp(3rem,6vw,5.5rem);font-weight:700;line-height:1.02;letter-spacing:-0.03em;max-width:900px;color:var(--ink)}
.hero h1 .hl{color:var(--accent)}
.hero-sub{margin-top:1.5rem;font-size:1.1rem;color:var(--ink2);max-width:480px;font-weight:400;line-height:1.7}
.hero-ctas{margin-top:2.5rem;display:flex;gap:1rem;flex-wrap:wrap}
.btn-dark{background:var(--ink);color:#fff;padding:0.8rem 2rem;border-radius:100px;font-weight:600;font-size:0.95rem;text-decoration:none;transition:background 0.2s,transform 0.15s;display:inline-block}
.btn-dark:hover{background:var(--accent);transform:translateY(-2px)}
.btn-outline{border:1.5px solid var(--line);color:var(--ink);padding:0.8rem 2rem;border-radius:100px;font-weight:600;font-size:0.95rem;text-decoration:none;transition:border-color 0.2s,transform 0.15s;display:inline-block}
.btn-outline:hover{border-color:var(--ink);transform:translateY(-2px)}
.wrap{max-width:1200px;margin:0 auto;padding:0 4rem}
.sec-head{display:flex;align-items:baseline;justify-content:space-between;border-top:1.5px solid var(--ink);padding-top:0.8rem;margin-bottom:3rem}
.sec-title{font-family:'Clash Display',sans-serif;font-size:0.75rem;font-weight:700;letter-spacing:0.1em;text-transform:uppercase;color:var(--ink)}
.sec-sub{font-size:0.75rem;color:var(--ink3)}
#projects{padding:5rem 0}
.proj-big{background:var(--off);border-radius:20px;overflow:hidden;margin-bottom:1.5rem;display:grid;grid-template-columns:1fr 1.1fr;min-height:460px}
.proj-big.flip{direction:rtl}
.proj-big.flip>*{direction:ltr}
.proj-copy{padding:3.5rem;display:flex;flex-direction:column;justify-content:center}
.proj-num{font-family:'Clash Display',sans-serif;font-size:0.7rem;font-weight:700;letter-spacing:0.12em;text-transform:uppercase;color:var(--ink3);margin-bottom:1.1rem}
.proj-copy h2{font-family:'Clash Display',sans-serif;font-size:2.2rem;font-weight:700;letter-spacing:-0.02em;line-height:1.1;margin-bottom:0.7rem}
.proj-copy p{font-size:0.95rem;color:var(--ink2);line-height:1.7;margin-bottom:1.4rem;max-width:360px}
.tags{display:flex;flex-wrap:wrap;gap:0.4rem;margin-bottom:1.75rem}
.tag{font-size:0.72rem;font-weight:600;padding:0.25rem 0.7rem;border-radius:100px;background:#fff;border:1px solid var(--line);color:var(--ink2)}
.proj-link{display:inline-flex;align-items:center;gap:0.5rem;color:var(--ink);font-weight:700;font-size:0.9rem;text-decoration:none;border-bottom:2px solid var(--ink);padding-bottom:0.1rem;width:fit-content;transition:color 0.2s,border-color 0.2s}
.proj-link:hover{color:var(--accent);border-color:var(--accent)}
.proj-link svg{width:13px;height:13px;transition:transform 0.2s}
.proj-link:hover svg{transform:translate(2px,-2px)}
.screens{display:flex;align-items:center;justify-content:center;padding:2.5rem 2rem;gap:12px;overflow:hidden}
.screens.a{background:linear-gradient(135deg,#f0eeff 0%,#e8f5ff 100%)}
.screens.b{background:linear-gradient(135deg,#fff0f5 0%,#ffe0ea 100%)}
.screens.c{background:linear-gradient(135deg,#e8fff5 0%,#d0ffe8 100%)}
.screens.d{background:linear-gradient(135deg,#fff8e0 0%,#ffefc0 100%)}
.screens.e{background:linear-gradient(135deg,#e8f0ff 0%,#d8e4ff 100%)}
.ph{width:110px;flex-shrink:0;background:#fff;border-radius:20px;overflow:hidden;box-shadow:0 4px 24px rgba(0,0,0,0.10),0 1px 4px rgba(0,0,0,0.06);transition:transform 0.4s cubic-bezier(.34,1.56,.64,1)}
.ph:nth-child(odd){transform:translateY(-14px) rotate(-1deg)}
.ph:nth-child(even){transform:translateY(14px) rotate(1deg)}
.proj-big:hover .ph,.proj-card:hover .ph,.wide-card:hover .ph{transform:translateY(0) rotate(0) !important}
.ph img{width:100%;display:block}
.grid3{display:grid;grid-template-columns:repeat(3,1fr);gap:1.5rem;margin-top:1.5rem}
.proj-card{background:var(--off);border-radius:16px;overflow:hidden;transition:transform 0.3s cubic-bezier(.34,1.56,.64,1)}
.proj-card:hover{transform:translateY(-6px)}
.card-scr{display:flex;align-items:center;justify-content:center;padding:2rem 1.5rem;gap:10px;min-height:200px}
.card-scr .ph{width:80px;border-radius:14px}
.card-scr .ph:nth-child(odd){transform:translateY(-10px) rotate(-1deg)}
.card-scr .ph:nth-child(even){transform:translateY(10px) rotate(1deg)}
.card-body{padding:1.5rem}
.card-body h3{font-family:'Clash Display',sans-serif;font-size:1.2rem;font-weight:700;letter-spacing:-0.01em;margin-bottom:0.4rem}
.card-body p{font-size:0.85rem;color:var(--ink2);line-height:1.6;margin-bottom:1rem}
.wide-card{background:var(--off);border-radius:16px;overflow:hidden;display:grid;grid-template-columns:260px 1fr;margin-top:1.5rem;transition:transform 0.3s}
.wide-card:hover{transform:translateY(-4px)}
.wide-body{padding:2.5rem;display:flex;flex-direction:column;justify-content:center}
.wide-body h3{font-family:'Clash Display',sans-serif;font-size:1.6rem;font-weight:700;letter-spacing:-0.02em;margin-bottom:0.5rem}
.wide-body p{font-size:0.9rem;color:var(--ink2);line-height:1.7;margin-bottom:1.25rem;max-width:420px}
#about{padding:5rem 0;border-top:1px solid var(--line)}
.about-grid{display:grid;grid-template-columns:1fr 1fr;gap:6rem;align-items:start}
.about-left h2{font-family:'Clash Display',sans-serif;font-size:clamp(2rem,3.5vw,3rem);font-weight:700;letter-spacing:-0.025em;line-height:1.1;margin-bottom:1.25rem}
.about-left p{color:var(--ink2);margin-bottom:1rem;font-size:0.975rem;line-height:1.75}
.chips{display:flex;flex-wrap:wrap;gap:0.5rem;margin-top:1.75rem}
.chip{font-size:0.8rem;font-weight:500;border:1px solid var(--line);border-radius:8px;padding:0.3rem 0.75rem;color:var(--ink2);transition:border-color 0.2s,color 0.2s;background:#fff}
.chip:hover{border-color:var(--accent);color:var(--accent)}
.svcs{display:flex;flex-direction:column}
.svc{display:grid;grid-template-columns:2.5rem 1fr;gap:1rem;padding:1.5rem 0;border-bottom:1px solid var(--line);align-items:start}
.svc-n{font-family:'Clash Display',sans-serif;font-size:0.7rem;font-weight:700;color:var(--ink3);letter-spacing:0.1em;padding-top:0.15rem}
.svc h4{font-family:'Clash Display',sans-serif;font-size:1rem;font-weight:700;margin-bottom:0.3rem}
.svc p{font-size:0.85rem;color:var(--ink2);line-height:1.6}
#contact{padding:5rem 0;border-top:1px solid var(--line)}
.cbox{background:var(--ink);color:#fff;border-radius:24px;padding:5rem 4rem;text-align:center}
.cbox h2{font-family:'Clash Display',sans-serif;font-size:clamp(2.2rem,4vw,3.5rem);font-weight:700;letter-spacing:-0.03em;line-height:1.05;margin-bottom:1rem}
.cbox h2 span{color:#a89bff}
.cbox p{color:#9a9a9a;font-size:1rem;margin-bottom:2.5rem}
.cbtns{display:flex;justify-content:center;gap:1rem;flex-wrap:wrap}
.btn-w{background:#fff;color:var(--ink);padding:0.8rem 2rem;border-radius:100px;font-weight:700;font-size:0.95rem;text-decoration:none;transition:background 0.2s,transform 0.15s;display:inline-block}
.btn-w:hover{background:#a89bff;transform:translateY(-2px)}
.btn-g{border:1.5px solid rgba(255,255,255,0.2);color:#fff;padding:0.8rem 2rem;border-radius:100px;font-weight:600;font-size:0.95rem;text-decoration:none;transition:border-color 0.2s;display:inline-block}
.btn-g:hover{border-color:rgba(255,255,255,0.5)}
footer{padding:1.75rem 4rem;border-top:1px solid var(--line);display:flex;align-items:center;justify-content:space-between;font-size:0.82rem;color:var(--ink3)}
footer a{color:var(--ink3);text-decoration:none}
footer a:hover{color:var(--ink)}
@media(max-width:960px){
  nav,footer{padding:1.25rem 2rem}
  .hero,.wrap{padding-left:2rem;padding-right:2rem}
  .proj-big{grid-template-columns:1fr}
  .proj-big.flip{direction:ltr}
  .screens{order:-1}
  .grid3{grid-template-columns:1fr 1fr}
  .about-grid{grid-template-columns:1fr;gap:3rem}
  .nav-links{display:none}
  .cbox{padding:3rem 2rem}
  footer{flex-direction:column;gap:0.5rem;text-align:center}
}
@media(max-width:600px){
  .grid3{grid-template-columns:1fr}
  .wide-card{grid-template-columns:1fr}
  .hero h1{font-size:2.6rem}
}
</style>
</head>
<body>

<nav>
  <a href="#" class="logo">Hasnain<span>.</span></a>
  <ul class="nav-links">
    <li><a href="#projects">Work</a></li>
    <li><a href="#about">About</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
  <a href="#contact" class="nav-btn">Hire me</a>
</nav>

<header class="hero">
  <div class="hero-badge">Flutter Developer · AI Specialist</div>
  <h1>Building mobile apps<br><span class="hl">clients love.</span></h1>
  <p class="hero-sub">I craft intelligent Flutter apps — beautiful UI, seamless performance, and AI that actually works.</p>
  <div class="hero-ctas">
    <a href="#projects" class="btn-dark">See my apps</a>
    <a href="#contact" class="btn-outline">Let's talk</a>
  </div>
</header>

<section id="projects">
  <div class="wrap">
    <div class="sec-head">
      <span class="sec-title">Selected work</span>
      <span class="sec-sub">7 projects</span>
    </div>

    <div class="proj-big">
      <div class="proj-copy">
        <div class="proj-num">01 — Education · AI</div>
        <h2>Revisable</h2>
        <p>AI-powered study app for medical and finance students. Generates practice tests, flashcards, and study material — with ChatGPT for instant doubt-solving.</p>
        <div class="tags">
          <span class="tag">MBBS</span><span class="tag">NEET</span><span class="tag">USMLE</span><span class="tag">CA · CFA</span><span class="tag">ChatGPT</span>
        </div>
        <a href="https://www.revisable.in/" class="proj-link" target="_blank">Visit Revisable <svg viewBox="0 0 16 16" fill="none" stroke="currentColor" stroke-width="2.5"><path d="M3 8h10M9 4l4 4-4 4"/></svg></a>
      </div>
      <div class="screens a">
        <div class="ph"><img src="Revisable/1.png" alt="Revisable" loading="lazy"></div>
        <div class="ph"><img src="Revisable/2.png" alt="Revisable" loading="lazy"></div>
        <div class="ph"><img src="Revisable/3.png" alt="Revisable" loading="lazy"></div>
        <div class="ph"><img src="Revisable/4.png" alt="Revisable" loading="lazy"></div>
        <div class="ph"><img src="Revisable/5.png" alt="Revisable" loading="lazy"></div>
      </div>
    </div>

    <div class="proj-big flip">
      <div class="proj-copy">
        <div class="proj-num">02 — AI · Learning</div>
        <h2>Doubt Clear AI</h2>
        <p>Snap a photo of any question and get expert-level answers instantly — 24/7, in any language, for any subject.</p>
        <div class="tags">
          <span class="tag">Snap & Solve</span><span class="tag">Multilingual</span><span class="tag">Math</span><span class="tag">Science</span>
        </div>
        <a href="https://www.doubtclear.ai/" class="proj-link" target="_blank">Visit Doubt Clear AI <svg viewBox="0 0 16 16" fill="none" stroke="currentColor" stroke-width="2.5"><path d="M3 8h10M9 4l4 4-4 4"/></svg></a>
      </div>
      <div class="screens b">
        <div class="ph"><img src="doubtclearai/1.png" alt="Doubt Clear AI" loading="lazy"></div>
        <div class="ph"><img src="doubtclearai/2.png" alt="Doubt Clear AI" loading="lazy"></div>
        <div class="ph"><img src="doubtclearai/3.png" alt="Doubt Clear AI" loading="lazy"></div>
        <div class="ph"><img src="doubtclearai/4.png" alt="Doubt Clear AI" loading="lazy"></div>
      </div>
    </div>

    <div class="proj-big">
      <div class="proj-copy">
        <div class="proj-num">03 — Creative · Writing</div>
        <h2>ScriptBae</h2>
        <p>AI writing assistant for content creators. Smart plot suggestions, dialogue tools, and real-time collaboration for TV, film, and e-learning.</p>
        <div class="tags">
          <span class="tag">AI Writing</span><span class="tag">Collaboration</span><span class="tag">TV & Film</span>
        </div>
        <a href="http://www.visionarchitech.com" class="proj-link" target="_blank">View ScriptBae <svg viewBox="0 0 16 16" fill="none" stroke="currentColor" stroke-width="2.5"><path d="M3 8h10M9 4l4 4-4 4"/></svg></a>
      </div>
      <div class="screens c">
        <div class="ph"><img src="scriptbae/1.png" alt="ScriptBae" loading="lazy"></div>
        <div class="ph"><img src="scriptbae/2.png" alt="ScriptBae" loading="lazy"></div>
        <div class="ph"><img src="scriptbae/3.png" alt="ScriptBae" loading="lazy"></div>
        <div class="ph"><img src="scriptbae/4.png" alt="ScriptBae" loading="lazy"></div>
      </div>
    </div>

    <div class="grid3">
      <div class="proj-card">
        <div class="card-scr d">
          <div class="ph"><img src="remoteTal/1.png" alt="RemoteTal" loading="lazy"></div>
          <div class="ph"><img src="remoteTal/2.png" alt="RemoteTal" loading="lazy"></div>
        </div>
        <div class="card-body">
          <div class="tags"><span class="tag">Recruitment</span><span class="tag">Remote</span></div>
          <h3>RemoteTal</h3>
          <p>Global talent marketplace — connecting companies with verified remote professionals, streamlined hiring, secure payments.</p>
          <a href="http://www.itechgemini.com" class="proj-link" target="_blank" style="font-size:0.85rem">View project <svg viewBox="0 0 16 16" fill="none" stroke="currentColor" stroke-width="2.5" style="width:12px;height:12px"><path d="M3 8h10M9 4l4 4-4 4"/></svg></a>
        </div>
      </div>
      <div class="proj-card">
        <div class="card-scr a">
          <div class="ph"><img src="codeAI/1.png" alt="CodeAI" loading="lazy"></div>
          <div class="ph"><img src="codeAI/2.png" alt="CodeAI" loading="lazy"></div>
        </div>
        <div class="card-body">
          <div class="tags"><span class="tag">Dev Tool</span><span class="tag">AI</span></div>
          <h3>CodeAI</h3>
          <p>Virtual coding assistant — turns natural language into code, debugs errors, and teaches programming on demand.</p>
          <a href="http://www.itechgemini.com" class="proj-link" target="_blank" style="font-size:0.85rem">View project <svg viewBox="0 0 16 16" fill="none" stroke="currentColor" stroke-width="2.5" style="width:12px;height:12px"><path d="M3 8h10M9 4l4 4-4 4"/></svg></a>
        </div>
      </div>
      <div class="proj-card">
        <div class="card-scr c">
          <div class="ph"><img src="pizzagpt/1.png" alt="PizzaGPT" loading="lazy"></div>
          <div class="ph"><img src="pizzagpt/2.png" alt="PizzaGPT" loading="lazy"></div>
        </div>
        <div class="card-body">
          <div class="tags"><span class="tag">AI Chat</span><span class="tag">Free</span></div>
          <h3>PizzaGPT</h3>
          <p>Multi-purpose AI chatbot for personalized recommendations and on-demand help — available 24/7 at no cost.</p>
          <a href="http://www.itechgemini.com" class="proj-link" target="_blank" style="font-size:0.85rem">View project <svg viewBox="0 0 16 16" fill="none" stroke="currentColor" stroke-width="2.5" style="width:12px;height:12px"><path d="M3 8h10M9 4l4 4-4 4"/></svg></a>
        </div>
      </div>
    </div>

    <div class="wide-card">
      <div class="card-scr e" style="min-height:180px">
        <div class="ph"><img src="speechAI/1.png" alt="Speech AI" loading="lazy"></div>
        <div class="ph"><img src="speechAI/2.png" alt="Speech AI" loading="lazy"></div>
      </div>
      <div class="wide-body">
        <div class="tags"><span class="tag">Voice AI</span><span class="tag">Multilingual</span><span class="tag">Speech</span></div>
        <h3>Speech AI</h3>
        <p>Natural voice interaction for language learning and on-demand AI knowledge — communicate in any language, anytime.</p>
        <a href="http://www.itechgemini.com" class="proj-link" target="_blank" style="font-size:0.9rem">View project <svg viewBox="0 0 16 16" fill="none" stroke="currentColor" stroke-width="2.5" style="width:12px;height:12px"><path d="M3 8h10M9 4l4 4-4 4"/></svg></a>
      </div>
    </div>

  </div>
</section>

<section id="about">
  <div class="wrap">
    <div class="sec-head"><span class="sec-title">About</span></div>
    <div class="about-grid">
      <div class="about-left">
        <h2>Hasnain Ali.<br>Flutter developer<br>& AI builder.</h2>
        <p>I'm a passionate Flutter developer specializing in intelligent mobile applications that blend innovative design with cutting-edge AI and machine learning technologies.</p>
        <p>Every project starts with understanding what users actually need — then I execute with clean architecture, beautiful UI, and meaningful features that solve real problems.</p>
        <div class="chips">
          <span class="chip">Flutter</span>
          <span class="chip">Dart</span>
          <span class="chip">AI Integration</span>
          <span class="chip">ChatGPT API</span>
          <span class="chip">Firebase</span>
          <span class="chip">REST APIs</span>
          <span class="chip">UI/UX Design</span>
          <span class="chip">State Management</span>
          <span class="chip">Clean Architecture</span>
          <span class="chip">App Store Optimization</span>
        </div>
      </div>
      <div class="svcs">
        <div class="svc"><span class="svc-n">01</span><div><h4>Mobile App Development</h4><p>Production-ready Flutter apps for iOS and Android — clean code, great performance, zero compromise.</p></div></div>
        <div class="svc"><span class="svc-n">02</span><div><h4>AI & ML Integration</h4><p>Embedding ChatGPT, vision models, and ML directly into mobile apps with seamless user experiences.</p></div></div>
        <div class="svc"><span class="svc-n">03</span><div><h4>EdTech Solutions</h4><p>Specialized in education apps — flashcards, test engines, video courses, and AI tutoring.</p></div></div>
        <div class="svc"><span class="svc-n">04</span><div><h4>UI/UX Craftsmanship</h4><p>Pixel-perfect Flutter interfaces that feel native, intuitive, and genuinely delightful to use.</p></div></div>
      </div>
    </div>
  </div>
</section>

<section id="contact">
  <div class="wrap">
    <div class="cbox">
      <h2>Let's build something<br><span>great together.</span></h2>
      <p>Open to freelance, full-time, and collaboration opportunities.</p>
      <div class="cbtns">
        <a href="mailto:hasnainali@example.com" class="btn-w">Send an email</a>
        <a href="http://www.itechgemini.com" class="btn-g" target="_blank">iTech Gemini</a>
        <a href="http://www.visionarchitech.com" class="btn-g" target="_blank">Vision Architech</a>
      </div>
    </div>
  </div>
</section>

<footer>
  <span>© 2025 Hasnain Ali</span>
  <div style="display:flex;gap:1.5rem">
    <a href="http://www.itechgemini.com">iTech Gemini</a>
    <a href="http://www.visionarchitech.com">Vision Architech</a>
  </div>
</footer>

</body>
</html>
