<!DOCTYPE html>
<html lang="en" class="dark">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Sumanth — Full-Stack MERN Developer</title>
  
  <!-- Fonts & Icons -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Fira+Code:wght@400;500;700&family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@tabler/icons-webfont@latest/tabler-icons.min.css" />
  
  <!-- Tailwind CSS CDN -->
  <script src="https://cdn.tailwindcss.com"></script>
  
  <!-- Tailwind Configuration -->
  <script>
    tailwind.config = {
      darkMode: 'class',
      theme: {
        extend: {
          fontFamily: {
            sans: ['Inter', 'sans-serif'],
            mono: ['Fira Code', 'monospace'],
          },
          animation: {
            'blob': 'blob 10s infinite',
            'fade-up': 'fadeUp 0.8s ease-out forwards',
            'glow': 'glow 2s ease-in-out infinite alternate',
            'shimmer': 'shimmer 2.5s linear infinite',
            'ping-slow': 'ping 3s cubic-bezier(0, 0, 0.2, 1) infinite',
          },
          keyframes: {
            blob: {
              '0%': { transform: 'translate(0px, 0px) scale(1)' },
              '33%': { transform: 'translate(40px, -60px) scale(1.1)' },
              '66%': { transform: 'translate(-30px, 30px) scale(0.9)' },
              '100%': { transform: 'translate(0px, 0px) scale(1)' },
            },
            fadeUp: {
              '0%': { opacity: '0', transform: 'translateY(20px)' },
              '100%': { opacity: '1', transform: 'translateY(0)' },
            },
            glow: {
              '0%': { boxShadow: '0 0 10px rgba(45, 212, 191, 0.2)' },
              '100%': { boxShadow: '0 0 20px rgba(45, 212, 191, 0.6), 0 0 40px rgba(45, 212, 191, 0.2)' }
            },
            shimmer: {
              '0%': { transform: 'translateX(-100%)' },
              '100%': { transform: 'translateX(100%)' }
            }
          }
        }
      }
    }
  </script>
  
  <style type="text/tailwindcss">
    @layer utilities {
      .glass-card {
        @apply bg-slate-900/60 backdrop-blur-xl border border-white/5 shadow-xl relative overflow-hidden;
      }
      .hover-glass-card {
        @apply transition-all duration-300 hover:bg-slate-800/80 hover:border-teal-500/30 hover:shadow-[0_0_30px_-5px_rgba(45,212,191,0.15)] hover:-translate-y-1;
      }
      .section-heading {
        @apply text-xs font-semibold text-slate-400 uppercase tracking-[0.2em] mb-6 flex items-center gap-4;
      }
      .section-heading::after {
        content: '';
        @apply flex-1 h-px bg-gradient-to-r from-slate-800 to-transparent;
      }
      .animation-delay-2000 {
        animation-delay: 2s;
      }
      .animation-delay-4000 {
        animation-delay: 4s;
      }
    }
  </style>
