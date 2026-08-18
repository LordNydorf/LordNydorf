```aura width=860 height=300
<div style={{
  width: '100%', height: '100%', background: '#040409',
  display: 'flex', alignItems: 'center', fontFamily: 'Inter, sans-serif',
  position: 'relative', overflow: 'hidden', borderRadius: 20,
  border: '1px solid rgba(168, 85, 247, 0.35)',
  boxSizing: 'border-box'
}}>

  <style>{`
    @keyframes nebula-a {
      0%, 100% { transform: translate(0px, 0px) scale(1); opacity: 0.85; }
      50% { transform: translate(240px, -25px) scale(1.15); opacity: 1.1; }
    }
    @keyframes nebula-b {
      0%, 100% { transform: translate(0px, 0px) scale(1); opacity: 0.75; }
      50% { transform: translate(-200px, 30px) scale(0.9); opacity: 1.0; }
    }
    @keyframes nebula-c {
      0%, 100% { transform: translate(0px, 0px) scale(1); opacity: 0.65; }
      50% { transform: translate(140px, 20px) scale(1.2); opacity: 0.95; }
    }
    @keyframes nebula-d {
      0%, 100% { transform: translate(0px, 0px); opacity: 0.7; }
      50% { transform: translate(-160px, -20px); opacity: 0.45; }
    }
    @keyframes orbit-spin {
      0% { transform: rotate(0deg); }
      100% { transform: rotate(360deg); }
    }
    @keyframes orbit-spin-rev {
      0% { transform: rotate(360deg); }
      100% { transform: rotate(0deg); }
    }
    @keyframes hud-pulse {
      0%, 100% { opacity: 0.15; transform: scale(1); }
      50% { opacity: 0.45; transform: scale(1.06); }
    }
    @keyframes beam-glow {
      0%, 100% { opacity: 0.3; }
      50% { opacity: 0.85; }
    }
    @keyframes live-status {
      0%, 100% { transform: scale(1); opacity: 1; }
      50% { transform: scale(1.35); opacity: 0.4; }
    }
    #neb-1 { animation: nebula-a 11s ease-in-out infinite; }
    #neb-2 { animation: nebula-b 14s ease-in-out infinite; }
    #neb-3 { animation: nebula-c 9s ease-in-out infinite; }
    #neb-4 { animation: nebula-d 13s ease-in-out infinite reverse; }
    #orbit-group-1 { transform-origin: 730px 145px; animation: orbit-spin 20s linear infinite; }
    #orbit-group-2 { transform-origin: 730px 145px; animation: orbit-spin-rev 30s linear infinite; }
    #hud-ring-1 { animation: hud-pulse 6s ease-in-out infinite; }
    #laser-beam { animation: beam-glow 4s ease-in-out infinite; }
    #live-beacon { animation: live-status 2s ease-in-out infinite; }
  `}</style>

  <svg width="860" height="300" style={{ position: 'absolute', top: 0, left: 0 }}>
    <defs>
      {/* High-Impact Plasma Gradients */}
      <radialGradient id="plasma-violet" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(168, 85, 247, 0.85)" />
        <stop offset="40%" stopColor="rgba(126, 34, 206, 0.4)" />
        <stop offset="70%" stopColor="rgba(126, 34, 206, 0)" />
      </radialGradient>
      <radialGradient id="plasma-cyan" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(6, 214, 255, 0.75)" />
        <stop offset="45%" stopColor="rgba(14, 116, 144, 0.3)" />
        <stop offset="70%" stopColor="rgba(14, 116, 144, 0)" />
      </radialGradient>
      <radialGradient id="plasma-pink" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(244, 63, 94, 0.7)" />
        <stop offset="50%" stopColor="rgba(190, 18, 60, 0.22)" />
        <stop offset="75%" stopColor="rgba(190, 18, 60, 0)" />
      </radialGradient>
      <radialGradient id="plasma-emerald" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(16, 185, 129, 0.6)" />
        <stop offset="55%" stopColor="rgba(5, 150, 105, 0.18)" />
        <stop offset="75%" stopColor="rgba(5, 150, 105, 0)" />
      </radialGradient>
      <radialGradient id="plasma-indigo" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(79, 70, 229, 0.7)" />
        <stop offset="50%" stopColor="rgba(67, 56, 202, 0.25)" />
        <stop offset="70%" stopColor="rgba(67, 56, 202, 0)" />
      </radialGradient>

      {/* Cyber Grid Pattern */}
      <pattern id="cyber-grid" width="30" height="30" patternUnits="userSpaceOnUse">
        <path d="M 30 0 L 0 0 0 30" fill="none" stroke="rgba(255, 255, 255, 0.035)" strokeWidth="0.8" />
        <circle cx="0" cy="0" r="0.8" fill="rgba(168, 85, 247, 0.3)" />
      </pattern>

      <linearGradient id="beam-gradient" x1="0%" y1="0%" x2="100%" y2="0%">
        <stop offset="0%" stopColor="rgba(168, 85, 247, 0)" />
        <stop offset="30%" stopColor="rgba(168, 85, 247, 0.8)" />
        <stop offset="50%" stopColor="rgba(6, 214, 255, 1)" />
        <stop offset="70%" stopColor="rgba(244, 63, 94, 0.8)" />
        <stop offset="100%" stopColor="rgba(244, 63, 94, 0)" />
      </linearGradient>
    </defs>

    {/* Background Grid */}
    <rect width="860" height="300" fill="url(#cyber-grid)" />

    {/* Floating Cosmic Plasma Nebulas */}
    <ellipse id="neb-1" cx="160" cy="270" rx="300" ry="210" fill="url(#plasma-violet)" />
    <ellipse id="neb-2" cx="440" cy="280" rx="260" ry="180" fill="url(#plasma-cyan)" />
    <ellipse id="neb-3" cx="740" cy="260" rx="230" ry="170" fill="url(#plasma-pink)" />
    <ellipse id="neb-4" cx="660" cy="40"  rx="220" ry="150" fill="url(#plasma-indigo)" />
    <ellipse cx="280" cy="30"  rx="180" ry="130" fill="url(#plasma-emerald)" />

    {/* Horizontal Laser Accent Beam */}
    <rect id="laser-beam" x="0" y="0" width="860" height="2" fill="url(#beam-gradient)" />
    <rect x="0" y="298" width="860" height="2" fill="url(#beam-gradient)" />

    {/* Orbital Celestial Ring System */}
    <g id="orbit-group-1">
      <circle cx="730" cy="145" r="75" fill="none" stroke="rgba(168, 85, 247, 0.35)" strokeWidth="1" strokeDasharray="6 4" />
      <circle cx="805" cy="145" r="4" fill="#06d6ff" />
      <circle cx="655" cy="145" r="2.5" fill="#f43f5e" />
    </g>
    <g id="orbit-group-2">
      <circle cx="730" cy="145" r="125" fill="none" stroke="rgba(6, 214, 255, 0.25)" strokeWidth="0.8" strokeDasharray="3 6" />
      <circle cx="730" cy="20" r="3.5" fill="#a855f7" />
      <circle cx="730" cy="270" r="2" fill="#10b981" />
    </g>
    <circle id="hud-ring-1" cx="730" cy="145" r="100" fill="none" stroke="rgba(255, 255, 255, 0.12)" strokeWidth="1" />

    {/* Corner Telemetry Brackets */}
    <path d="M 16 36 L 16 16 L 36 16" fill="none" stroke="rgba(168, 85, 247, 0.6)" strokeWidth="1.5" />
    <path d="M 844 36 L 844 16 L 824 16" fill="none" stroke="rgba(6, 214, 255, 0.6)" strokeWidth="1.5" />
    <path d="M 16 264 L 16 284 L 36 284" fill="none" stroke="rgba(6, 214, 255, 0.6)" strokeWidth="1.5" />
    <path d="M 844 264 L 844 284 L 824 284" fill="none" stroke="rgba(168, 85, 247, 0.6)" strokeWidth="1.5" />
  </svg>

  {/* Left: Avatar Pod with Holographic Glow */}
  <div style={{
    position: 'absolute', left: 44, top: 48, width: 114, height: 114,
    borderRadius: 57, background: 'linear-gradient(135deg, #a855f7, #06d6ff, #f43f5e)',
    display: 'flex', alignItems: 'center', justifyContent: 'center',
    padding: 3
  }}>
    <div style={{
      width: '100%', height: '100%', borderRadius: 54, background: '#040409',
      display: 'flex', alignItems: 'center', justifyContent: 'center', padding: 2
    }}>
      <img
        src={(github && github.user && github.user.avatarUrl) || 'https://github.com/LordNydorf.png'}
        width={104}
        height={104}
        style={{ borderRadius: 52 }}
      />
    </div>
  </div>

  {/* Main Profile Identity Column */}
  <div style={{ display: 'flex', flexDirection: 'column', marginLeft: 184, marginRight: 40, gap: 9 }}>
    {/* Telemetry Status Line */}
    <div style={{ display: 'flex', alignItems: 'center', gap: 10 }}>
      <div style={{
        display: 'flex', alignItems: 'center', gap: 6, padding: '4px 12px', borderRadius: 20,
        background: 'rgba(168, 85, 247, 0.18)', border: '1px solid rgba(192, 132, 252, 0.45)',
        color: '#d8b4fe', fontSize: 11, fontWeight: 800, letterSpacing: '1.5px'
      }}>
        <div id="live-beacon" style={{ width: 7, height: 7, borderRadius: 4, background: '#10b981', display: 'flex' }} />
        FULL-STACK & AI ARCHITECT
      </div>
      <div style={{ display: 'flex', fontSize: 12, color: 'rgba(216, 180, 254, 0.7)', fontWeight: 600, letterSpacing: '0.5px' }}>
        // SYS.LOC: KOCHI, IN
      </div>
    </div>

    {/* Display Name */}
    <div style={{ display: 'flex', fontSize: 38, fontWeight: 900, color: '#ffffff', letterSpacing: '-1px', lineHeight: 1.05 }}>
      {(github && github.user && (github.user.name || github.user.login)) || 'Rohit Krishnan'}
    </div>

    {/* Bio Statement */}
    <div style={{ display: 'flex', fontSize: 14, color: 'rgba(235, 225, 255, 0.92)', fontWeight: 400, letterSpacing: '0.2px', lineHeight: 1.45 }}>
      Building intelligent mobile ecosystems, high-performance web platforms and next-gen AI integrations.
    </div>

    {/* Glowing Tech Pills */}
    <div style={{ display: 'flex', gap: 8, marginTop: 4, flexWrap: 'wrap' }}>
      {[
        { name: 'Flutter & Dart', color: '#38bdf8' },
        { name: 'React & Next.js', color: '#a78bfa' },
        { name: 'FastAPI & Python', color: '#34d399' },
        { name: 'Google Gemini AI', color: '#f472b6' },
        { name: 'System Architecture', color: '#fbbf24' }
      ].map(function(t, i) {
        return (
          <div key={t.name + '-' + i} style={{
            display: 'flex', alignItems: 'center', gap: 5, padding: '4px 12px', borderRadius: 20,
            background: 'rgba(255, 255, 255, 0.04)', border: '1px solid ' + t.color + '44',
            color: 'rgba(250, 245, 255, 0.95)', fontSize: 11, fontWeight: 700,
          }}>
            <div style={{ width: 5, height: 5, borderRadius: 3, background: t.color, display: 'flex' }} />
            {t.name}
          </div>
        );
      })}
    </div>
  </div>
</div>
```

