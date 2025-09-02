# ffghtxsd
<title>Kenzo | Ethical Hacker</title>
<script src="https://cdn.tailwindcss.com"></script>
<script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>

<style>
/* Animated Gradient Background (lebih redup) */
body {
  background: linear-gradient(-45deg, #0a0f1a, #111827, #0b2c3d, #16213e);
  background-size: 400% 400%;
  animation: gradientMove 15s ease infinite;
  font-family: 'Courier New', monospace;
  color: #cbd5e1; /* lebih soft dari #e2e8f0 */
}
@keyframes gradientMove {
  0% { background-position: 0% 50%; }
  50% { background-position: 100% 50%; }
  100% { background-position: 0% 50%; }
}

/* Neon Border Glow (lebih redup) */
.card {
  border: 1px solid #00e0d6;
  border-radius: 0.5rem;
  padding: 1rem;
  background-color: rgba(10, 15, 25, 0.85);
  position: relative;
  overflow: hidden;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}
.card::before {
  content: "";
  position: absolute;
  top: -50%;
  left: -50%;
  width: 200%;
  height: 200%;
  background: conic-gradient(
    from 0deg,
    #00e0d6,
    transparent,
    #00e0d6,
    transparent
  );
  animation: spin 6s linear infinite;
  z-index: 0;
  opacity: 0.4; /* efek lebih redup */
}
.card > * {
  position: relative;
  z-index: 1;
}
.card:hover {
  transform: scale(1.03);
  box-shadow: 0 0 15px #00e0d6;
}
@keyframes spin {
  100% { transform: rotate(360deg); }
}

/* Floating Particles (lebih redup & kecil) */
.particles {
  position: fixed;
  top: 0; left: 0;
  width: 100%; height: 100%;
  z-index: -1;
  overflow: hidden;
}
.particle {
  position: absolute;
  width: 3px; height: 3px;
  background: #00e0d6;
  border-radius: 50%;
  opacity: 0.35;
  animation: float 14s linear infinite;
}
@keyframes float {
  from { transform: translateY(100vh) scale(0.4); opacity: 0; }
  20% { opacity: 0.7; }
  to { transform: translateY(-10vh) scale(0.9); opacity: 0; }
}
</style>

<body>
<div class="particles">
  <!-- Partikel akan di-generate via JS -->
</div>

<h1 class="text-center text-lg font-bold text-cyan-400 mb-4">Kenzo — Ethical Hacker</h1>
<p class="text-center text-sm text-slate-300 mb-6">Security Researcher & Pentester</p>

<!-- About -->
<section class="card mx-2 mb-4" data-aos="fade-up">
  <h2 class="text-base font-bold text-cyan-300 mb-2">About Me</h2>
  <p class="text-xs text-slate-300">Saya Kenzo, fokus dalam keamanan siber & ethical hacking. 
  Tujuan saya adalah mengamankan sistem dan berbagi pengetahuan dengan komunitas.</p>
  <div class="mt-2 text-xs">
    <div><strong>Email:</strong> <a href="mailto:pykcyber@gmail.com" class="underline">pykcyber@gmail.com</a></div>
    <div><strong>WA:</strong> <a href="https://wa.me/6283143490913" class="underline">+62 831-4349-0913</a></div>
  </div>
</section>

<!-- Skills -->
<section class="card mx-2 mb-4" data-aos="fade-up">
  <h3 class="text-base font-bold text-cyan-300 mb-2">Skills</h3>
  <ul class="space-y-1 text-xs">
    <li>Web App Pentesting ⭐⭐⭐⭐⭐</li>
    <li>API Security ⭐⭐⭐⭐☆</li>
    <li>Network Hardening ⭐⭐⭐⭐☆</li>
    <li>Reverse Engineering ⭐⭐⭐☆</li>
    <li>OSINT & Threat Intel ⭐⭐⭐⭐⭐</li>
  </ul>
</section>

<!-- Projects -->
<section class="card mx-2 mb-4" data-aos="fade-up">
  <h3 class="text-base font-bold text-cyan-300 mb-2">Projects</h3>
  <ul class="space-y-1 text-xs">
    <li>Enterprise Audit ⭐⭐⭐⭐⭐</li>
    <li>Cloud Infra Review ⭐⭐⭐⭐☆</li>
    <li>Bug Bounty Findings ⭐⭐⭐⭐⭐</li>
    <li>API Security Hardening ⭐⭐⭐⭐☆</li>
  </ul>
</section>

<!-- Contact -->
<section class="card mx-2 mb-4" data-aos="fade-up">
  <h3 class="text-base font-bold text-cyan-300 mb-2">Contact</h3>
  <form class="space-y-2">
    <textarea rows="3" placeholder="Your message..."
      class="w-full text-xs p-2 rounded bg-black text-white border border-cyan-400"></textarea>
    <button class="w-full bg-cyan-500 text-black py-1 rounded font-bold text-xs hover:bg-cyan-400">Send Message</button>
  </form>
</section>

<!-- Footer -->
<footer class="text-center text-[10px] text-slate-500 mt-6" data-aos="fade-up">
  <div>Website ini dibuat oleh <strong>Kenzo</strong></div>
  <div>© 2025 Kenzo. Semua hak cipta dilindungi.</div>
</footer>

<script>
AOS.init();

// Generate floating particles
const particlesContainer = document.querySelector('.particles');
for (let i = 0; i < 40; i++) {
  const p = document.createElement('div');
  p.classList.add('particle');
  p.style.left = Math.random() * 100 + 'vw';
  p.style.animationDuration = (10 + Math.random() * 10) + 's';
  p.style.opacity = Math.random() * 0.4 + 0.2;
  particlesContainer.appendChild(p);
}
</script>
</body>
