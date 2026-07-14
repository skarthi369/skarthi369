<div align="center">

<!-- ╔══════════════════════════════════════════════════════════════╗
     ║  K A R T H I K E Y A N   S  —  A I   N E U R A L   C O R E  ║
     ╚══════════════════════════════════════════════════════════════╝ -->

<svg width="100%" height="280" viewBox="0 0 1200 280" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <!-- Game-level neon gradients -->
    <linearGradient id="grad1" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#00f5ff;stop-opacity:1">
        <animate attributeName="stop-color" values="#00f5ff;#7c3aed;#f472b6;#00f5ff" dur="6s" repeatCount="indefinite"/>
      </stop>
      <stop offset="50%" style="stop-color:#7c3aed;stop-opacity:1">
        <animate attributeName="stop-color" values="#7c3aed;#f472b6;#00f5ff;#7c3aed" dur="6s" repeatCount="indefinite"/>
      </stop>
      <stop offset="100%" style="stop-color:#f472b6;stop-opacity:1">
        <animate attributeName="stop-color" values="#f472b6;#00f5ff;#7c3aed;#f472b6" dur="6s" repeatCount="indefinite"/>
      </stop>
    </linearGradient>
    <linearGradient id="grad2" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" style="stop-color:#00f5ff;stop-opacity:0"/>
      <stop offset="50%" style="stop-color:#00f5ff;stop-opacity:0.6"/>
      <stop offset="100%" style="stop-color:#00f5ff;stop-opacity:0"/>
    </linearGradient>
    <!-- Neon glow filter -->
    <filter id="neon" x="-50%" y="-50%" width="200%" height="200%">
      <feGaussianBlur stdDeviation="4" result="blur"/>
      <feMerge>
        <feMergeNode in="blur"/>
        <feMergeNode in="blur"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>
    <filter id="soft-glow" x="-50%" y="-50%" width="200%" height="200%">
      <feGaussianBlur stdDeviation="2" result="blur"/>
      <feMerge>
        <feMergeNode in="blur"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>
    <!-- Neural grid pattern -->
    <pattern id="grid" width="40" height="40" patternUnits="userSpaceOnUse">
      <path d="M 40 0 L 0 0 0 40" fill="none" stroke="rgba(0,245,255,0.08)" stroke-width="0.5"/>
    </pattern>
    <!-- Clip path for hexagon avatar -->
    <clipPath id="hexClip">
      <polygon points="100,20 170,55 170,125 100,160 30,125 30,55"/>
    </clipPath>
  </defs>

  <!-- Dark background with grid -->
  <rect width="100%" height="100%" fill="#0a0a0f"/>
  <rect width="100%" height="100%" fill="url(#grid)"/>

  <!-- Animated neural nodes -->
  <g id="nodes">
    <circle cx="80" cy="60" r="2.5" fill="#00f5ff" opacity="0.8">
      <animate attributeName="opacity" values="0.3;1;0.3" dur="3s" repeatCount="indefinite"/>
      <animate attributeName="r" values="2;4;2" dur="3s" repeatCount="indefinite"/>
    </circle>
    <circle cx="1120" cy="220" r="2.5" fill="#f472b6" opacity="0.8">
      <animate attributeName="opacity" values="0.3;1;0.3" dur="2.5s" repeatCount="indefinite"/>
      <animate attributeName="r" values="2;4;2" dur="2.5s" repeatCount="indefinite"/>
    </circle>
    <circle cx="150" cy="240" r="2" fill="#7c3aed" opacity="0.6">
      <animate attributeName="opacity" values="0.2;0.9;0.2" dur="4s" repeatCount="indefinite"/>
    </circle>
    <circle cx="1050" cy="50" r="2" fill="#00f5ff" opacity="0.6">
      <animate attributeName="opacity" values="0.2;0.9;0.2" dur="3.5s" repeatCount="indefinite"/>
    </circle>
    <circle cx="300" cy="40" r="1.5" fill="#f472b6" opacity="0.5">
      <animate attributeName="opacity" values="0.1;0.7;0.1" dur="2.8s" repeatCount="indefinite"/>
    </circle>
    <circle cx="900" cy="250" r="1.5" fill="#7c3aed" opacity="0.5">
      <animate attributeName="opacity" values="0.1;0.7;0.1" dur="3.2s" repeatCount="indefinite"/>
    </circle>
  </g>

  <!-- Animated neural connections -->
  <g stroke-width="0.8" opacity="0.3">
    <line x1="80" y1="60" x2="150" y2="240" stroke="#00f5ff">
      <animate attributeName="opacity" values="0.1;0.5;0.1" dur="3s" repeatCount="indefinite"/>
    </line>
    <line x1="1120" y1="220" x2="1050" y2="50" stroke="#f472b6">
      <animate attributeName="opacity" values="0.1;0.5;0.1" dur="2.5s" repeatCount="indefinite"/>
    </line>
    <line x1="300" y1="40" x2="80" y2="60" stroke="#7c3aed">
      <animate attributeName="opacity" values="0.1;0.4;0.1" dur="4s" repeatCount="indefinite"/>
    </line>
    <line x1="900" y1="250" x2="1120" y2="220" stroke="#00f5ff">
      <animate attributeName="opacity" values="0.1;0.4;0.1" dur="3.5s" repeatCount="indefinite"/>
    </line>
  </g>

  <!-- Animated corner brackets -->
  <g stroke="#00f5ff" stroke-width="2" fill="none" filter="url(#neon)">
    <!-- Top-left -->
    <path d="M 40 80 L 40 40 L 80 40">
      <animate attributeName="opacity" values="0.4;1;0.4" dur="2s" repeatCount="indefinite"/>
    </path>
    <!-- Top-right -->
    <path d="M 1120 40 L 1160 40 L 1160 80">
      <animate attributeName="opacity" values="0.4;1;0.4" dur="2.2s" repeatCount="indefinite"/>
    </path>
    <!-- Bottom-left -->
    <path d="M 40 200 L 40 240 L 80 240">
      <animate attributeName="opacity" values="0.4;1;0.4" dur="2.4s" repeatCount="indefinite"/>
    </path>
    <!-- Bottom-right -->
    <path d="M 1120 240 L 1160 240 L 1160 200">
      <animate attributeName="opacity" values="0.4;1;0.4" dur="1.8s" repeatCount="indefinite"/>
    </path>
  </g>

  <!-- Scanning line animation -->
  <line x1="0" y1="0" x2="1200" y2="0" stroke="url(#grad2)" stroke-width="2" opacity="0.6">
    <animateTransform attributeName="transform" type="translate" values="0,0; 0,280; 0,0" dur="8s" repeatCount="indefinite"/>
  </line>

  <!-- HEXAGON AVATAR FRAME -->
  <g transform="translate(60, 50)">
    <!-- Outer hexagon glow -->
    <polygon points="100,10 180,50 180,130 100,170 20,130 20,50" fill="none" stroke="url(#grad1)" stroke-width="3" filter="url(#neon)">
      <animateTransform attributeName="transform" type="rotate" values="0 100 90; 360 100 90" dur="30s" repeatCount="indefinite"/>
    </polygon>
    <!-- Inner hexagon -->
    <polygon points="100,25 165,55 165,125 100,155 35,125 35,55" fill="none" stroke="rgba(0,245,255,0.3)" stroke-width="1"/>
    <!-- Avatar placeholder with initials -->
    <circle cx="100" cy="90" r="45" fill="rgba(124,58,237,0.15)" stroke="#7c3aed" stroke-width="1"/>
    <text x="100" y="105" text-anchor="middle" font-family="monospace" font-size="32" font-weight="bold" fill="url(#grad1)">KS</text>
    <!-- Orbiting dot -->
    <circle r="4" fill="#00f5ff" filter="url(#neon)">
      <animateMotion path="M100,10 L180,50 L180,130 L100,170 L20,130 L20,50 Z" dur="8s" repeatCount="indefinite"/>
    </circle>
  </g>

  <!-- MAIN TITLE with typing animation -->
  <text x="280" y="85" font-family="'Courier New', monospace" font-size="38" font-weight="bold" fill="#e2e8f0" filter="url(#soft-glow)">
    KARTHIKEYAN S
    <animate attributeName="opacity" values="0;1" dur="0.5s" fill="freeze"/>
  </text>

  <!-- Subtitle -->
  <text x="280" y="115" font-family="'Courier New', monospace" font-size="14" fill="#94a3b8">
    <tspan fill="#00f5ff">&#60;AI_Engineer&#62;</tspan>
    <tspan>  Neural Core Active  </tspan>
    <tspan fill="#f472b6">&#60;/AI_Engineer&#62;</tspan>
    <animate attributeName="opacity" values="0;1" dur="0.8s" fill="freeze"/>
  </text>

  <!-- ROLE BADGES -->
  <g transform="translate(280, 140)">
    <!-- Badge 1 -->
    <rect x="0" y="0" width="200" height="28" rx="14" fill="rgba(0,245,255,0.08)" stroke="#00f5ff" stroke-width="1" opacity="0.9"/>
    <text x="100" y="19" text-anchor="middle" font-family="monospace" font-size="11" fill="#00f5ff">LLM SECURITY RESEARCHER</text>

    <!-- Badge 2 -->
    <rect x="215" y="0" width="160" height="28" rx="14" fill="rgba(244,114,182,0.08)" stroke="#f472b6" stroke-width="1" opacity="0.9"/>
    <text x="295" y="19" text-anchor="middle" font-family="monospace" font-size="11" fill="#f472b6">GEN-AI ARCHITECT</text>

    <!-- Badge 3 -->
    <rect x="390" y="0" width="140" height="28" rx="14" fill="rgba(124,58,237,0.08)" stroke="#7c3aed" stroke-width="1" opacity="0.9"/>
    <text x="460" y="19" text-anchor="middle" font-family="monospace" font-size="11" fill="#7c3aed">3x HACKATHON CHAMP</text>
  </g>

  <!-- STATUS INDICATORS -->
  <g transform="translate(280, 190)">
    <!-- Pulsing status dot -->
    <circle cx="8" cy="8" r="5" fill="#22c55e">
      <animate attributeName="r" values="4;7;4" dur="2s" repeatCount="indefinite"/>
      <animate attributeName="opacity" values="1;0.4;1" dur="2s" repeatCount="indefinite"/>
    </circle>
    <text x="22" y="13" font-family="monospace" font-size="12" fill="#22c55e">SYSTEM ONLINE</text>

    <text x="180" y="13" font-family="monospace" font-size="12" fill="#94a3b8">|</text>

    <circle cx="200" cy="8" r="4" fill="#00f5ff" opacity="0.8">
      <animate attributeName="opacity" values="0.3;1;0.3" dur="1.5s" repeatCount="indefinite"/>
    </circle>
    <text x="212" y="13" font-family="monospace" font-size="12" fill="#00f5ff">CDAC ACTIVE</text>

    <text x="350" y="13" font-family="monospace" font-size="12" fill="#94a3b8">|</text>

    <circle cx="370" cy="8" r="4" fill="#f472b6" opacity="0.8">
      <animate attributeName="opacity" values="0.3;1;0.3" dur="2.5s" repeatCount="indefinite"/>
    </circle>
    <text x="382" y="13" font-family="monospace" font-size="12" fill="#f472b6">ICACT 2026</text>
  </g>

  <!-- Bottom stats bar -->
  <g transform="translate(280, 225)">
    <text x="0" y="15" font-family="monospace" font-size="11" fill="#64748b">
      <tspan fill="#00f5ff">NEURAL.PARAMS:</tspan> 653K+ <tspan fill="#94a3b8">|</tspan> 
      <tspan fill="#f472b6" dx="10">ACCURACY:</tspan> 88% <tspan fill="#94a3b8">|</tspan> 
      <tspan fill="#7c3aed" dx="10">PAPERS:</tspan> 1 <tspan fill="#94a3b8">|</tspan> 
      <tspan fill="#22c55e" dx="10">TROPHIES:</tspan> 3x
    </text>
  </g>

  <!-- Animated bottom border line -->
  <line x1="280" y1="250" x2="280" y2="250" stroke="url(#grad1)" stroke-width="2" filter="url(#neon)">
    <animate attributeName="x2" values="280;1100" dur="1.5s" fill="freeze"/>
  </line>
