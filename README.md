<div align="center">
  <svg width="100%" height="800" viewBox="0 0 1200 800" xmlns="http://www.w3.org/2000/svg">
    <defs>
      <!-- Cosmic Gradients -->
      <radialGradient id="space-bg" cx="50%" cy="50%" r="70%">
        <stop offset="0%" stop-color="#0a0520" />
        <stop offset="50%" stop-color="#05020a" />
        <stop offset="100%" stop-color="#000000" />
      </radialGradient>
      
      <linearGradient id="neon-purple-blue" x1="0%" y1="0%" x2="100%" y2="100%">
        <stop offset="0%" stop-color="#a855f7" />
        <stop offset="50%" stop-color="#3b82f6" />
        <stop offset="100%" stop-color="#06b6d4" />
      </linearGradient>

      <linearGradient id="hud-glow" x1="0%" y1="0%" x2="0%" y2="100%">
        <stop offset="0%" stop-color="#06b6d4" stop-opacity="0.8" />
        <stop offset="100%" stop-color="#3b82f6" stop-opacity="0.1" />
      </linearGradient>

      <!-- Glow Filters -->
      <filter id="glow" x="-20%" y="-20%" width="140%" height="140%">
        <feGaussianBlur stdDeviation="6" result="blur" />
        <feComposite in="SourceGraphic" in2="blur" operator="over" />
      </filter>
      
      <filter id="deep-glow" x="-50%" y="-50%" width="200%" height="200%">
        <feGaussianBlur stdDeviation="15" result="blur1" />
        <feGaussianBlur stdDeviation="30" result="blur2" />
        <feMerge>
          <feMergeNode in="blur2" />
          <feMergeNode in="blur1" />
          <feMergeNode in="SourceGraphic" />
        </feMerge>
      </filter>

      <!-- Star Template -->
      <circle id="star" r="1.2" fill="#ffffff" opacity="0.8">
        <animate attributeName="opacity" values="0.3;1;0.3" dur="3s" repeatCount="indefinite" />
      </circle>
    </defs>

    <!-- Deep Space Background -->
    <rect width="1200" height="800" fill="url(#space-bg)" />

    <!-- Nebula Effects -->
    <path d="M100,50 Q400,200 300,500 T700,600 Q900,400 1100,200 Z" fill="url(#neon-purple-blue)" opacity="0.15" filter="url(#deep-glow)" />
    <path d="M800,100 Q600,400 900,700 T300,300 Z" fill="#8b5cf6" opacity="0.1" filter="url(#deep-glow)" />

    <!-- Starfield Grid -->
    <use href="#star" x="150" y="80" />
    <use href="#star" x="350" y="120" />
    <use href="#star" x="550" y="60" />
    <use href="#star" x="750" y="150" />
    <use href="#star" x="950" y="90" />
    <use href="#star" x="1100" y="180" />
    <use href="#star" x="50" y="250" />
    <use href="#star" x="250" y="320" />
    <use href="#star" x="650" y="280" />
    <use href="#star" x="850" y="350" />
    <use href="#star" x="150" y="450" />
    <use href="#star" x="450" y="520" />
    <use href="#star" x="1050" y="480" />
    <use href="#star" x="350" y="650" />
    <use href="#star" x="750" y="720" />
    <use href="#star" x="950" y="620" />

    <!-- Black Hole / Portal Center -->
    <g transform="translate(300, 320)" filter="url(#deep-glow)">
      <circle r="90" fill="#000000" stroke="#3b82f6" stroke-width="2" opacity="0.9" />
      <circle r="110" fill="none" stroke="#06b6d4" stroke-width="1.5" stroke-dasharray="10 15">
        <animateTransform attributeName="transform" type="rotate" from="0" to="360" dur="20s" repeatCount="indefinite" />
      </circle>
      <circle r="130" fill="none" stroke="#a855f7" stroke-width="1" stroke-dasharray="5 25">
        <animateTransform attributeName="transform" type="rotate" from="360" to="0" dur="15s" repeatCount="indefinite" />
      </circle>
    </g>

    <!-- Sci-Fi HUD Frame Borders -->
    <path d="M 40,40 L 120,40 L 140,70 L 1160,70 L 1160,760 L 40,760 Z" fill="none" stroke="#3b82f6" stroke-width="1.5" opacity="0.4" />
    <path d="M 60,20 L 200,20 L 220,50 L 1140,50" fill="none" stroke="#06b6d4" stroke-width="2" opacity="0.7" />
    
    <!-- Corner Tech Accents -->
    <path d="M 30,60 L 30,30 L 60,30" fill="none" stroke="#06b6d4" stroke-width="3" filter="url(#glow)" />
    <path d="M 1170,60 L 1170,30 L 1140,30" fill="none" stroke="#06b6d4" stroke-width="3" filter="url(#glow)" />
    <path d="M 30,740 L 30,770 L 60,770" fill="none" stroke="#06b6d4" stroke-width="3" filter="url(#glow)" />
    <path d="M 1170,740 L 1170,770 L 1140,770" fill="none" stroke="#06b6d4" stroke-width="3" filter="url(#glow)" />

    <!-- Sidebar Navigation HUD -->
    <g transform="translate(60, 180)">
      <rect x="0" y="0" width="45" height="320" rx="6" fill="#05020a" stroke="#3b82f6" stroke-width="1" opacity="0.8" />
      <!-- Nav Items -->
      <g transform="translate(12, 20)" fill="#06b6d4">
        <!-- HOME -->
        <path d="M10,0 L20,10 L15,10 L15,20 L5,20 L5,10 L0,10 Z" />
      </g>
      <g transform="translate(12, 80)" fill="#a855f7">
        <!-- ABOUT -->
        <circle cx="10" cy="7" r="5" /><path d="M2,18 C2,13 6,12 10,12 C14,12 18,13 18,18" />
      </g>
      <g transform="translate(12, 140)" fill="#a855f7">
        <!-- SKILLS -->
        <polygon points="10,0 20,6 20,16 10,22 0,16 0,6" fill="none" stroke="#a855f7" stroke-width="2" />
      </g>
      <g transform="translate(12, 200)" fill="#a855f7">
        <!-- STATS -->
        <rect x="0" y="10" width="4" height="10" /><rect x="6" y="4" width="4" height="16" /><rect x="12" y="0" width="4" height="20" />
      </g>
      <g transform="translate(12, 260)" fill="#a855f7">
        <!-- CONNECT -->
        <circle cx="10" cy="10" r="8" fill="none" stroke="#a855f7" stroke-width="2" /><circle cx="10" cy="10" r="3" />
      </g>
      <!-- Active Indicator Glow -->
      <rect x="-3" y="15" width="4" height="30" rx="2" fill="#06b6d4" filter="url(#glow)" />
    </g>

    <!-- Hero Typography & Titles -->
    <g transform="translate(520, 180)">
      <text x="0" y="30" font-family="monospace" font-size="16" fill="#06b6d4" letter-spacing="4" filter="url(#glow)">MAURYA C R</text>
      <text x="0" y="105" font-family="system-ui, -apple-system, sans-serif" font-weight="900" font-size="64" fill="#ffffff" letter-spacing="2">
        DEVELOPER
      </text>
      <text x="0" y="175" font-family="system-ui, -apple-system, sans-serif" font-weight="900" font-size="64" fill="url(#neon-purple-blue)" letter-spacing="2" filter="url(#glow)">
        EXPLORER
      </text>
      
      <!-- Subtitle Badges -->
      <g transform="translate(0, 210)" font-family="monospace" font-size="12" fill="#94a3b8">
        <rect x="0" y="0" width="90" height="26" rx="4" fill="#1e1b4b" stroke="#3b82f6" stroke-width="1" />
        <text x="45" y="17" text-anchor="middle" fill="#38bdf8">AI</text>

        <rect x="100" y="0" width="130" height="26" rx="4" fill="#1e1b4b" stroke="#3b82f6" stroke-width="1" />
        <text x="165" y="17" text-anchor="middle" fill="#38bdf8">CYBERSECURITY</text>

        <rect x="240" y="0" width="110" height="26" rx="4" fill="#1e1b4b" stroke="#3b82f6" stroke-width="1" />
        <text x="295" y="17" text-anchor="middle" fill="#38bdf8">FULL STACK</text>
      </g>
    </g>

    <!-- Portal CTA Button -->
    <g transform="translate(880, 80)" filter="url(#glow)">
      <rect x="0" y="0" width="160" height="40" rx="6" fill="#0f172a" stroke="#06b6d4" stroke-width="2" />
      <text x="80" y="25" text-anchor="middle" font-family="monospace" font-size="13" fill="#ffffff" font-weight="bold" letter-spacing="1">ENTER PORTAL</text>
      <circle cx="140" cy="20" r="4" fill="#06b6d4">
        <animate attributeName="opacity" values="1;0.2;1" dur="1.5s" repeatCount="indefinite" />
      </circle>
    </g>

    <!-- Solar System Timeline & Orbiting Planets (Bottom HUD) -->
    <g transform="translate(150, 680)">
      <!-- Timeline Track Line -->
      <line x1="0" y1="0" x2="900" y2="0" stroke="#3b82f6" stroke-width="2" opacity="0.5" />
      
      <!-- Timeline Nodes / Planets -->
      <!-- Mercury -->
      <g transform="translate(50, 0)">
        <circle cx="0" cy="0" r="6" fill="#94a3b8" filter="url(#glow)" />
        <text x="0" y="25" text-anchor="middle" font-family="monospace" font-size="10" fill="#64748b">HOME</text>
      </g>
      <!-- Venus -->
      <g transform="translate(160, 0)">
        <circle cx="0" cy="0" r="8" fill="#f97316" filter="url(#glow)" />
        <text x="0" y="25" text-anchor="middle" font-family="monospace" font-size="10" fill="#64748b">ABOUT</text>
      </g>
      <!-- Earth -->
      <g transform="translate(270, 0)">
        <circle cx="0" cy="0" r="10" fill="#3b82f6" filter="url(#glow)" />
        <text x="0" y="25" text-anchor="middle" font-family="monospace" font-size="10" fill="#38bdf8" font-weight="bold">SKILLS</text>
        <circle cx="0" cy="0" r="14" fill="none" stroke="#06b6d4" stroke-width="1" stroke-dasharray="2 2">
          <animateTransform attributeName="transform" type="rotate" from="0" to="360" dur="10s" repeatCount="indefinite" />
        </circle>
      </g>
      <!-- Mars -->
      <g transform="translate(380, 0)">
        <circle cx="0" cy="0" r="8" fill="#ef4444" filter="url(#glow)" />
        <text x="0" y="25" text-anchor="middle" font-family="monospace" font-size="10" fill="#64748b">STATS</text>
      </g>
      <!-- Jupiter -->
      <g transform="translate(490, 0)">
        <circle cx="0" cy="0" r="14" fill="#eab308" filter="url(#glow)" />
        <text x="0" y="25" text-anchor="middle" font-family="monospace" font-size="10" fill="#64748b">CONNECT</text>
      </g>
      <!-- Saturn -->
      <g transform="translate(600, 0)">
        <ellipse cx="0" cy="0" rx="18" ry="6" fill="none" stroke="#cbd5e1" stroke-width="2" transform="rotate(-20)" />
        <circle cx="0" cy="0" r="11" fill="#fde047" filter="url(#glow)" />
        <text x="0" y="25" text-anchor="middle" font-family="monospace" font-size="10" fill="#64748b">SYSTEM</text>
      </g>
      <!-- Deep Space Ship Icon moving -->
      <g transform="translate(780, -5)" filter="url(#glow)">
        <polygon points="0,0 20,-5 15,0 20,5" fill="#06b6d4" />
        <path d="M-10,0 L0,-3 L0,3 Z" fill="#3b82f6" />
        <text x="10" y="25" text-anchor="middle" font-family="monospace" font-size="10" fill="#06b6d4">EXPLORING</text>
      </g>
    </g>

    <!-- Scroll Indicator -->
    <g transform="translate(560, 610)">
      <rect x="0" y="0" width="80" height="22" rx="11" fill="#020617" stroke="#3b82f6" stroke-width="1" opacity="0.8" />
      <circle cx="12" cy="11" r="3" fill="#06b6d4">
        <animate attributeName="cy" values="8;14;8" dur="1.5s" repeatCount="indefinite" />
      </circle>
      <text x="46" y="15" text-anchor="middle" font-family="monospace" font-size="9" fill="#94a3b8" letter-spacing="1">SCROLL</text>
    </g>
  </svg>