```aura width=860 height=140
(function() {
  var repos = String((github && github.stats && github.stats.totalRepos) || 25);
  var commits = String((github && github.stats && github.stats.totalCommits) || '1,500+');

  var stats = [
    { label: 'Repositories', value: repos, color: '#a855f7', sub: 'Public & Private', glow: 'rgba(168, 85, 247, 0.4)' },
    { label: 'Contributions', value: commits, color: '#10b981', sub: 'Commits & Reviews', glow: 'rgba(16, 185, 129, 0.4)' },
    { label: 'Core Stack', value: 'Flutter · React · FastAPI', color: '#06d6ff', sub: 'Cross-Platform & APIs', glow: 'rgba(6, 214, 255, 0.4)' },
    { label: 'Domain Focus', value: 'AI Agents & Products', color: '#f43f5e', sub: 'LLMs & Modern UX', glow: 'rgba(244, 63, 94, 0.4)' },
  ];

  return (
    <div style={{
      width: '100%', height: '100%',
      background: '#040409',
      display: 'flex', alignItems: 'center', justifyContent: 'center',
      fontFamily: 'Inter, sans-serif', borderRadius: 18,
      border: '1px solid rgba(168, 85, 247, 0.3)',
      position: 'relative', overflow: 'hidden',
      padding: '0 8px'
    }}>

      <style>{`
        @keyframes stat-sweep-1 { 0%, 100% { transform: translateX(0px); opacity: 0.6; } 50% { transform: translateX(200px); opacity: 0.95; } }
        @keyframes stat-sweep-2 { 0%, 100% { transform: translateX(0px); opacity: 0.5; } 50% { transform: translateX(-180px); opacity: 0.85; } }
        #st-neb-1 { animation: stat-sweep-1 10s ease-in-out infinite; }
        #st-neb-2 { animation: stat-sweep-2 12s ease-in-out infinite; }
      `}</style>

      <svg width="860" height="140" style={{ position: 'absolute', top: 0, left: 0 }}>
        <defs>
          <radialGradient id="stg-1" cx="50%" cy="50%" r="50%">
            <stop offset="0%" stopColor="rgba(168, 85, 247, 0.5)" />
            <stop offset="50%" stopColor="rgba(126, 34, 206, 0.18)" />
            <stop offset="70%" stopColor="rgba(126, 34, 206, 0)" />
          </radialGradient>
          <radialGradient id="stg-2" cx="50%" cy="50%" r="50%">
            <stop offset="0%" stopColor="rgba(6, 214, 255, 0.45)" />
            <stop offset="50%" stopColor="rgba(14, 116, 144, 0.15)" />
            <stop offset="70%" stopColor="rgba(14, 116, 144, 0)" />
          </radialGradient>
        </defs>
        <ellipse id="st-neb-1" cx="200" cy="140" rx="240" ry="130" fill="url(#stg-1)" />
        <ellipse id="st-neb-2" cx="660" cy="140" rx="260" ry="140" fill="url(#stg-2)" />
      </svg>

      {stats.map(function(s, i) {
        return (
          <div key={s.label} style={{
            flex: i >= 2 ? 1.45 : 1, display: 'flex', flexDirection: 'column',
            alignItems: 'center', justifyContent: 'center',
            padding: '14px 10px',
            borderRight: i < stats.length - 1 ? '1px solid rgba(255, 255, 255, 0.08)' : 'none',
            gap: 5
          }}>
            <div style={{
              display: 'flex', fontSize: i >= 2 ? 18 : 28, fontWeight: 900,
              color: s.color, lineHeight: 1.1, textAlign: 'center',
              letterSpacing: i >= 2 ? '-0.3px' : '-0.8px'
            }}>
              {s.value}
            </div>
            <div style={{ display: 'flex', fontSize: 10, color: 'rgba(230, 220, 255, 0.55)', fontWeight: 800, letterSpacing: '1.5px', textTransform: 'uppercase' }}>
              {s.label}
            </div>
            <div style={{ display: 'flex', fontSize: 10, color: 'rgba(255, 255, 255, 0.4)', fontWeight: 500 }}>
              {s.sub}
            </div>
          </div>
        );
      })}
    </div>
  );
})()
```