</head>
<body class="bg-[#0a0f1c] text-slate-200 font-sans antialiased selection:bg-teal-500/30 selection:text-teal-200 min-h-screen relative overflow-x-hidden">

  <!-- Background Animated Blobs -->
  <div class="fixed inset-0 overflow-hidden pointer-events-none z-0">
    <div class="absolute top-[-10%] left-[-10%] w-[500px] h-[500px] bg-teal-600/10 rounded-full mix-blend-screen filter blur-[100px] animate-blob"></div>
    <div class="absolute top-[20%] right-[-10%] w-[400px] h-[400px] bg-cyan-600/10 rounded-full mix-blend-screen filter blur-[100px] animate-blob animation-delay-2000"></div>
    <div class="absolute bottom-[-20%] left-[20%] w-[600px] h-[600px] bg-blue-600/10 rounded-full mix-blend-screen filter blur-[100px] animate-blob animation-delay-4000"></div>
  </div>

  <main class="relative z-10 max-w-[900px] mx-auto px-6 py-16 sm:py-24">
    
    <h2 class="sr-only">Sumanth — Full-Stack MERN Developer GitHub profile</h2>

    <!-- Hero Section -->
    <header class="glass-card rounded-[2rem] p-8 sm:p-10 mb-12 flex flex-col sm:flex-row items-center gap-8 sm:gap-10 animate-fade-up">
      <!-- Glow effect behind hero -->
      <div class="absolute -top-24 -right-24 w-48 h-48 bg-teal-500/20 blur-[60px] rounded-full pointer-events-none"></div>
      
      <div class="relative shrink-0">
        <div class="w-32 h-32 rounded-full bg-gradient-to-br from-teal-400 to-cyan-600 p-[3px] animate-glow">
          <div class="w-full h-full rounded-full bg-[#0a0f1c] flex items-center justify-center border-4 border-slate-900/50 shadow-inner">
            <span class="font-mono text-5xl font-bold text-transparent bg-clip-text bg-gradient-to-br from-teal-400 to-cyan-400">S</span>
          </div>
        </div>
        <div class="absolute bottom-2 right-2 w-6 h-6 bg-[#0a0f1c] rounded-full flex items-center justify-center" title="Available for opportunities">
          <div class="w-4 h-4 bg-emerald-500 rounded-full relative">
            <span class="absolute inset-0 rounded-full bg-emerald-500 animate-ping-slow opacity-75"></span>
          </div>
        </div>
      </div>
      
      <div class="text-center sm:text-left relative z-10">
        <h1 class="text-4xl sm:text-5xl font-bold text-white mb-3 tracking-tight">Sumanth</h1>
        <p class="font-mono text-sm sm:text-base text-slate-400 mb-8">
          &lt;<span class="text-teal-400 font-medium">Full-Stack</span> MERN Developer /&gt;
        </p>
        
        <div class="flex flex-wrap items-center justify-center sm:justify-start gap-3 sm:gap-4">
          <a href="https://portfolio-sumanth-wiee.onrender.com/" target="_blank" class="flex items-center gap-2 px-5 py-2.5 rounded-full text-sm font-medium bg-slate-800/50 border border-slate-700 text-slate-300 hover:text-white hover:border-teal-500/50 hover:bg-teal-500/10 transition-all duration-300 group">
            <i class="ti ti-world text-teal-400 text-lg group-hover:scale-110 transition-transform"></i> Portfolio
          </a>
          <a href="https://github.com/sumanth965" target="_blank" class="flex items-center gap-2 px-5 py-2.5 rounded-full text-sm font-medium bg-slate-800/50 border border-slate-700 text-slate-300 hover:text-white hover:border-teal-500/50 hover:bg-teal-500/10 transition-all duration-300 group">
            <i class="ti ti-brand-github text-teal-400 text-lg group-hover:scale-110 transition-transform"></i> GitHub
          </a>
          <a href="https://leetcode.com/sumanth965" target="_blank" class="flex items-center gap-2 px-5 py-2.5 rounded-full text-sm font-medium bg-slate-800/50 border border-slate-700 text-slate-300 hover:text-white hover:border-teal-500/50 hover:bg-teal-500/10 transition-all duration-300 group">
            <i class="ti ti-code text-teal-400 text-lg group-hover:scale-110 transition-transform"></i> LeetCode
          </a>
        </div>
      </div>
    </header>

    <!-- About Section -->
    <section class="glass-card rounded-3xl p-8 sm:p-10 mb-12 animate-fade-up [animation-delay:100ms]">
      <h3 class="section-heading">About</h3>
      <div class="space-y-5 text-slate-300 leading-relaxed sm:text-lg font-light">
        <p>I build full-stack applications with the <span class="text-teal-400 font-medium">MERN stack</span>, focusing on clean frontend experiences backed by robust APIs and secure authentication flows.</p>
        <p>Currently leveling up in <span class="text-teal-400 font-medium">scalable backend architecture</span>, <span class="text-teal-400 font-medium">performance optimization</span>, and <span class="text-teal-400 font-medium">cloud deployment</span> (AWS EC2, S3, Lambda, CloudFront).</p>
        <p class="text-white font-medium">Career goal: ship production-ready software that matters.</p>
      </div>
    </section>

    <!-- Stats Section -->
    <section class="mb-14 animate-fade-up [animation-delay:200ms]">
      <h3 class="section-heading">Key Metrics</h3>
      <div class="grid grid-cols-2 sm:grid-cols-4 gap-4 sm:gap-6">
        <div class="glass-card rounded-2xl p-6 sm:p-8 text-center hover-glass-card group cursor-default">
          <div class="font-mono text-4xl sm:text-5xl font-bold text-teal-400 mb-2 group-hover:scale-110 transition-transform duration-300">10<span class="text-2xl text-teal-600">+</span></div>
          <div class="text-xs text-slate-400 font-medium uppercase tracking-widest">Projects shipped</div>
        </div>
        <div class="glass-card rounded-2xl p-6 sm:p-8 text-center hover-glass-card group cursor-default">
          <div class="font-mono text-4xl sm:text-5xl font-bold text-cyan-400 mb-2 group-hover:scale-110 transition-transform duration-300">5<span class="text-2xl text-cyan-600">+</span></div>
          <div class="text-xs text-slate-400 font-medium uppercase tracking-widest">Tech stacks</div>
        </div>
        <div class="glass-card rounded-2xl p-6 sm:p-8 text-center hover-glass-card group cursor-default">
          <div class="font-mono text-4xl sm:text-5xl font-bold text-blue-400 mb-2 group-hover:scale-110 transition-transform duration-300">DSA</div>
          <div class="text-xs text-slate-400 font-medium uppercase tracking-widest">Daily practice</div>
        </div>
        <div class="glass-card rounded-2xl p-6 sm:p-8 text-center hover-glass-card group cursor-default">
          <div class="font-mono text-4xl sm:text-5xl font-bold text-indigo-400 mb-2 group-hover:scale-110 transition-transform duration-300">4<span class="text-2xl text-indigo-600">+</span></div>
          <div class="text-xs text-slate-400 font-medium uppercase tracking-widest">Cloud services</div>
        </div>
      </div>
    </section>

    <!-- Skills Section -->
    <section class="glass-card rounded-3xl p-8 sm:p-10 mb-14 animate-fade-up [animation-delay:300ms]">
      <h3 class="section-heading">Core Skills</h3>
      
      <div class="grid lg:grid-cols-2 gap-10 lg:gap-16">
        <div class="space-y-8">
          <div>
            <div class="text-sm font-medium text-white mb-4 flex items-center gap-2">
              <i class="ti ti-code text-teal-400 text-lg"></i> Languages & Frameworks
            </div>
            <div class="flex flex-wrap gap-2.5">
              <span class="px-3.5 py-1.5 bg-teal-500/10 border border-teal-500/20 text-teal-300 rounded-lg text-sm font-mono shadow-[0_0_15px_-3px_rgba(45,212,191,0.2)] hover:bg-teal-500/20 hover:border-teal-500/40 transition-all cursor-default">JavaScript</span>
              <span class="px-3.5 py-1.5 bg-cyan-500/10 border border-cyan-500/20 text-cyan-300 rounded-lg text-sm font-mono shadow-[0_0_15px_-3px_rgba(34,211,238,0.2)] hover:bg-cyan-500/20 hover:border-cyan-500/40 transition-all cursor-default">TypeScript</span>
              <span class="px-3.5 py-1.5 bg-blue-500/10 border border-blue-500/20 text-blue-300 rounded-lg text-sm font-mono shadow-[0_0_15px_-3px_rgba(59,130,246,0.2)] hover:bg-blue-500/20 hover:border-blue-500/40 transition-all cursor-default">React</span>
              <span class="px-3.5 py-1.5 bg-emerald-500/10 border border-emerald-500/20 text-emerald-300 rounded-lg text-sm font-mono shadow-[0_0_15px_-3px_rgba(16,185,129,0.2)] hover:bg-emerald-500/20 hover:border-emerald-500/40 transition-all cursor-default">Node.js</span>
              <span class="px-3.5 py-1.5 bg-slate-800 border border-slate-700 text-slate-300 rounded-lg text-sm font-mono hover:bg-slate-700 transition-all cursor-default">Express.js</span>
              <span class="px-3.5 py-1.5 bg-slate-800 border border-slate-700 text-slate-300 rounded-lg text-sm font-mono hover:bg-slate-700 transition-all cursor-default">Python</span>
              <span class="px-3.5 py-1.5 bg-slate-800 border border-slate-700 text-slate-300 rounded-lg text-sm font-mono hover:bg-slate-700 transition-all cursor-default">Java</span>
            </div>
          </div>
          <div>
            <div class="text-sm font-medium text-white mb-4 flex items-center gap-2">
              <i class="ti ti-database text-cyan-400 text-lg"></i> Databases & Cloud
            </div>
            <div class="flex flex-wrap gap-2.5">
              <span class="px-3.5 py-1.5 bg-green-500/10 border border-green-500/20 text-green-300 rounded-lg text-sm font-mono shadow-[0_0_15px_-3px_rgba(34,197,94,0.2)] hover:bg-green-500/20 hover:border-green-500/40 transition-all cursor-default">MongoDB</span>
              <span class="px-3.5 py-1.5 bg-orange-500/10 border border-orange-500/20 text-orange-300 rounded-lg text-sm font-mono shadow-[0_0_15px_-3px_rgba(249,115,22,0.2)] hover:bg-orange-500/20 hover:border-orange-500/40 transition-all cursor-default">AWS EC2</span>
              <span class="px-3.5 py-1.5 bg-slate-800 border border-slate-700 text-slate-300 rounded-lg text-sm font-mono hover:bg-slate-700 transition-all cursor-default">S3</span>
              <span class="px-3.5 py-1.5 bg-slate-800 border border-slate-700 text-slate-300 rounded-lg text-sm font-mono hover:bg-slate-700 transition-all cursor-default">Lambda</span>
              <span class="px-3.5 py-1.5 bg-slate-800 border border-slate-700 text-slate-300 rounded-lg text-sm font-mono hover:bg-slate-700 transition-all cursor-default">CloudFront</span>
            </div>
          </div>
          <div>
            <div class="text-sm font-medium text-white mb-4 flex items-center gap-2">
              <i class="ti ti-tools text-purple-400 text-lg"></i> Tooling & Practices
            </div>
            <div class="flex flex-wrap gap-2.5">
              <span class="px-3 py-1.5 bg-slate-800 border border-slate-700 text-slate-300 rounded-lg text-xs font-mono hover:bg-slate-700 transition-all cursor-default">Redux</span>
              <span class="px-3 py-1.5 bg-slate-800 border border-slate-700 text-slate-300 rounded-lg text-xs font-mono hover:bg-slate-700 transition-all cursor-default">Git</span>
              <span class="px-3 py-1.5 bg-slate-800 border border-slate-700 text-slate-300 rounded-lg text-xs font-mono hover:bg-slate-700 transition-all cursor-default">JWT Auth</span>
              <span class="px-3 py-1.5 bg-slate-800 border border-slate-700 text-slate-300 rounded-lg text-xs font-mono hover:bg-slate-700 transition-all cursor-default">REST APIs</span>
              <span class="px-3 py-1.5 bg-slate-800 border border-slate-700 text-slate-300 rounded-lg text-xs font-mono hover:bg-slate-700 transition-all cursor-default">WebSocket</span>
              <span class="px-3 py-1.5 bg-slate-800 border border-slate-700 text-slate-300 rounded-lg text-xs font-mono hover:bg-slate-700 transition-all cursor-default">Render</span>
              <span class="px-3 py-1.5 bg-slate-800 border border-slate-700 text-slate-300 rounded-lg text-xs font-mono hover:bg-slate-700 transition-all cursor-default">Vercel</span>
              <span class="px-3 py-1.5 bg-slate-800 border border-slate-700 text-slate-300 rounded-lg text-xs font-mono hover:bg-slate-700 transition-all cursor-default">Netlify</span>
            </div>
          </div>
        </div>

        <div>
          <div class="text-sm font-medium text-white mb-6 flex items-center gap-2">
            <i class="ti ti-chart-pie text-blue-400 text-lg"></i> Proficiency
          </div>
          <div class="space-y-6">
            <div class="group">
              <div class="flex justify-between text-sm font-mono mb-2">
                <span class="text-slate-400 group-hover:text-teal-400 transition-colors">React / JS</span>
                <span class="text-teal-400 font-bold">90%</span>
              </div>
              <div class="w-full bg-slate-800/80 rounded-full h-2 overflow-hidden border border-slate-700/50">
                <div class="bg-gradient-to-r from-teal-500 to-cyan-400 h-2 rounded-full relative shadow-[0_0_10px_rgba(45,212,191,0.5)]" style="width: 90%">
                  <div class="absolute inset-0 bg-white/30 w-full animate-[shimmer_2s_infinite]"></div>
                </div>
              </div>
            </div>
            <div class="group">
              <div class="flex justify-between text-sm font-mono mb-2">
                <span class="text-slate-400 group-hover:text-cyan-400 transition-colors">Node / API</span>
                <span class="text-cyan-400 font-bold">85%</span>
              </div>
              <div class="w-full bg-slate-800/80 rounded-full h-2 overflow-hidden border border-slate-700/50">
                <div class="bg-gradient-to-r from-cyan-500 to-blue-400 h-2 rounded-full relative shadow-[0_0_10px_rgba(34,211,238,0.5)]" style="width: 85%"></div>
              </div>
            </div>
            <div class="group">
              <div class="flex justify-between text-sm font-mono mb-2">
                <span class="text-slate-400 group-hover:text-green-400 transition-colors">MongoDB</span>
                <span class="text-green-400 font-bold">80%</span>
              </div>
              <div class="w-full bg-slate-800/80 rounded-full h-2 overflow-hidden border border-slate-700/50">
                <div class="bg-gradient-to-r from-green-500 to-emerald-400 h-2 rounded-full relative shadow-[0_0_10px_rgba(16,185,129,0.5)]" style="width: 80%"></div>
              </div>
            </div>
            <div class="group">
              <div class="flex justify-between text-sm font-mono mb-2">
                <span class="text-slate-400 group-hover:text-blue-400 transition-colors">TypeScript</span>
                <span class="text-blue-400 font-bold">75%</span>
              </div>
              <div class="w-full bg-slate-800/80 rounded-full h-2 overflow-hidden border border-slate-700/50">
                <div class="bg-gradient-to-r from-blue-500 to-indigo-400 h-2 rounded-full relative shadow-[0_0_10px_rgba(59,130,246,0.5)]" style="width: 75%"></div>
              </div>
            </div>
            <div class="group">
              <div class="flex justify-between text-sm font-mono mb-2">
                <span class="text-slate-400 group-hover:text-orange-400 transition-colors">AWS</span>
                <span class="text-orange-400 font-bold">65%</span>
              </div>
              <div class="w-full bg-slate-800/80 rounded-full h-2 overflow-hidden border border-slate-700/50">
                <div class="bg-gradient-to-r from-orange-500 to-amber-400 h-2 rounded-full relative shadow-[0_0_10px_rgba(249,115,22,0.5)]" style="width: 65%"></div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Projects Section -->
    <section class="mb-14 animate-fade-up [animation-delay:400ms]">
      <h3 class="section-heading">Featured Projects</h3>
      <div class="grid grid-cols-1 sm:grid-cols-2 gap-6">
        
        <!-- Project 1 -->
        <div class="glass-card hover-glass-card rounded-3xl p-8 flex flex-col h-full group">
          <div class="flex items-center gap-5 mb-5">
            <div class="w-14 h-14 rounded-2xl bg-teal-500/10 flex items-center justify-center text-teal-400 group-hover:bg-teal-500 group-hover:text-white transition-all duration-300 shadow-[0_0_20px_-5px_rgba(45,212,191,0.3)] group-hover:scale-110 group-hover:-rotate-3">
              <i class="ti ti-building-office text-3xl"></i>
            </div>
            <h4 class="text-lg font-bold text-white group-hover:text-teal-300 transition-colors">Employee Leave Management</h4>
          </div>
          <p class="text-slate-400 leading-relaxed mb-8 flex-grow">Enterprise leave tracking with multi-role auth, approval workflows, and dashboard analytics.</p>
          <div class="mt-auto">
            <div class="flex flex-wrap gap-2 mb-6">
              <span class="text-xs font-mono px-2.5 py-1 rounded bg-slate-800/80 border border-slate-700 text-slate-300">MERN</span>
              <span class="text-xs font-mono px-2.5 py-1 rounded bg-slate-800/80 border border-slate-700 text-slate-300">JWT</span>
            </div>
            <div class="flex items-center gap-4 pt-5 border-t border-slate-800/60">
              <a href="https://github.com/sumanth965/Employee-Leave-Management-System" target="_blank" class="text-sm font-medium flex items-center gap-2 text-slate-400 hover:text-teal-400 transition-colors"><i class="ti ti-brand-github text-lg"></i> Code</a>
              <a href="https://elms-management.onrender.com/" target="_blank" class="text-sm font-medium flex items-center gap-2 text-slate-400 hover:text-teal-400 transition-colors"><i class="ti ti-external-link text-lg"></i> Demo</a>
            </div>
          </div>
        </div>

        <!-- Project 2 -->
        <div class="glass-card hover-glass-card rounded-3xl p-8 flex flex-col h-full group">
          <div class="flex items-center gap-5 mb-5">
            <div class="w-14 h-14 rounded-2xl bg-cyan-500/10 flex items-center justify-center text-cyan-400 group-hover:bg-cyan-500 group-hover:text-white transition-all duration-300 shadow-[0_0_20px_-5px_rgba(34,211,238,0.3)] group-hover:scale-110 group-hover:rotate-3">
              <i class="ti ti-target text-3xl"></i>
            </div>
            <h4 class="text-lg font-bold text-white group-hover:text-cyan-300 transition-colors">Smart Student Productivity</h4>
          </div>
          <p class="text-slate-400 leading-relaxed mb-8 flex-grow">Task management, deadline tracking, and schedule optimization for students.</p>
          <div class="mt-auto">
            <div class="flex flex-wrap gap-2 mb-6">
              <span class="text-xs font-mono px-2.5 py-1 rounded bg-slate-800/80 border border-slate-700 text-slate-300">React</span>
              <span class="text-xs font-mono px-2.5 py-1 rounded bg-slate-800/80 border border-slate-700 text-slate-300">Node.js</span>
            </div>
            <div class="flex items-center gap-4 pt-5 border-t border-slate-800/60">
              <a href="https://github.com/sumanth965/smart-student-productivity-system" target="_blank" class="text-sm font-medium flex items-center gap-2 text-slate-400 hover:text-cyan-400 transition-colors"><i class="ti ti-brand-github text-lg"></i> Code</a>
              <a href="https://smart-student-productivity-system.onrender.com/" target="_blank" class="text-sm font-medium flex items-center gap-2 text-slate-400 hover:text-cyan-400 transition-colors"><i class="ti ti-external-link text-lg"></i> Demo</a>
            </div>
          </div>
        </div>

        <!-- Project 3 -->
        <div class="glass-card hover-glass-card rounded-3xl p-8 flex flex-col h-full group">
          <div class="flex items-center gap-5 mb-5">
            <div class="w-14 h-14 rounded-2xl bg-purple-500/10 flex items-center justify-center text-purple-400 group-hover:bg-purple-500 group-hover:text-white transition-all duration-300 shadow-[0_0_20px_-5px_rgba(168,85,247,0.3)] group-hover:scale-110 group-hover:-rotate-3">
              <i class="ti ti-gavel text-3xl"></i>
            </div>
            <h4 class="text-lg font-bold text-white group-hover:text-purple-300 transition-colors">Online Art Auction</h4>
          </div>
          <p class="text-slate-400 leading-relaxed mb-8 flex-grow">Real-time digital art auction platform with WebSocket bidding and curated galleries.</p>
          <div class="mt-auto">
            <div class="flex flex-wrap gap-2 mb-6">
              <span class="text-xs font-mono px-2.5 py-1 rounded bg-slate-800/80 border border-slate-700 text-slate-300">MERN</span>
              <span class="text-xs font-mono px-2.5 py-1 rounded bg-slate-800/80 border border-slate-700 text-slate-300">WebSocket</span>
            </div>
            <div class="flex items-center gap-4 pt-5 border-t border-slate-800/60">
              <a href="https://github.com/sumanth965/Online-Art-Auction" target="_blank" class="text-sm font-medium flex items-center gap-2 text-slate-400 hover:text-purple-400 transition-colors"><i class="ti ti-brand-github text-lg"></i> Code</a>
              <a href="https://online-art-auction.vercel.app/" target="_blank" class="text-sm font-medium flex items-center gap-2 text-slate-400 hover:text-purple-400 transition-colors"><i class="ti ti-external-link text-lg"></i> Demo</a>
            </div>
          </div>
        </div>

        <!-- Project 4 -->
        <div class="glass-card hover-glass-card rounded-3xl p-8 flex flex-col h-full group">
          <div class="flex items-center gap-5 mb-5">
            <div class="w-14 h-14 rounded-2xl bg-blue-500/10 flex items-center justify-center text-blue-400 group-hover:bg-blue-500 group-hover:text-white transition-all duration-300 shadow-[0_0_20px_-5px_rgba(59,130,246,0.3)] group-hover:scale-110 group-hover:rotate-3">
              <i class="ti ti-chart-bar text-3xl"></i>
            </div>
            <h4 class="text-lg font-bold text-white group-hover:text-blue-300 transition-colors">MERN Excel Analytics</h4>
          </div>
          <p class="text-slate-400 leading-relaxed mb-8 flex-grow">Converts Excel datasets into visual charts and report-ready insights.</p>
          <div class="mt-auto">
            <div class="flex flex-wrap gap-2 mb-6">
              <span class="text-xs font-mono px-2.5 py-1 rounded bg-slate-800/80 border border-slate-700 text-slate-300">Chart.js</span>
              <span class="text-xs font-mono px-2.5 py-1 rounded bg-slate-800/80 border border-slate-700 text-slate-300">Express</span>
            </div>
            <div class="flex items-center gap-4 pt-5 border-t border-slate-800/60">
              <a href="https://github.com/sumanth965/MERN-excel-analytics-" target="_blank" class="text-sm font-medium flex items-center gap-2 text-slate-400 hover:text-blue-400 transition-colors"><i class="ti ti-brand-github text-lg"></i> Code</a>
              <a href="https://excel-analytic-sumanth09.onrender.com" target="_blank" class="text-sm font-medium flex items-center gap-2 text-slate-400 hover:text-blue-400 transition-colors"><i class="ti ti-external-link text-lg"></i> Demo</a>
            </div>
          </div>
        </div>

        <!-- Project 5 -->
        <div class="glass-card hover-glass-card rounded-3xl p-8 flex flex-col h-full group">
          <div class="flex items-center gap-5 mb-5">
            <div class="w-14 h-14 rounded-2xl bg-orange-500/10 flex items-center justify-center text-orange-400 group-hover:bg-orange-500 group-hover:text-white transition-all duration-300 shadow-[0_0_20px_-5px_rgba(249,115,22,0.3)] group-hover:scale-110 group-hover:-rotate-3">
              <i class="ti ti-shopping-bag text-3xl"></i>
            </div>
            <h4 class="text-lg font-bold text-white group-hover:text-orange-300 transition-colors">Foodify</h4>
          </div>
          <p class="text-slate-400 leading-relaxed mb-8 flex-grow">Food delivery platform with menu handling, order flow, and admin controls.</p>
          <div class="mt-auto">
            <div class="flex flex-wrap gap-2 mb-6">
              <span class="text-xs font-mono px-2.5 py-1 rounded bg-slate-800/80 border border-slate-700 text-slate-300">Redux</span>
              <span class="text-xs font-mono px-2.5 py-1 rounded bg-slate-800/80 border border-slate-700 text-slate-300">MERN</span>
            </div>
            <div class="flex items-center gap-4 pt-5 border-t border-slate-800/60">
              <a href="https://github.com/sumanth965/Foodify" target="_blank" class="text-sm font-medium flex items-center gap-2 text-slate-400 hover:text-orange-400 transition-colors"><i class="ti ti-brand-github text-lg"></i> Code</a>
              <a href="https://foodify-frontend-4vlo.onrender.com" target="_blank" class="text-sm font-medium flex items-center gap-2 text-slate-400 hover:text-orange-400 transition-colors"><i class="ti ti-external-link text-lg"></i> Demo</a>
            </div>
          </div>
        </div>

        <!-- Project 6 -->
        <div class="glass-card hover-glass-card rounded-3xl p-8 flex flex-col h-full group">
          <div class="flex items-center gap-5 mb-5">
            <div class="w-14 h-14 rounded-2xl bg-emerald-500/10 flex items-center justify-center text-emerald-400 group-hover:bg-emerald-500 group-hover:text-white transition-all duration-300 shadow-[0_0_20px_-5px_rgba(16,185,129,0.3)] group-hover:scale-110 group-hover:rotate-3">
              <i class="ti ti-device-laptop text-3xl"></i>
            </div>
            <h4 class="text-lg font-bold text-white group-hover:text-emerald-300 transition-colors">TST Gadgets</h4>
          </div>
          <p class="text-slate-400 leading-relaxed mb-8 flex-grow">E-commerce gadget storefront + admin panel for inventory and product management.</p>
          <div class="mt-auto">
            <div class="flex flex-wrap gap-2 mb-6">
              <span class="text-xs font-mono px-2.5 py-1 rounded bg-slate-800/80 border border-slate-700 text-slate-300">E-commerce</span>
              <span class="text-xs font-mono px-2.5 py-1 rounded bg-slate-800/80 border border-slate-700 text-slate-300">MERN</span>
            </div>
            <div class="flex items-center gap-4 pt-5 border-t border-slate-800/60">
              <a href="https://github.com/sumanth965/TST_Electronic_Gadgets-" target="_blank" class="text-sm font-medium flex items-center gap-2 text-slate-400 hover:text-emerald-400 transition-colors"><i class="ti ti-brand-github text-lg"></i> Code</a>
              <a href="https://tst-electronic-gadgets-su-manth09.onrender.com" target="_blank" class="text-sm font-medium flex items-center gap-2 text-slate-400 hover:text-emerald-400 transition-colors"><i class="ti ti-external-link text-lg"></i> Demo</a>
            </div>
          </div>
        </div>

      </div>
    </section>

    <!-- Floating Code Section -->
    <section class="glass-card rounded-3xl p-8 sm:p-10 mb-14 font-mono text-sm sm:text-base leading-relaxed overflow-x-auto shadow-2xl border-t-teal-500/30 animate-fade-up [animation-delay:500ms]">
      <div class="flex gap-2 mb-6">
        <div class="w-3 h-3 rounded-full bg-red-500/80"></div>
        <div class="w-3 h-3 rounded-full bg-yellow-500/80"></div>
        <div class="w-3 h-3 rounded-full bg-green-500/80"></div>
      </div>
      <div class="text-slate-500 mb-2 italic">// current focus</div>
      <div class="text-slate-300">
        <span class="text-purple-400">const</span> <span class="text-blue-300">sumanth</span> <span class="text-teal-400">=</span> {<br>
        &nbsp;&nbsp;<span class="text-cyan-200">stack:</span> [<span class="text-orange-300">"React"</span>, <span class="text-orange-300">"Node.js"</span>, <span class="text-orange-300">"MongoDB"</span>, <span class="text-orange-300">"Express"</span>],<br>
        &nbsp;&nbsp;<span class="text-cyan-200">solving:</span> <span class="text-orange-300">"DSA daily on LeetCode"</span>,<br>
        &nbsp;&nbsp;<span class="text-cyan-200">learning:</span> [<span class="text-orange-300">"AWS"</span>, <span class="text-orange-300">"TypeScript"</span>, <span class="text-orange-300">"System Design"</span>],<br>
        &nbsp;&nbsp;<span class="text-cyan-200">goal:</span> <span class="text-orange-300">"High-impact Full Stack Engineer"</span><br>
        };
      </div>
    </section>

    <!-- Connect & Footer Section -->
    <section class="animate-fade-up [animation-delay:600ms]">
      <h3 class="section-heading">Connect</h3>
      <div class="flex flex-wrap gap-4 mb-16">
        <a href="https://github.com/sumanth965" target="_blank" class="flex items-center gap-2.5 px-6 py-3 rounded-2xl text-sm font-medium bg-slate-800/80 border border-slate-700 text-white hover:border-teal-500/50 hover:bg-teal-500/10 hover:-translate-y-1.5 transition-all duration-300 shadow-lg hover:shadow-[0_10px_20px_-10px_rgba(45,212,191,0.4)]">
          <i class="ti ti-brand-github text-teal-400 text-xl"></i> sumanth965
        </a>
        <a href="https://portfolio-sumanth-wiee.onrender.com/" target="_blank" class="flex items-center gap-2.5 px-6 py-3 rounded-2xl text-sm font-medium bg-slate-800/80 border border-slate-700 text-white hover:border-teal-500/50 hover:bg-teal-500/10 hover:-translate-y-1.5 transition-all duration-300 shadow-lg hover:shadow-[0_10px_20px_-10px_rgba(45,212,191,0.4)]">
          <i class="ti ti-world text-teal-400 text-xl"></i> Portfolio
        </a>
        <a href="https://leetcode.com/sumanth965" target="_blank" class="flex items-center gap-2.5 px-6 py-3 rounded-2xl text-sm font-medium bg-slate-800/80 border border-slate-700 text-white hover:border-teal-500/50 hover:bg-teal-500/10 hover:-translate-y-1.5 transition-all duration-300 shadow-lg hover:shadow-[0_10px_20px_-10px_rgba(45,212,191,0.4)]">
          <i class="ti ti-code text-teal-400 text-xl"></i> LeetCode
        </a>
        <a href="https://github.com/sumanth965/leetcode-dsa-solutions" target="_blank" class="flex items-center gap-2.5 px-6 py-3 rounded-2xl text-sm font-medium bg-slate-800/80 border border-slate-700 text-white hover:border-teal-500/50 hover:bg-teal-500/10 hover:-translate-y-1.5 transition-all duration-300 shadow-lg hover:shadow-[0_10px_20px_-10px_rgba(45,212,191,0.4)]">
          <i class="ti ti-git-branch text-teal-400 text-xl"></i> DSA repo
        </a>
      </div>

      <footer class="text-center pt-8 border-t border-slate-800/50 text-slate-500 font-mono text-sm tracking-wide">
        <span class="text-teal-400">⭐ Code. Create. Contribute.</span> — if my work helps you, drop a star.
      </footer>
    </section>

  </main>
</body>
</html>