</div>

---

## 🛰️ SYSTEM NAVIGATION & TELEMETRY

<div align="center">
  <a href="https://github.com/maurya-03"><img src="https://img.shields.io/badge/GITHUB-MATRIX-0f172a?style=for-the-badge&logo=github&logoColor=06b6d4&color=1e1b4b" alt="GitHub"></a>
  <a href="https://www.linkedin.com/in/maurya-c-r-20495b296"><img src="https://img.shields.io/badge/LINKEDIN-UPLINK-0f172a?style=for-the-badge&logo=linkedin&logoColor=3b82f6&color=1e1b4b" alt="LinkedIn"></a>
  <a href="mailto:mauryacr05@gmail.com"><img src="https://img.shields.io/badge/COMMS-SECURE-0f172a?style=for-the-badge&logo=minutemailer&logoColor=a855f7&color=1e1b4b" alt="Email"></a>
  <img src="https://img.shields.io/badge/SECTOR-BENGALURU_EARTH-0f172a?style=for-the-badge&logo=nasa&logoColor=38bdf8&color=1e1b4b" alt="Location">
</div>

---

## ⚡ 01 // IDENTITY CARD // PROFILE.EXE

<div align="center">
  <svg width="100%" height="340" viewBox="0 0 1200 340" xmlns="http://www.w3.org/2000/svg">
    <defs>
      <linearGradient id="card-bg" x1="0%" y1="0%" x2="100%" y2="100%">
        <stop offset="0%" stop-color="#090514" />
        <stop offset="100%" stop-color="#020617" />
      </linearGradient>
      <filter id="card-glow" x="-10%" y="-10%" width="120%" height="120%">
        <feGaussianBlur stdDeviation="8" result="blur" />
        <feComposite in="SourceGraphic" in2="blur" operator="over" />
      </filter>
    </defs>

    <!-- Holographic Card Body -->
    <rect x="40" y="20" width="1120" height="300" rx="12" fill="url(#card-bg)" stroke="#3b82f6" stroke-width="2" filter="url(#card-glow)" opacity="0.95" />
    
    <!-- Top HUD Bar inside Card -->
    <path d="M 40,60 L 360,60 L 380,20 L 1160,20" fill="none" stroke="#06b6d4" stroke-width="1" opacity="0.4" />
    <text x="70" y="43" font-family="monospace" font-size="12" fill="#06b6d4" letter-spacing="2">>> IDENTITY CARD // SPEC-03</text>
    <circle cx="1120" cy="40" r="4" fill="#a855f7" />
    <circle cx="1100" cy="40" r="4" fill="#3b82f6" />
    <circle cx="1080" cy="40" r="4" fill="#06b6d4" />

    <!-- Avatar Frame -->
    <g transform="translate(100, 90)">
      <!-- Outer Hexagon / Circle HUD -->
      <circle cx="80" cy="80" r="75" fill="#030712" stroke="#a855f7" stroke-width="2" />
      <circle cx="80" cy="80" r="82" fill="none" stroke="#06b6d4" stroke-width="1" stroke-dasharray="6 10">
        <animateTransform attributeName="transform" type="rotate" from="0" to="360" dur="25s" repeatCount="indefinite" />
      </circle>
      <!-- Avatar Placeholder Art / Icon Container -->
      <circle cx="80" cy="80" r="68" fill="#0f172a" />
      <path d="M80,45 C62,45 48,59 48,77 C48,95 62,109 80,109 C98,109 112,95 112,77 C112,59 98,45 80,45 Z" fill="#1e1b4b" />
      <path d="M35,130 C35,108 55,98 80,98 C105,98 125,108 125,130 Z" fill="#3b82f6" opacity="0.8" />
    </g>

    <!-- Profile Metadata -->
    <g transform="translate(290, 105)">
      <text x="0" y="0" font-family="system-ui, sans-serif" font-weight="900" font-size="28" fill="#ffffff" letter-spacing="1">MAURYA C R</text>
      <text x="0" y="24" font-family="monospace" font-size="13" fill="#38bdf8" letter-spacing="1">Full Stack Developer & AI Enthusiast</text>
      
      <!-- Grid Stats inside Card -->
      <g transform="translate(0, 50)" font-family="monospace" font-size="11">
        <text x="0" y="0" fill="#64748b">LOCATION</text>
        <text x="0" y="16" fill="#f8fafc">Bengaluru, India 🇮🇳</text>

        <text x="180" y="0" fill="#64748b">STATUS</text>
        <text x="180" y="16" fill="#22c55e">● Always Building</text>

        <text x="360" y="0" fill="#64748b">EXPERIENCE</text>
        <text x="360" y="16" fill="#a855f7">Systems & AI Engineering</text>
      </g>

      <!-- Mission Statement Bar -->
      <g transform="translate(0, 110)">
        <rect x="0" y="0" width="460" height="360" fill="transparent" />
        <text x="0" y="0" font-family="monospace" font-size="11" fill="#64748b">MISSION</text>
        <text x="0" y="18" font-family="monospace" font-size="12" fill="#06b6d4">Code. Secure. Innovate. Solve Real-World Problems.</text>
      </g>
    </g>

    <!-- Terminal Code Window on Right -->
    <g transform="translate(780, 95)">
      <rect x="0" y="0" width="340" height="190" rx="6" fill="#020617" stroke="#3b82f6" stroke-width="1" />
      <rect x="0" y="0" width="340" height="24" fill="#0f172a" rx="6" />
      <text x="15" y="16" font-family="monospace" font-size="10" fill="#38bdf8">INITIALIZING_PROFILE.EXE</text>
      
      <!-- Terminal Output Lines -->
      <text x="15" y="48" font-family="monospace" font-size="11" fill="#22c55e">> WHO_AM_I:</text>
      <text x="15" y="68" font-family="monospace" font-size="10" fill="#cbd5e1">Computer Science student passionate</text>
      <text x="15" y="84" font-family="monospace" font-size="10" fill="#cbd5e1">about secure, scalable full-stack apps.</text>
      
      <text x="15" y="114" font-family="monospace" font-size="11" fill="#38bdf8">> CORE_STACK:</text>
      <text x="15" y="132" font-family="monospace" font-size="10" fill="#cbd5e1">Next.js, TypeScript, Python, Node.js,</text>
      <text x="15" y="148" font-family="monospace" font-size="10" fill="#cbd5e1">MongoDB, Tailwind & Cybersecurity labs.</text>
      
      <text x="15" y="172" font-family="monospace" font-size="10" fill="#a855f7">> STATUS: READY FOR DEPLOYMENT_</text>
    </g>
  </svg>