</svg>

<!-- ═══════════════════════════════════════════════════════════════ -->

<br/>

<!-- TYPING ANIMATION INTRO -->
<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&pause=800&color=00F5FF&center=true&vCenter=true&width=900&lines=🧠+Initializing+Neural+Network...;⚡+Loading+LLM+Security+Modules...;🔬+Activating+Generative+AI+Protocols...;🚀+System+Ready.+Welcome+to+my+Digital+Brain." alt="Typing Animation"/>
</p>

<!-- NEUROMORPHIC SOCIAL DOCK -->
<p align="center">
  <a href="https://github.com/skarthi369">
    <img src="https://img.shields.io/badge/Neural_Link-GitHub-0a0a0f?style=for-the-badge&logo=github&logoColor=00f5ff&labelColor=0f172a&color=0a0a0f&borderColor=00f5ff" alt="GitHub"/>
  </a>
  <a href="https://linkedin.com/in/karthikeyan-s">
    <img src="https://img.shields.io/badge/Neural_Link-LinkedIn-0a0a0f?style=for-the-badge&logo=linkedin&logoColor=7c3aed&labelColor=0f172a&color=0a0a0f" alt="LinkedIn"/>
  </a>
  <a href="mailto:karthikeyan123401@gmail.com">
    <img src="https://img.shields.io/badge/Neural_Link-Email-0a0a0f?style=for-the-badge&logo=gmail&logoColor=f472b6&labelColor=0f172a&color=0a0a0f" alt="Email"/>
  </a>
