<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Ahmad Raza - Holographic About</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r134/three.min.js"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/gsap.min.js"></script>
  <script src="https://cdn.jsdelivr.net/npm/@tensorflow/tfjs@3.21.0/dist/tf.min.js"></script>
  <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&display=swap" rel="stylesheet">
  <style>
    body { 
      margin: 0; 
      background: #000; 
      color: #fff; 
      font-family: 'Orbitron', sans-serif; 
      overflow-x: hidden; 
    }
    #scene-container { 
      position: fixed; 
      top: 0; 
      left: 0; 
      width: 100vw; 
      height: 100vh; 
      z-index: -1; 
    }
    .holo-section { 
      background: linear-gradient(135deg, rgba(0,255,255,0.2), rgba(255,0,255,0.2));
      backdrop-filter: blur(15px);
      border-radius: 20px;
      padding: 40px;
      margin: 20px auto;
      max-width: 1200px;
      box-shadow: 0 10px 40px rgba(0,255,255,0.5);
    }
    .holo-badge { 
      transition: all 0.6s; 
      filter: drop-shadow(0 0 10px #00FFFF); 
    }
    .holo-badge:hover { 
      transform: rotateY(360deg) scale(1.2); 
      filter: drop-shadow(0 0 20px #00FFFF); 
    }
    .timeline-card { 
      background: rgba(0,0,0,0.5); 
      border-radius: 15px; 
      padding: 20px; 
      margin: 20px 0; 
      transition: transform 0.6s; 
    }
    .timeline-card:hover { 
      transform: scale(1.1) translateY(-10px); 
    }
    .contact-orb { 
      transition: all 0.5s; 
      filter: drop-shadow(0 0 15px #00FFFF); 
    }
    .contact-orb:hover { 
      transform: scale(1.2) rotate(10deg); 
      filter: drop-shadow(0 0 25px #00FFFF); 
    }
    .stats-card { 
      position: relative;
      transition: all 0.6s; 
      filter: drop-shadow(0 0 15px #00FFFF); 
    }
    .stats-card:hover { 
      transform: scale(1.1) rotate(2deg); 
      filter: drop-shadow(0 0 25px #00FFFF); 
    }
    .stats-card svg.border { 
      position: absolute; 
      top: 0; 
      left: 0; 
      width: 100%; 
      height: 100%; 
      z-index: -1; 
    }
    @keyframes pulse { 
      0% { transform: scale(1); } 
      50% { transform: scale(1.1); } 
      100% { transform: scale(1); } 
    }
    @keyframes morphBorder { 
      0% { rx: 20; } 
      50% { rx: 40; } 
      100% { rx: 20; } 
    }
  </style>
</head>
<body>
  <!-- 3D Background Scene -->
  <div id="scene-container"></div>

  <!-- Hero Section -->
  <section class="holo-section text-center mt-20">
    <h1 class="text-5xl font-bold text-cyan-300 animate-pulse">Ahmad Raza</h1>
    <p class="text-xl mt-4 text-magenta-300">Architect of the Digital Multiverse</p>
    <img src="https://lottiefiles.com/animations/holographic-avatar.json" alt="Holographic Avatar" class="mx-auto mt-8 w-48" data-lottie="true" data-loop="true" data-autoplay="true" loading="lazy">
    <p class="text-lg mt-6 max-w-2xl mx-auto">I’m a full-stack visionary crafting <span class="text-cyan-300">holographic-grade experiences</span> with 3D animations, AI-driven interfaces, and cyberpunk aesthetics. Let’s redefine reality through code!</p>
  </section>

  <!-- Skills Section -->
  <section class="holo-section">
    <h2 class="text-3xl font-bold text-center text-cyan-300 mb-8">Hyper-Tech Arsenal</h2>
    <div class="flex flex-wrap gap-6 justify-center">
      <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript" class="holo-badge">
        <svg width="140" height="60" viewBox="0 0 140 60">
          <rect width="140" height="60" rx="15" fill="url(#jsGradient)"/>
          <text x="50%" y="50%" font-size="20" fill="#FFF" text-anchor="middle" dominant-baseline="middle">JavaScript</text>
          <defs>
            <linearGradient id="jsGradient" x1="0%" y1="0%" x2="100%" y2="100%">
              <stop offset="0%" style="stop-color:#F7DF1E;stop-opacity:1"/>
              <stop offset="100%" style="stop-color:#FF6F61;stop-opacity:1"/>
            </linearGradient>
          </defs>
        </svg>
      </a>
      <a href="https://www.python.org/" class="holo-badge">
        <svg width="140" height="60" viewBox="0 0 140 60">
          <rect width="140" height="60" rx="15" fill="url(#pyGradient)"/>
          <text x="50%" y="50%" font-size="20" fill="#FFF" text-anchor="middle" dominant-baseline="middle">Python</text>
          <defs>
            <linearGradient id="pyGradient" x1="0%" y1="0%" x2="100%" y2="100%">
              <stop offset="0%" style="stop-color:#3776AB;stop-opacity:1"/>
              <stop offset="100%" style="stop-color:#00FFFF;stop-opacity:1"/>
            </linearGradient>
          </defs>
        </svg>
      </a>
      <a href="https://react.dev/" class="holo-badge">
        <svg width="140" height="60" viewBox="0 0 140 60">
          <rect width="140" height="60" rx="15" fill="url(#reactGradient)"/>
          <text x="50%" y="50%" font-size="20" fill="#FFF" text-anchor="middle" dominant-baseline="middle">React</text>
          <defs>
            <linearGradient id="reactGradient" x1="0%" y1="0%" x2="100%" y2="100%">
              <stop offset="0%" style="stop-color:#61DAFB;stop-opacity:1"/>
              <stop offset="100%" style="stop-color:#FF00FF;stop-opacity:1"/>
            </linearGradient>
          </defs>
        </svg>
      </a>
      <a href="https://threejs.org/" class="holo-badge">
        <svg width="140" height="60" viewBox="0 0 140 60">
          <rect width="140" height="60" rx="15" fill="url(#threeGradient)"/>
          <text x="50%" y="50%" font-size="20" fill="#FFF" text-anchor="middle" dominant-baseline="middle">Three.js</text>
          <defs>
            <linearGradient id="threeGradient" x1="0%" y1="0%" x2="100%" y2="100%">
              <stop offset="0%" style="stop-color:#FFFFFF;stop-opacity:1"/>
              <stop offset="100%" style="stop-color:#00FF00;stop-opacity:1"/>
            </linearGradient>
          </defs>
        </svg>
      </a>
    </div>
  </section>

  <!-- GitHub Stats Section -->
  <section class="holo-section">
    <h2 class="text-3xl font-bold text-center text-cyan-300 mb-8">Cosmic Code Metrics</h2>
    <div class="flex flex-wrap gap-6 justify-center">
      <div class="stats-card relative">
        <img src="https://github-readme-stats.vercel.app/api?username=ahmadraza76&show_icons=true&theme=transparent&hide_border=true&bg_color=00000000&text_color=ffffff&icon_color=00FFFF&custom_title=Code%20Constellation" alt="GitHub Stats" loading="lazy">
        <svg class="border" viewBox="0 0 500 200" preserveAspectRatio="none">
          <rect width="500" height="200" rx="20" fill="none" stroke="url(#statsGradient)" stroke-width="4" style="animation: morphBorder 3s infinite;"/>
          <defs>
            <linearGradient id="statsGradient" x1="0%" y1="0%" x2="100%" y2="100%">
              <stop offset="0%" style="stop-color:#00FFFF;stop-opacity:1"/>
              <stop offset="100%" style="stop-color:#FF00FF;stop-opacity:1"/>
            </linearGradient>
          </defs>
        </svg>
      </div>
      <div class="stats-card relative">
        <img src="https://github-readme-streak-stats.herokuapp.com/?user=ahmadraza76&theme=transparent&hide_border=true&bg_color=00000000&text_color=ffffff&icon_color=00FFFF&fire=FF00FF&currStreakLabel=Stellar%20Streak" alt="GitHub Streak" loading="lazy">
        <svg class="border" viewBox="0 0 500 200" preserveAspectRatio="none">
          <rect width="500" height="200" rx="20" fill="none" stroke="url(#streakGradient)" stroke-width="4" style="animation: morphBorder 3s infinite;"/>
          <defs>
            <linearGradient id="streakGradient" x1="0%" y1="0%" x2="100%" y2="100%">
              <stop offset="0%" style="stop-color:#FF00FF;stop-opacity:1"/>
              <stop offset="100%" style="stop-color:#00FFFF;stop-opacity:1"/>
            </linearGradient>
          </defs>
        </svg>
      </div>
      <div class="stats-card relative">
        <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=ahmadraza76&layout=compact&theme=transparent&hide_border=true&bg_color=00000000&text_color=ffffff&icon_color=00FFFF&title_color=FF00FF" alt="Top Languages" loading="lazy">
        <svg class="border" viewBox="0 0 500 150" preserveAspectRatio="none">
          <rect width="500" height="150" rx="20" fill="none" stroke="url(#langGradient)" stroke-width="4" style="animation: morphBorder 3s infinite;"/>
          <defs>
            <linearGradient id="langGradient" x1="0%" y1="0%" x2="100%" y2="100%">
              <stop offset="0%" style="stop-color:#00FFFF;stop-opacity:1"/>
              <stop offset="100%" style="stop-color:#FF00FF;stop-opacity:1"/>
            </linearGradient>
          </defs>
        </svg>
      </div>
    </div>
  </section>

  <!-- Timeline Section -->
  <section class="holo-section">
    <h2 class="text-3xl font-bold text-center text-cyan-300 mb-8">My Cosmic Journey</h2>
    <div class="space-y-8">
      <div class="timeline-card">
        <h3 class="text-xl text-magenta-300">2020: First Code Spark</h3>
        <p>Wrote my first line of code in JavaScript, igniting a passion for building digital worlds.</p>
      </div>
      <div class="timeline-card">
        <h3 class="text-xl text-magenta-300">2022: Full-Stack Mastery</h3>
        <p>Mastered MERN stack and launched my first holographic portfolio with 3D animations.</p>
      </div>
      <div class="timeline-card">
        <h3 class="text-xl text-magenta-300">2025: AI & WebGL Frontier</h3>
        <p>Pioneering AI-driven interfaces and WebGL experiences that redefine UI/UX.</p>
      </div>
    </div>
  </section>

  <!-- Contact Section -->
  <section class="holo-section text-center">
    <h2 class="text-3xl font-bold text-cyan-300 mb-8">Interstellar Comms</h2>
    <p class="text-lg mb-6">Beam me a message to collaborate on the next big thing!</p>
    <div class="flex gap-8 justify-center">
      <a href="mailto:your-email@example.com" class="contact-orb">
        <svg width="80" height="80" viewBox="0 0 80 80">
          <circle cx="40" cy="40" r="40" fill="url(#emailGradient)"/>
          <path d="M20 30 H60 V50 H20 Z M20 30 L40 45 L60 30" fill="#FFF"/>
          <defs>
            <radialGradient id="emailGradient" cx="50%" cy="50%" r="50%">
              <stop offset="0%" style="stop-color:#00FFFF;stop-opacity:1"/>
              <stop offset="100%" style="stop-color:#000;stop-opacity:0.5"/>
            </radialGradient>
          </defs>
        </svg>
      </a>
      <a href="https://linkedin.com/in/yourprofile" class="contact-orb">
        <svg width="80" height="80" viewBox="0 0 80 80">
          <circle cx="40" cy="40" r="40" fill="url(#linkedinGradient)"/>
          <path d="M25 35 H30 V55 H25 Z M27.5 30 A2.5 2.5 0 1 1 27.5 25 A2.5 2.5 0 1 1 27.5 30 Z M35 35 H40 V55 H35 Z M45 35 H50 V55 H45 Z" fill="#FFF"/>
          <defs>
            <radialGradient id="linkedinGradient" cx="50%" cy="50%" r="50%">
              <stop offset="0%" style="stop-color:#0A66C2;stop-opacity:1"/>
              <stop offset="100%" style="stop-color:#000;stop-opacity:0.5"/>
            </radialGradient>
          </defs>
        </svg>
      </a>
      <a href="https://your-portfolio-link.com" class="contact-orb">
        <svg width="80" height="80" viewBox="0 0 80 80">
          <circle cx="40" cy="40" r="40" fill="url(#portfolioGradient)"/>
          <path d="M25 25 H55 V55 H25 Z M30 30 H50 V50 H30 Z" fill="#FFF"/>
          <defs>
            <radialGradient id="portfolioGradient" cx="50%" cy="50%" r="50%">
              <stop offset="0%" style="stop-color:#FF4500;stop-opacity:1"/>
              <stop offset="100%" style="stop-color:#000;stop-opacity:0.5"/>
            </radialGradient>
          </defs>
        </svg>
      </a>
    </div>
  </section>

  <script>
    // Three.js Scene Setup
    const scene = new THREE.Scene();
    const camera = new THREE.PerspectiveCamera(75, window.innerWidth / window.innerHeight, 0.1, 1000);
    const renderer = new THREE.WebGLRenderer({ antialias: true, alpha: true });
    renderer.setSize(window.innerWidth, window.innerHeight);
    document.getElementById('scene-container').appendChild(renderer.domElement);

    // 3D Orb for Background
    const geometry = new THREE.SphereGeometry(2, 64, 64);
    const material = new THREE.MeshBasicMaterial({ color: 0x00FFFF, wireframe: true });
    const orb = new THREE.Mesh(geometry, material);
    scene.add(orb);
    camera.position.z = 8;

    // GSAP Animations
    gsap.from('h1', { y: -100, opacity: 0, duration: 1, ease: 'power3.out' });
    gsap.from('.holo-badge', { y: 50, opacity: 0, stagger: 0.2, duration: 1, delay: 0.5, ease: 'power3.out' });
    gsap.from('.stats-card', { x: 100, opacity: 0, stagger: 0.3, duration: 1, delay: 1, ease: 'power3.out' });
    gsap.from('.timeline-card', { x: -100, opacity: 0, stagger: 0.3, duration: 1, delay: 1.5, ease: 'power3.out' });
    gsap.from('.contact-orb', { scale: 0, opacity: 0, stagger Sunt: 0.2, duration: 1, delay: 2, ease: 'elastic.out(1, 0.3)' });

    // AI-Driven Mouse Interaction
    let mouseX = 0, mouseY = 0;
    document.addEventListener('mousemove', (e) => {
      mouseX = e.clientX / window.innerWidth;
      mouseY = e.clientY / window.innerHeight;
      gsap.to(orb.rotation, { x: mouseY * 0.5, y: mouseX * 0.5, duration: 1 });
      gsap.to('.stats-card', { 
        rotationY: mouseX * 10, 
        rotationX: mouseY * -10, 
        duration: 1, 
        ease: 'power2.out' 
      });
    });

    // Render Loop
    function animate() {
      requestAnimationFrame(animate);
      orb.rotation.y += 0.01;
      renderer.render(scene, camera);
    }
    animate();

    // Resize Handler
    window.addEventListener('resize', () => {
      camera.aspect = window.innerWidth / window.innerHeight;
      camera.updateProjectionMatrix();
      renderer.setSize(window.innerWidth, window.innerHeight);
    });
  </script>
</body>
</html>