```aura width=860 height=240
(function() {
  var projects = [
    {
      num: '// 01',
      title: 'Pennora',
      tag: 'FINTECH APP',
      color: '#a855f7',
      desc: 'Smart spare-change micro-investing platform democratizing wealth building through automated portfolio balancing.',
      tech: 'Flutter · Firebase · Provider',
    },
    {
      num: '// 02',
      title: 'Smart Trip Planner',
      tag: 'AI TRAVEL',
      color: '#06d6ff',
      desc: 'Intelligent trip planning engine that generates tailored personalized travel itineraries using Google Gemini AI.',
      tech: 'Flutter · Gemini AI · Dart',
    },
    {
      num: '// 03',
      title: 'PrepGenius',
      tag: 'EDTECH PLATFORM',
      color: '#10b981',
      desc: 'Full-featured learning web application with solved previous year papers, curated video playlists & interactive quizzes.',
      tech: 'React.js · JavaScript · Modern UI',
    },
  ];

  return (
    <div style={{
      width: '100%', height: '100%',
      background: '#040409',
      display: 'flex', flexDirection: 'column',
      fontFamily: 'Inter, sans-serif', padding: '20px 24px',
      borderRadius: 18, border: '1px solid rgba(168, 85, 247, 0.3)',
      position: 'relative', overflow: 'hidden', gap: 14
    }}>

      <style>{`
        @keyframes pr-plasma { 0%, 100% { transform: translateY(0px) scale(1); opacity: 0.5; } 50% { transform: translateY(-25px) scale(1.1); opacity: 0.85; } }
        #proj-plasma { animation: pr-plasma 8s ease-in-out infinite; }
      `}</style>

      <svg width="860" height="240" style={{ position: 'absolute', top: 0, left: 0 }}>
        <defs>
          <radialGradient id="ppg-1" cx="50%" cy="50%" r="50%">
            <stop offset="0%" stopColor="rgba(168, 85, 247, 0.45)" />
            <stop offset="60%" stopColor="rgba(126, 34, 206, 0.12)" />
            <stop offset="75%" stopColor="rgba(126, 34, 206, 0)" />
          </radialGradient>
        </defs>
        <ellipse id="proj-plasma" cx="430" cy="230" rx="400" ry="180" fill="url(#ppg-1)" />
      </svg>

      <div style={{ display: 'flex', alignItems: 'center', justifyContent: 'space-between' }}>
        <div style={{ display: 'flex', alignItems: 'center', gap: 8 }}>
          <div style={{ width: 8, height: 8, borderRadius: 2, background: '#a855f7', display: 'flex' }} />
          <div style={{ display: 'flex', fontSize: 11, fontWeight: 800, color: '#d8b4fe', letterSpacing: '2.5px' }}>
            FEATURED ARCHITECTURE & PRODUCTS
          </div>
        </div>
        <div style={{ display: 'flex', fontSize: 11, color: 'rgba(255, 255, 255, 0.4)', fontWeight: 600, letterSpacing: '1px' }}>
          01 — 03
        </div>
      </div>

      <div style={{ display: 'flex', gap: 14, flex: 1 }}>
        {projects.map(function(p) {
          return (
            <div key={p.title} style={{
              flex: 1, display: 'flex', flexDirection: 'column',
              background: 'rgba(255, 255, 255, 0.035)',
              borderRadius: 14, padding: '16px 16px',
              border: '1px solid rgba(255, 255, 255, 0.09)',
              borderTop: '2px solid ' + p.color,
              justifyContent: 'space-between'
            }}>
              <div style={{ display: 'flex', flexDirection: 'column', gap: 6 }}>
                <div style={{ display: 'flex', alignItems: 'center', justifyContent: 'space-between' }}>
                  <div style={{
                    display: 'flex', padding: '2px 8px', borderRadius: 6,
                    background: p.color + '18', border: '1px solid ' + p.color + '44',
                    color: p.color, fontSize: 9, fontWeight: 800, letterSpacing: '1px'
                  }}>
                    {p.tag}
                  </div>
                  <div style={{ display: 'flex', fontSize: 10, color: 'rgba(255, 255, 255, 0.35)', fontWeight: 700 }}>
                    {p.num}
                  </div>
                </div>
                <div style={{ display: 'flex', fontSize: 16, fontWeight: 800, color: '#ffffff', letterSpacing: '-0.3px', marginTop: 2 }}>
                  {p.title}
                </div>
                <div style={{ display: 'flex', fontSize: 12, color: 'rgba(225, 220, 250, 0.82)', lineHeight: 1.4 }}>
                  {p.desc}
                </div>
              </div>
              <div style={{
                display: 'flex', fontSize: 11, fontWeight: 700,
                color: 'rgba(255, 255, 255, 0.6)', marginTop: 8,
                paddingTop: 8, borderTop: '1px solid rgba(255, 255, 255, 0.07)'
              }}>
                {p.tech}
              </div>
            </div>
          );
        })}
      </div>
    </div>
  );
})()
```