</p>

<!-- VISITOR COUNTER with cyber style -->
<p align="center">
  <img src="https://api.visitorbadge.io/api/visitors?path=skarthi369%2Fskarthi369&label=SYSTEM%20VISITS&countColor=%230a0a0f&style=flat-square&labelStyle=none" alt="Visitors"/>
</p>

</div>

---

<!-- ╔══════════════════════════════════════════════════════════════╗
     ║  S Y S T E M   D I A G N O S T I C S  —  A B O U T   M E   ║
     ╚══════════════════════════════════════════════════════════════╝ -->

<div align="center">

## <img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExbGtxdHRiM2FkbmZ1bWQ2dHRqY3F2d2x1Y2V6Z2Z1bmd4ZHJ5eSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9cw/3kPDmoWdBpQPNhCnUG/giphy.gif" width="35"/> `SYSTEM.IDENTITY`

</div>

```yaml
neural_profile:
  identity:
    name: "Karthikeyan S"
    designation: "AI Neural Core / LLM Security Architect"
    institution: "SA Engineering College, Chennai"
    degree: "B.Tech Artificial Intelligence & Data Science"
    
  active_mission:
    role: "Generative AI Research Intern"
    organization: "CDAC — Centre for Development of Advanced Computing"
    project: "LLM-powered Autonomous Intrusion Detection & Prevention System"
    status: "🔴 LIVE"
    
  neural_stack:
    paradigm: "Full ML Lifecycle"
    pipeline: "Data Preprocessing → Model Training → Evaluation → REST API Deployment"
    
  specialization:
    primary: "Generative AI / LLM Engineering"
    toolkit: ["RAG", "Agentic AI", "LangChain", "LangGraph", "Multi-Agent Systems"]
    
  visual_cortex:
    focus: "Computer Vision & Deep Learning"
    tools: ["CNNs", "Transformers", "TensorFlow", "OpenCV"]
    
  publication:
    paper: "EDITH — Enhanced Daily Interaction & Therapeutic Hardware for Paralysis Patients"
    venue: "ICACT 2026 International Conference"
    status: "✅ Accepted & Presented"
    
  trophies:
    - "🏆 Winner — Hexaware 36-Hour National Hackathon (Enterprise AI Track)"
    - "🏆 Winner — Prompt-o-Mania Hackathon (Generative AI Track)"
    - "🏆 Winner — Sparathon: Semantic Understanding & Fine-Tuning Challenge"
    
  availability:
    seeking: ["Python Developer", "AI-ML Engineer"]
    open_to: "Collaborations on LLM Security, GenAI Agents, Computer Vision"
```