</div>

---

## ⚡ 02 // TECH ARSENAL // SKILL MATRIX

<div align="center">
  <svg width="100%" height="220" viewBox="0 0 1200 220" xmlns="http://www.w3.org/2000/svg">
    <defs>
      <filter id="hex-glow" x="-20%" y="-20%" width="140%" height="140%">
        <feGaussianBlur stdDeviation="5" result="blur" />
        <feComposite in="SourceGraphic" in2="blur" operator="over" />
      </filter>
    </defs>

    <!-- Background Grid Pane -->
    <rect x="40" y="10" width="1120" height="200" rx="10" fill="#05020a" stroke="#1e1b4b" stroke-width="2" />

    <!-- Hexagonal Skill Nodes -->
    <!-- Node 1: JavaScript -->
    <g transform="translate(100, 80)" filter="url(#hex-glow)">
      <polygon points="40,0 80,23 80,69 40,92 0,69 0,23" fill="#0f172a" stroke="#facc15" stroke-width="2" />
      <text x="40" y="52" text-anchor="middle" font-family="monospace" font-size="12" fill="#facc15" font-weight="bold">JS</text>
      <text x="40" y="115" text-anchor="middle" font-family="monospace" font-size="11" fill="#94a3b8">JavaScript</text>
    </g>

    <!-- Node 2: TypeScript -->
    <g transform="translate(220, 80)" filter="url(#hex-glow)">
      <polygon points="40,0 80,23 80,69 40,92 0,69 0,23" fill="#0f172a" stroke="#3b82f6" stroke-width="2" />
      <text x="40" y="52" text-anchor="middle" font-family="monospace" font-size="12" fill="#3b82f6" font-weight="bold">TS</text>
      <text x="40" y="115" text-anchor="middle" font-family="monospace" font-size="11" fill="#94a3b8">TypeScript</text>
    </g>

    <!-- Node 3: React -->
    <g transform="translate(340, 80)" filter="url(#hex-glow)">
      <polygon points="40,0 80,23 80,69 40,92 0,69 0,23" fill="#0f172a" stroke="#06b6d4" stroke-width="2" />
      <text x="40" y="52" text-anchor="middle" font-family="monospace" font-size="12" fill="#06b6d4" font-weight="bold">REACT</text>
      <text x="40" y="115" text-anchor="middle" font-family="monospace" font-size="11" fill="#94a3b8">React</text>
    </g>

    <!-- Node 4: Next.js -->
    <g transform="translate(460, 80)" filter="url(#hex-glow)">
      <polygon points="40,0 80,23 80,69 40,92 0,69 0,23" fill="#0f172a" stroke="#ffffff" stroke-width="2" />
      <text x="40" y="52" text-anchor="middle" font-family="monospace" font-size="12" fill="#ffffff" font-weight="bold">NEXT</text>
      <text x="40" y="115" text-anchor="middle" font-family="monospace" font-size="11" fill="#94a3b8">Next.js</text>
    </g>

    <!-- Node 5: Node.js -->
    <g transform="translate(580, 80)" filter="url(#hex-glow)">
      <polygon points="40,0 80,23 80,69 40,92 0,69 0,23" fill="#0f172a" stroke="#22c55e" stroke-width="2" />
      <text x="40" y="52" text-anchor="middle" font-family="monospace" font-size="12" fill="#22c55e" font-weight="bold">NODE</text>
      <text x="40" y="115" text-anchor="middle" font-family="monospace" font-size="11" fill="#94a3b8">Node.js</text>
    </g>

    <!-- Node 6: Python -->
    <g transform="translate(700, 80)" filter="url(#hex-glow)">
      <polygon points="40,0 80,23 80,69 40,92 0,69 0,23" fill="#0f172a" stroke="#3b82f6" stroke-width="2" />
      <text x="40" y="52" text-anchor="middle" font-family="monospace" font-size="12" fill="#3b82f6" font-weight="bold">PY</text>
      <text x="40" y="115" text-anchor="middle" font-family="monospace" font-size="11" fill="#94a3b8">Python</text>
    </g>

    <!-- Node 7: MongoDB -->
    <g transform="translate(820, 80)" filter="url(#hex-glow)">
      <polygon points="40,0 80,23 80,69 40,92 0,69 0,23" fill="#0f172a" stroke="#22c55e" stroke-width="2" />
      <text x="40" y="52" text-anchor="middle" font-family="monospace" font-size="12" fill="#22c55e" font-weight="bold">DB</text>
      <text x="40" y="115" text-anchor="middle" font-family="monospace" font-size="11" fill="#94a3b8">MongoDB</text>
    </g>

    <!-- Node 8: Tailwind -->
    <g transform="translate(940, 80)" filter="url(#hex-glow)">
      <polygon points="40,0 80,23 80,69 40,92 0,69 0,23" fill="#0f172a" stroke="#38bdf8" stroke-width="2" />
      <text x="40" y="52" text-anchor="middle" font-family="monospace" font-size="12" fill="#38bdf8" font-weight="bold">TW</text>
      <text x="40" y="115" text-anchor="middle" font-family="monospace" font-size="11" fill="#94a3b8">Tailwind</text>
    </g>

    <!-- Node 9: Security & Git -->
    <g transform="translate(1060, 80)" filter="url(#hex-glow)">
      <polygon points="40,0 80,23 80,69 40,92 0,69 0,23" fill="#0f172a" stroke="#a855f7" stroke-width="2" />
      <text x="40" y="52" text-anchor="middle" font-family="monospace" font-size="12" fill="#a855f7" font-weight="bold">SEC</text>
      <text x="40" y="115" text-anchor="middle" font-family="monospace" font-size="11" fill="#94a3b8">Cyber / Git</text>
    </g>
  </svg>