```aura width=860 height=200
(function() {
  var categories = [
    {
      title: 'Mobile & Frontend',
      color: '#a855f7',
      items: ['Flutter', 'Dart', 'React.js', 'Next.js', 'TypeScript', 'Tailwind CSS']
    },
    {
      title: 'Backend & AI',
      color: '#06d6ff',
      items: ['FastAPI', 'Python', 'Google Gemini AI', 'Firebase', 'Node.js', 'REST APIs']
    },
    {
      title: 'Systems & DevOps',
      color: '#10b981',
      items: ['System Architecture', 'YOLO / CV', 'Git & GitHub', 'Docker', 'State Management']
    },
  ];

  return (
    <div style={{
      width: '100%', height: '100%',
      background: '#040409',
      display: 'flex', flexDirection: 'column',
      fontFamily: 'Inter, sans-serif', padding: '18px 28px', gap: 14,
      borderRadius: 18, border: '1px solid rgba(168, 85, 247, 0.3)',
      position: 'relative', overflow: 'hidden',
    }}>

      <style>{`
        @keyframes tech-plasma { 0%, 100% { opacity: 0.35; } 50% { opacity: 0.8; } }
        #tg-plasma { animation: tech-plasma 7s ease-in-out infinite; }
      `}</style>

      <svg width="860" height="200" style={{ position: 'absolute', top: 0, left: 0 }}>
        <defs>
          <radialGradient id="t-pl" cx="50%" cy="50%" r="50%">
            <stop offset="0%" stopColor="rgba(6, 214, 255, 0.45)" />
            <stop offset="50%" stopColor="rgba(14, 116, 144, 0.15)" />
            <stop offset="70%" stopColor="rgba(14, 116, 144, 0)" />
          </radialGradient>
        </defs>
        <ellipse id="tg-plasma" cx="720" cy="180" rx="240" ry="150" fill="url(#t-pl)" />
      </svg>

      <div style={{ display: 'flex', alignItems: 'center', gap: 8 }}>
        <div style={{ width: 8, height: 8, borderRadius: 2, background: '#06d6ff', display: 'flex' }} />
        <div style={{ display: 'flex', fontSize: 11, fontWeight: 800, color: '#67e8f9', letterSpacing: '2.5px' }}>
          NEURAL TECH STACK & CAPABILITIES
        </div>
      </div>

      <div style={{ display: 'flex', flexDirection: 'column', gap: 10 }}>
        {categories.map(function(cat) {
          return (
            <div key={cat.title} style={{ display: 'flex', alignItems: 'center', gap: 14 }}>
              <div style={{ display: 'flex', fontSize: 11, fontWeight: 800, color: cat.color, letterSpacing: '0.8px', width: 145 }}>
                {cat.title}
              </div>
              <div style={{ display: 'flex', flexWrap: 'wrap', gap: 7, flex: 1 }}>
                {cat.items.map(function(item) {
                  return (
                    <div key={item} style={{
                      display: 'flex', padding: '4px 12px', borderRadius: 8,
                      background: cat.color + '15', border: '1px solid ' + cat.color + '38',
                      color: 'rgba(250, 245, 255, 0.95)', fontSize: 12, fontWeight: 700,
                    }}>{item}</div>
                  );
                })}
              </div>
            </div>
          );
        })}
      </div>
    </div>
  );
})()
```