---

<!-- ╔══════════════════════════════════════════════════════════════╗
     ║  T E C H   S T A C K  —  A R S E N A L   M A T R I X       ║
     ╚══════════════════════════════════════════════════════════════╝ -->

<div align="center">

## <img src="https://media2.giphy.com/media/QssGEmpkyEOhBCb7e1/giphy.gif?cid=ecf05e47a0n3gi1bfqntqmob8g9aid1oyj2wr3ds3mg700bl&rid=giphy.gif" width="30"/> `TECH.ARSENAL`

</div>

<!-- LANGUAGES -->
<p align="center">
  <img src="https://img.shields.io/badge/Python-★★★★★-0a0a0f?style=for-the-badge&logo=python&logoColor=00f5ff&labelColor=0f172a&color=0a0a0f&borderColor=00f5ff" alt="Python"/>
  <img src="https://img.shields.io/badge/Java-★★★☆☆-0a0a0f?style=for-the-badge&logo=openjdk&logoColor=f472b6&labelColor=0f172a&color=0a0a0f" alt="Java"/>
  <img src="https://img.shields.io/badge/JavaScript-★★★★☆-0a0a0f?style=for-the-badge&logo=javascript&logoColor=facc15&labelColor=0f172a&color=0a0a0f" alt="JavaScript"/>
  <img src="https://img.shields.io/badge/TypeScript-★★★☆☆-0a0a0f?style=for-the-badge&logo=typescript&logoColor=3178c6&labelColor=0f172a&color=0a0a0f" alt="TypeScript"/>
</p>

<!-- AI/ML -->
<p align="center">
  <img src="https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white&labelColor=0a0a0f" alt="TensorFlow"/>
  <img src="https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white&labelColor=0a0a0f" alt="Scikit-Learn"/>
  <img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white&labelColor=0a0a0f" alt="OpenCV"/>
  <img src="https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white&labelColor=0a0a0f" alt="NumPy"/>
  <img src="https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white&labelColor=0a0a0f" alt="Pandas"/>
  <img src="https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white&labelColor=0a0a0f" alt="LangChain"/>
  <img src="https://img.shields.io/badge/LangGraph-00f5ff?style=flat-square&logo=langchain&logoColor=black&labelColor=0a0a0f" alt="LangGraph"/>
</p>