</div>

---

## ⚡ 03 // GITHUB MATRIX // TELEMETRY STATS

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=maurya-03&show_icons=true&theme=tokyonight&hide_border=true&bg_color=05020a&title_color=38bdf8&icon_color=a855f7&text_color=94a3b8" alt="GitHub Stats" />
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=maurya-03&theme=tokyonight&hide_border=true&background=05020a&stroke=3b82f6&side_fire=38bdf8&ring=a855f7" alt="GitHub Streak" />
</div>

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=maurya-03&layout=compact&theme=tokyonight&hide_border=true&bg_color=05020a&title_color=38bdf8&text_color=94a3b8" alt="Top Languages" />
</div>

---

## ⚡ 04 // SOLAR UPLINK // CONNECT

<div align="center">
  <svg width="100%" height="280" viewBox="0 0 1200 280" xmlns="http://www.w3.org/2000/svg">
    <defs>
      <radialGradient id="sun-glow" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stop-color="#38bdf8" />
        <stop offset="50%" stop-color="#8b5cf6" />
        <stop offset="100%" stop-color="#05020a" stop-opacity="0" />
      </radialGradient>
    </defs>

    <!-- Background Dashboard Panel -->
    <rect x="40" y="10" width="1120" height="260" rx="10" fill="#05020a" stroke="#3b82f6" stroke-width="1.5" opacity="0.9" />

    <!-- Miniature Solar System Animation Center -->
    <g transform="translate(600, 140)">
      <!-- Sun Core -->
      <circle cx="0" cy="0" r="25" fill="url(#sun-glow)" filter="url(#deep-glow)" />
      <circle cx="0" cy="0" r="10" fill="#ffffff" filter="url(#glow)" />

      <!-- Orbit Rings -->
      <ellipse cx="0" cy="0" rx="120" ry="40" fill="none" stroke="#3b82f6" stroke-width="1" opacity="0.4" />
      <ellipse cx="0" cy="0" rx="200" ry="70" fill="none" stroke="#a855f7" stroke-width="1" opacity="0.4" />

      <!-- Orbiting Planets (Links) -->
      <!-- Planet 1: GitHub -->
      <g>
        <animateTransform attributeName="transform" type="rotate" from="0" to="360" dur="12s" repeatCount="indefinite" />
        <circle cx="120" cy="0" r="8" fill="#38bdf8" filter="url(#glow)" />
      </g>
      <!-- Planet 2: LinkedIn -->
      <g>
        <animateTransform attributeName="transform" type="rotate" from="180" to="540" dur="20s" repeatCount="indefinite" />
        <circle cx="-200" cy="0" r="10" fill="#a855f7" filter="url(#glow)" />
      </g>
    </g>

    <!-- Connect Terminal Cards on Sides -->
    <g transform="translate(80, 50)">
      <rect x="0" y="0" width="300" height="180" rx="6" fill="#090514" stroke="#06b6d4" stroke-width="1" />
      <text x="20" y="30" font-family="monospace" font-size="14" fill="#38bdf8" font-weight="bold">TRANSMIT SIGNAL</text>
      <text x="20" y="60" font-family="monospace" font-size="11" fill="#94a3b8">Ready for collaborations, AI</text>
      <text x="20" y="78" font-family="monospace" font-size="11" fill="#94a3b8">ventures, or security research.</text>
      
      <!-- Interactive Signal Button -->
      <g transform="translate(20, 110)">
        <rect x="0" y="0" width="160" height="360" fill="transparent" />
        <rect x="0" y="0" width="160" height="35" rx="4" fill="#1e1b4b" stroke="#38bdf8" stroke-width="1" />
        <a href="mailto:mauryacr05@gmail.com">
          <text x="80" y="22" text-anchor="middle" font-family="monospace" font-size="12" fill="#ffffff">SEND SIGNAL 🚀</text>
        </a>
      </g>
    </g>

    <!-- Quick Links Panel Right -->
    <g transform="translate(820, 50)">
      <rect x="0" y="0" width="300" height="180" rx="6" fill="#090514" stroke="#a855f7" stroke-width="1" />
      <text x="20" y="30" font-family="monospace" font-size="14" fill="#a855f7" font-weight="bold">UPLINK CHANNELS</text>
      
      <g transform="translate(20, 55)" font-family="monospace" font-size="12">
        <text x="0" y="15" fill="#64748b">GITHUB</text>
        <a href="https://github.com/maurya-03"><text x="100" y="15" fill="#38bdf8">@maurya-03 →</text></a>

        <text x="0" y="55" fill="#64748b">LINKEDIN</text>
        <a href="https://www.linkedin.com/in/maurya-c-r-20495b296"><text x="100" y="55" fill="#38bdf8">Connect →</text></a>

        <text x="0" y="95" fill="#64748b">EMAIL</text>
        <a href="mailto:mauryacr05@gmail.com"><text x="100" y="95" fill="#38bdf8">Mail →</text></a>
      </g>
    </g>
  </svg>
</div>

<div align="center">
  <p><font face="monospace" size="2" color="#64748b">© 2026 Maurya C R. All systems nominal. The journey continues...</font></p>
</div>