```aura width=130 height=44 link="https://lordnydorf.github.io/Portfolio/" inline align=center
<SocialMediaButton
  icon="https://cdn.simpleicons.org/safari/ffffff"
  text="Portfolio"
  backgroundColor="#0f0c24"
  width={130}
  height={44}
  gradientStops={[
    { offset: '0%', color: '#06d6ff' },
    { offset: '25%', color: '#a855f7' },
    { offset: '50%', color: '#f43f5e' },
    { offset: '75%', color: '#a855f7' },
    { offset: '100%', color: '#06d6ff' },
  ]}
/>
```

```aura width=120 height=44 link="https://github.com/LordNydorf" inline align=center
<SocialMediaButton
  icon="https://cdn.simpleicons.org/github/ffffff"
  text="GitHub"
  backgroundColor="#090912"
  width={120}
  height={44}
  gradientStops={[
    { offset: '0%', color: '#ffffff' },
    { offset: '20%', color: '#1a1a2e' },
    { offset: '50%', color: '#a855f7' },
    { offset: '80%', color: '#1a1a2e' },
    { offset: '100%', color: '#ffffff' },
  ]}
/>
```

```aura width=120 height=44 link="https://x.com/r_hxt_" inline align=center
<SocialMediaButton
  icon="https://cdn.simpleicons.org/x/ffffff"
  text="X.com"
  backgroundColor="#090912"
  width={120}
  height={44}
  gradientStops={[
    { offset: '0%', color: '#06d6ff' },
    { offset: '30%', color: '#111122' },
    { offset: '50%', color: '#ffffff' },
    { offset: '70%', color: '#111122' },
    { offset: '100%', color: '#06d6ff' },
  ]}
/>
```

```aura width=110 height=44 link="mailto:rohitkrishnanofficial@gmail.com" inline align=center
<SocialMediaButton
  icon="https://cdn.simpleicons.org/gmail/EA4335"
  text="Email"
  backgroundColor="#180a0a"
  width={110}
  height={44}
  gradientStops={[
    { offset: '0%', color: '#f43f5e' },
    { offset: '25%', color: '#2b0a0a' },
    { offset: '50%', color: '#ffffff' },
    { offset: '75%', color: '#2b0a0a' },
    { offset: '100%', color: '#f43f5e' },
  ]}
/>
```

```aura width=860 height=24 link="https://collectioneur.github.io/readme-aura/"
<div style={{ display: 'flex', justifyContent: 'center', alignItems: 'center', width: '100%', height: '100%', padding: 0, margin: 0 }}>
  <span style={{ fontSize: 12, lineHeight: 1, color: 'rgba(192, 132, 252, 0.65)', fontWeight: 600, letterSpacing: '0.6px' }}>⚡ POWERED BY README-AURA · SATORI</span>
</div>
```