<!-- BACKEND / WEB -->
<p align="center">
  <img src="https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white&labelColor=0a0a0f" alt="Flask"/>
  <img src="https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white&labelColor=0a0a0f" alt="Node.js"/>
  <img src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black&labelColor=0a0a0f" alt="React"/>
  <img src="https://img.shields.io/badge/Firebase-FFCA28?style=flat-square&logo=firebase&logoColor=black&labelColor=0a0a0f" alt="Firebase"/>
  <img src="https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white&labelColor=0a0a0f" alt="Streamlit"/>
</p>

<!-- TOOLS & CLOUD -->
<p align="center">
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white&labelColor=0a0a0f" alt="Docker"/>
  <img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white&labelColor=0a0a0f" alt="Git"/>
  <img src="https://img.shields.io/badge/GCP-4285F4?style=flat-square&logo=googlecloud&logoColor=white&labelColor=0a0a0f" alt="GCP"/>
  <img src="https://img.shields.io/badge/Jupyter-F37626?style=flat-square&logo=jupyter&logoColor=white&labelColor=0a0a0f" alt="Jupyter"/>
  <img src="https://img.shields.io/badge/Ollama-ffffff?style=flat-square&logo=ollama&logoColor=black&labelColor=0a0a0f" alt="Ollama"/>
  <img src="https://img.shields.io/badge/Gemma-f472b6?style=flat-square&logo=google&logoColor=white&labelColor=0a0a0f" alt="Gemma"/>
</p>

---

<!-- ╔══════════════════════════════════════════════════════════════╗
     ║  F E A T U R E D   P R O J E C T S  —  M I S S I O N S      ║
     ╚══════════════════════════════════════════════════════════════╝ -->

<div align="center">

## <img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExZGVubnJ6YmRzb2Nhd2R1cWE3a3VqZ3Z1aGJ5d2J4Z3J5eSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9cw/Ll22OhMLAlVDb8UQAX/giphy.gif" width="35"/> `FEATURED.MISSIONS`

</div>

<!-- ═══ MISSION 01: AI FIREWALL ═══ -->
<table>
<tr>
<td width="100%">

### 🛡️ `MISSION.01` — AI Firewall: LLM-powered IDS/IPS

```
┌─────────────────────────────────────────────────────────────────┐
│  [TRAFFIC] → [Feature Extraction] → [Hybrid Retrieval]         │
│                                              ↓                  │
│  [Embeddings + Keyword Search] → [LLM Classifier] → [ACTION]   │
│                                              ↓                  │
│                                    [BLOCK] / [ALLOW]            │
└─────────────────────────────────────────────────────────────────┘
```

**Stack:** `Python · LLMs · Docker · Dense Vector Embeddings · REST APIs · Cybersecurity AI`

> Production-grade autonomous intrusion detection & prevention system exposed via REST APIs. Combines dense vector embeddings with keyword search in a hybrid retrieval pipeline for contextual threat intelligence, then hands the result to an LLM for real-time classification. Containerized and deployed with Docker.

**Status:** `● OPERATIONAL`

</td>
</tr>
</table>

<!-- ═══ MISSION 02: DEEPFAKE DETECTION ═══ -->
<table>
<tr>
<td width="100%">

### 🔍 `MISSION.02` — Deepfake Detection System: CNN-Transformer Hybrid

```
┌─────────────────────────────────────────────────────────────────┐
│  INPUT → [OpenCV Preprocessing] → [10-Layer Deep CNN]           │
│              ↓                         ↓                        │
│     [Transformer Features] ← [653K+ Parameters]                │
│              ↓                                                  │
│     [Binary Classifier] → 88% Validation Accuracy               │
└─────────────────────────────────────────────────────────────────┘
```

**Stack:** `TensorFlow · CNN · Transformers · OpenCV · Computer Vision`

> 10-layer deep CNN with 653K+ parameters achieving ~88% validation accuracy on binary deepfake classification, extended with Transformer-based feature extraction and OpenCV preprocessing for robust image analysis.

**Status:** `● OPERATIONAL`

</td>
</tr>
</table>

<!-- ═══ MISSION 03: MINDFULCHAT ═══ -->
<table>
<tr>
<td width="100%">

### 💬 `MISSION.03` — MindfulChat: Emotion-Aware AI Mental Wellness

```
┌──────────────────────────────────────────────────────────────────┐
│                    5-AGENT ARCHITECTURE                           │
│  ┌─────────┐  ┌─────────┐  ┌─────────┐  ┌─────────┐  ┌────────┐│
│  │ Emotion │→ │  Risk   │→ │ Therapy │→ │ Memory  │→ │ Report ││
│  │  Agent  │  │  Agent  │  │  Agent  │  │  Agent  │  │  Agent ││
│  └─────────┘  └─────────┘  └─────────┘  └─────────┘  └────────┘│
│       ↑             ↑            ↑            ↑           ↑     │
│       └─────────────┴────────────┴────────────┴───────────┘     │
│                          USER INPUT                               │
└──────────────────────────────────────────────────────────────────┘
```

**Stack:** `React · TypeScript · Ollama · Gemma · NLP`

> Full-stack, privacy-first chatbot running a locally hosted LLM, with emotion recognition, sentiment analysis, and a 5-agent architecture.

**Status:** `● OPERATIONAL`

</td>
</tr>
</table>

<!-- ═══ MISSION 04-06 COMPACT ═══ -->
<table>
<tr>
<td width="33%">

#### 🎣 `MISSION.04` Phishing URL Detection
`Python · Streamlit · Scikit-Learn`

ML-based phishing detector with entropy analysis, SSL validation, and brand impersonation checks.

</td>
<td width="33%">

#### 🌦️ `MISSION.05` Agentic Weather Prediction
`Python · Streamlit · LSTM · RNN · GNN`

Autonomous forecasting with reinforcement learning and real-time satellite data integration.

</td>
<td width="33%">

#### 🧩 `MISSION.06` Multi-Agent Orchestration
`Python · AsyncIO · LangGraph`

Planner-executor-reviewer workflows with dynamic routing and checkpoint recovery.

</td>
</tr>
</table>

---

<!-- ╔══════════════════════════════════════════════════════════════╗
     ║  E X P E R I E N C E  —  T I M E L I N E                    ║
     ╚══════════════════════════════════════════════════════════════╝ -->

<div align="center">

## <img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExZGVubnJ6YmRzb2Nhd2R1cWE3a3VqZ3Z1aGJ5d2J4Z3J5eSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9cw/WFZvB7VIXBgiz3oDXE/giphy.gif" width="30"/> `EXPERIENCE.TIMELINE`

</div>

```
2025 ───●────────────────────────────────────────────────────────── NOW
         │
         ▼
    ┌──────────────────────────────────────────────────────────────────────┐
    │  🏢 CDAC — Centre for Development of Advanced Computing              │
    │     ROLE: Generative AI Research Intern                              │
    │     STATUS: 🔴 LIVE — LLM-powered IDS/IPS Development               │
    │     PERIOD: 2025 – Present                                           │
    └──────────────────────────────────────────────────────────────────────┘
         │
2024 ───┼───●──────────────●─────────────────────────────────────────────
         │   │              │
         ▼   ▼              ▼
    ┌──────────┐      ┌──────────────────────────────────────────────┐
    │ Resolute │      │ CED — Centre for Entrepreneurship Development  │
    │    AI    │      │ ROLE: AI & IoT Research Intern                │
    │ AI & DL  │      │ PERIOD: 2024                                │
    │  Intern  │      └──────────────────────────────────────────────┘
    └──────────┘
    
2023 ────────────────────────────────────────────────────────────────────

2023 ─────────────────────●──────────────────────────────────────────────
                          │
                          ▼
                   ┌──────────────────────────────────────────────┐
                   │ Microsoft × Edunet Foundation × AICTE         │
                   │ ROLE: Foundations of AI Intern               │
                   │ PERIOD: Apr – May 2025                        │
                   └──────────────────────────────────────────────┘
```

---

<!-- ╔══════════════════════════════════════════════════════════════╗
     ║  R E S E A R C H  —  P U B L I C A T I O N   C A R D       ║
     ╚══════════════════════════════════════════════════════════════╝ -->

<div align="center">

## <img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExZGVubnJ6YmRzb2Nhd2R1cWE3a3VqZ3Z1aGJ5d2J4Z3J5eSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9cw/3oKIP8kNuTJJL3zT0I/giphy.gif" width="30"/> `RESEARCH.PUBLICATION`

</div>

<p align="center">
  <img src="https://img.shields.io/badge/ICACT_2026-Accepted_&_Presented-22c55e?style=for-the-badge&labelColor=0f172a" alt="ICACT 2026"/>
  <img src="https://img.shields.io/badge/Peer_Reviewed-Yes-00f5ff?style=for-the-badge&labelColor=0f172a" alt="Peer Reviewed"/>
  <img src="https://img.shields.io/badge/DOI-Coming_Soon-f472b6?style=for-the-badge&labelColor=0f172a" alt="DOI"/>
</p>

```asciidoc
╔══════════════════════════════════════════════════════════════════════════╗
║                                                                          ║
║   EDITH: Enhanced Daily Interaction and Therapeutic Hardware             ║
║          for Paralysis Patient Support                                   ║
║                                                                          ║
║   ┌─────────────────────────────────────────────────────────────────┐     ║
║   │  • AI-assisted modular robotics platform                         │     ║
║   │  • Biosignal monitoring integration                              │     ║
║   │  • Mobility assistance systems                                   │     ║
║   │  • Rehabilitation support modules                                │     ║
║   │  • Brain-Computer Interface (BCI) integration pathway            │     ║
║   └─────────────────────────────────────────────────────────────────┘     ║
║                                                                          ║
║   Venue: ICACT 2026 International Conference                             ║
║   Status: ✅ ACCEPTED & PRESENTED                                        ║
║                                                                          ║
╚══════════════════════════════════════════════════════════════════════════╝
```

---

<!-- ╔══════════════════════════════════════════════════════════════╗
     ║  T R O P H Y   C A B I N E T                                  ║
     ╚══════════════════════════════════════════════════════════════╝ -->

<div align="center">

## <img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExZGVubnJ6YmRzb2Nhd2R1cWE3a3VqZ3Z1aGJ5d2J4Z3J5eSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9cw/l4FGuhL4U2WyjcgoM/giphy.gif" width="35"/> `TROPHY.CABINET`

</div>

<table align="center">
<tr>
<td align="center" width="33%">

### 🥇
**Hexaware 36-Hour National Hackathon**
`Enterprise AI Track — WINNER`
<img src="https://img.shields.io/badge/Tier-National-gold?style=flat-square" alt="National"/>

</td>
<td align="center" width="33%">

### 🥇
**Prompt-o-Mania Hackathon**
`Generative AI Track — WINNER`
<img src="https://img.shields.io/badge/Tier-National-gold?style=flat-square" alt="National"/>

</td>
<td align="center" width="33%">

### 🥇
**Sparathon Challenge**
`Semantic Understanding & Fine-Tuning — WINNER`
<img src="https://img.shields.io/badge/Tier-National-gold?style=flat-square" alt="National"/>

</td>
</tr>
</table>

---

<!-- ╔══════════════════════════════════════════════════════════════╗
     ║  C E R T I F I C A T I O N S                                  ║
     ╚══════════════════════════════════════════════════════════════╝ -->

<div align="center">

## <img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExZGVubnJ6YmRzb2Nhd2R1cWE3a3VqZ3Z1aGJ5d2J4Z3J5eSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9cw/JIX9t2j0ZTN9S/giphy.gif" width="30"/> `CERTIFICATIONS.LOG`

</div>

<p align="center">
  <img src="https://img.shields.io/badge/Google-5--Day_AI_Agents_Intensive-4285F4?style=flat-square&logo=google&logoColor=white&labelColor=0a0a0f" alt="Google AI Agents"/>
  <img src="https://img.shields.io/badge/Microsoft-Foundations_of_AI-00A4EF?style=flat-square&logo=microsoft&logoColor=white&labelColor=0a0a0f" alt="Microsoft AI"/>
  <img src="https://img.shields.io/badge/Informatica-Data_Engineering_Foundation-FF4B4B?style=flat-square&logo=informatica&logoColor=white&labelColor=0a0a0f" alt="Informatica"/>
  <img src="https://img.shields.io/badge/Udemy-Git_&_GitHub-A435F0?style=flat-square&logo=udemy&logoColor=white&labelColor=0a0a0f" alt="Udemy Git"/>
  <img src="https://img.shields.io/badge/Infosys-Applied_Generative_AI-007CC3?style=flat-square&logo=infosys&logoColor=white&labelColor=0a0a0f" alt="Infosys GenAI"/>
</p>

---

<!-- ╔══════════════════════════════════════════════════════════════╗
     ║  G I T H U B   S T A T S  —  A N A L Y T I C S   D A S H    ║
     ╚══════════════════════════════════════════════════════════════╝ -->

<div align="center">

## <img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExZGVubnJ6YmRzb2Nhd2R1cWE3a3VqZ3Z1aGJ5d2J4Z3J5eSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9cw/W5eoZHPpUx9sapR0eu/giphy.gif" width="30"/> `GITHUB.ANALYTICS`

</div>

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=skarthi369&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0a0a0f&title_color=00f5ff&icon_color=f472b6&text_color=e2e8f0&border_radius=12" alt="GitHub Stats" height="180"/>
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=skarthi369&layout=compact&theme=tokyonight&hide_border=true&bg_color=0a0a0f&title_color=00f5ff&text_color=e2e8f0&border_radius=12" alt="Top Languages" height="180"/>
</p>

<p align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=skarthi369&theme=tokyonight&hide_border=true&background=0a0a0f&stroke=00f5ff&ring=f472b6&fire=f472b6&currStreakNum=00f5ff&sideNums=e2e8f0&currStreakLabel=00f5ff&sideLabels=94a3b8&dates=64748b&border_radius=12" alt="GitHub Streak" width="70%"/>
</p>

<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=skarthi369&theme=tokyo-night&hide_border=true&bg_color=0a0a0f&color=00f5ff&line=f472b6&point=7c3aed&area=true&area_color=f472b6" alt="Contribution Graph" width="95%"/>
</p>

---

<!-- ╔══════════════════════════════════════════════════════════════╗
     ║  T R O P H Y   S H O W C A S E                                ║
     ╚══════════════════════════════════════════════════════════════╝ -->

<div align="center">

## <img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExZGVubnJ6YmRzb2Nhd2R1cWE3a3VqZ3Z1aGJ5d2J4Z3J5eSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9cw/26ufnwz3wDUli7GU0/giphy.gif" width="30"/> `GITHUB.TROPHIES`

</div>

<p align="center">
  <img src="https://github-profile-trophy.vercel.app/?username=skarthi369&theme=tokyonight&no-frame=true&column=7&margin-w=10&margin-h=10&bg_color=0a0a0f&title_color=00f5ff&icon_color=f472b6" alt="GitHub Trophies" width="100%"/>
</p>

---

<!-- ╔══════════════════════════════════════════════════════════════╗
     ║  C O N N E C T  —  N E U R A L   U P L I N K                 ║
     ╚══════════════════════════════════════════════════════════════╝ -->

<div align="center">

## <img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExZGVubnJ6YmRzb2Nhd2R1cWE3a3VqZ3Z1aGJ5d2J4Z3J5eSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9cw/l41lUjUgLLwWrz20U/giphy.gif" width="35"/> `NEURAL.UPLINK`

<br/>

<a href="https://linkedin.com/in/karthikeyan-s">
  <img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white&labelColor=0a0a0f" alt="LinkedIn"/>
</a>
<a href="mailto:karthikeyan123401@gmail.com">
  <img src="https://img.shields.io/badge/Gmail-EA4335?style=for-the-badge&logo=gmail&logoColor=white&labelColor=0a0a0f" alt="Gmail"/>
</a>
<a href="https://github.com/skarthi369">
  <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white&labelColor=0a0a0f" alt="GitHub"/>
</a>

<br/><br/>

<!-- TERMINAL-STYLE FOOTER -->
```
╔══════════════════════════════════════════════════════════════════════════╗
║                                                                          ║
║   >_ System Status: All Neural Modules Operational                       ║
║   >_ Last Update: 2026-07-15                                             ║
║   >_ Location: Chennai, India                                            ║
║   >_ Availability: OPEN FOR OPPORTUNITIES                                ║
║                                                                          ║
║   "Building the future of AI, one neural network at a time."             ║
║                                                                          ║
║   ┌─────────────────────────────────────────────────────────────────┐     ║
║   │  Open to: Python Developer · AI-ML Engineer · LLM Security    │     ║
║   │  Let's talk about: LLM Security · GenAI Agents · Computer Vision│   ║
║   └─────────────────────────────────────────────────────────────────┘     ║
║                                                                          ║
║   [ Initialize Contact Sequence... ]                                      ║
║                                                                          ║
╚══════════════════════════════════════════════════════════════════════════╝
```

<br/>

<!-- NEURAL WAVE ANIMATION -->
<img src="https://capsule-render.vercel.app/api?type=waving&height=120&text=NEURAL%20CORE%20DISCONNECTING...&fontAlign=50&fontAlignY=40&color=0:00f5ff,50:7c3aed,100:f472b6&fontColor=e2e8f0&animation=twinkling&fontSize=16&desc=Thanks%20for%20visiting%20my%20digital%20cortex&descAlign=50&descAlignY=65&descSize=12" width="100%"/>

<!-- SNAKE ANIMATION -->
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/skarthi369/skarthi369/output/github-contribution-grid-snake-dark.svg"/>
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/skarthi369/skarthi369/output/github-contribution-grid-snake.svg"/>
  <img alt="GitHub Contribution Snake" src="https://raw.githubusercontent.com/skarthi369/skarthi369/output/github-contribution-grid-snake-dark.svg"/>
</picture>

</div>

---

<!-- ╔══════════════════════════════════════════════════════════════╗
     ║  F O O T E R                                                  ║
     ╚══════════════════════════════════════════════════════════════╝ -->

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=skarthi369&color=00f5ff&style=flat-square&label=NEURAL+VISITS" alt="Profile Views"/>
</p>

<p align="center">
  <sub><samp>
    <span style="color:#00f5ff">◆</span> Built with neural pathways <span style="color:#f472b6">♥</span> by <b>Karthikeyan S</b> <span style="color:#7c3aed">◆</span>
  </samp></sub>
</p>
