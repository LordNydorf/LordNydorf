```aura width=860 height=260
<div style={{
  width: '100%', height: '100%', background: '#080811',
  display: 'flex', alignItems: 'center', fontFamily: 'Inter, sans-serif',
  position: 'relative', overflow: 'hidden', borderRadius: 18,
  border: '1px solid rgba(139, 92, 246, 0.25)',
  boxSizing: 'border-box'
}}>

  <style>{`
    @keyframes aura-float-1 {
      0%, 100% { transform: translate(0px, 0px); opacity: 0.8; }
      50% { transform: translate(260px, -20px); opacity: 1.1; }
    }
    @keyframes aura-float-2 {
      0%, 100% { transform: translate(0px, 0px); opacity: 0.7; }
      50% { transform: translate(-220px, 25px); opacity: 1.0; }
    }
    @keyframes aura-float-3 {
      0%, 100% { transform: translate(0px, 0px); opacity: 0.85; }
      50% { transform: translate(160px, 15px); opacity: 0.55; }
    }
    @keyframes aura-float-4 {
      0%, 100% { transform: translate(0px, 0px); opacity: 0.6; }
      50% { transform: translate(-140px, -25px); opacity: 0.9; }
    }
    @keyframes pulse-ring {
      0%, 100% { opacity: 0.12; transform: scale(1); }
      50% { opacity: 0.35; transform: scale(1.08); }
    }
    @keyframes live-dot {
      0%, 100% { opacity: 1; transform: scale(1); }
      50% { opacity: 0.4; transform: scale(0.85); }
    }
    #bg-aura-1 { animation: aura-float-1 11s ease-in-out infinite; }
    #bg-aura-2 { animation: aura-float-2 14s ease-in-out infinite; }
    #bg-aura-3 { animation: aura-float-3 9s ease-in-out infinite; }
    #bg-aura-4 { animation: aura-float-4 13s ease-in-out infinite reverse; }
    #h-ring-1 { animation: pulse-ring 7s ease-in-out infinite; }
    #h-ring-2 { animation: pulse-ring 7s ease-in-out infinite 2.5s; }
    #status-dot { animation: live-dot 2s ease-in-out infinite; }
  `}</style>

  <svg width="860" height="260" style={{ position: 'absolute', top: 0, left: 0 }}>
    <defs>
      <radialGradient id="ha-g1" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(139, 92, 246, 0.75)" />
        <stop offset="45%" stopColor="rgba(109, 40, 217, 0.35)" />
        <stop offset="70%" stopColor="rgba(109, 40, 217, 0)" />
      </radialGradient>
      <radialGradient id="ha-g2" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(6, 182, 212, 0.65)" />
        <stop offset="50%" stopColor="rgba(14, 116, 144, 0.25)" />
        <stop offset="70%" stopColor="rgba(14, 116, 144, 0)" />
      </radialGradient>
      <radialGradient id="ha-g3" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(236, 72, 153, 0.55)" />
        <stop offset="50%" stopColor="rgba(190, 24, 93, 0.2)" />
        <stop offset="70%" stopColor="rgba(190, 24, 93, 0)" />
      </radialGradient>
      <radialGradient id="ha-g4" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(16, 185, 129, 0.45)" />
        <stop offset="60%" stopColor="rgba(16, 185, 129, 0.12)" />
        <stop offset="75%" stopColor="rgba(16, 185, 129, 0)" />
      </radialGradient>
      <radialGradient id="ha-g5" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(79, 70, 229, 0.6)" />
        <stop offset="55%" stopColor="rgba(67, 56, 202, 0.2)" />
        <stop offset="70%" stopColor="rgba(67, 56, 202, 0)" />
      </radialGradient>
    </defs>

    {/* Dynamic Glowing Auras */}
    <ellipse id="bg-aura-1" cx="150" cy="230" rx="270" ry="190" fill="url(#ha-g1)" />
    <ellipse id="bg-aura-2" cx="420" cy="250" rx="240" ry="170" fill="url(#ha-g2)" />
    <ellipse id="bg-aura-3" cx="720" cy="240" rx="210" ry="150" fill="url(#ha-g3)" />
    <ellipse id="bg-aura-4" cx="640" cy="50"  rx="190" ry="140" fill="url(#ha-g5)" />
    <ellipse cx="280" cy="40"  rx="170" ry="120" fill="url(#ha-g4)" />

    {/* Concentric Modern HUD Rings */}
    <circle id="h-ring-1" cx="740" cy="130" r="70"  fill="none" stroke="rgba(167, 139, 250, 0.4)" strokeWidth="0.8" strokeDasharray="4 4" />
    <circle id="h-ring-2" cx="740" cy="130" r="120" fill="none" stroke="rgba(6, 182, 212, 0.3)" strokeWidth="0.8" />
  </svg>

  {/* Avatar Section */}
  <div style={{
    position: 'absolute', left: 40, top: 44, width: 108, height: 108,
    borderRadius: 54, background: 'linear-gradient(135deg, #8b5cf6, #06b6d4, #ec4899)',
    display: 'flex', alignItems: 'center', justifyContent: 'center',
    padding: 3
  }}>
    <img
      src={(github && github.user && github.user.avatarUrl) || 'https://github.com/LordNydorf.png'}
      width={100}
      height={100}
      style={{ borderRadius: 50 }}
    />
  </div>

  {/* Content Section */}
  <div style={{ display: 'flex', flexDirection: 'column', marginLeft: 176, marginRight: 36, gap: 8 }}>
    <div style={{ display: 'flex', alignItems: 'center', gap: 10 }}>
      <div style={{
        display: 'flex', alignItems: 'center', gap: 6, padding: '4px 12px', borderRadius: 20,
        background: 'rgba(139, 92, 246, 0.2)', border: '1px solid rgba(167, 139, 250, 0.4)',
        color: '#c4b5fd', fontSize: 11, fontWeight: 700, letterSpacing: '1.2px'
      }}>
        <div id="status-dot" style={{ width: 6, height: 6, borderRadius: 3, background: '#34d399', display: 'flex' }} />
        FULL-STACK & AI ENGINEER
      </div>
      <div style={{ display: 'flex', fontSize: 12, color: 'rgba(215, 205, 255, 0.6)', fontWeight: 500 }}>
        📍 Kochi, Kerala, India
      </div>
    </div>

    <div style={{ display: 'flex', fontSize: 36, fontWeight: 800, color: '#ffffff', letterSpacing: '-0.8px', lineHeight: 1.1 }}>
      {(github && github.user && (github.user.name || github.user.login)) || 'Rohit Krishnan'}
    </div>

    <div style={{ display: 'flex', fontSize: 14, color: 'rgba(225, 220, 255, 0.9)', fontWeight: 400, letterSpacing: '0.2px', lineHeight: 1.4 }}>
      Building intelligent mobile applications, scalable web platforms and AI integrations.
    </div>

    <div style={{ display: 'flex', gap: 8, marginTop: 4, flexWrap: 'wrap' }}>
      {['Flutter / Dart', 'React & Next.js', 'FastAPI & Python', 'Google Gemini AI', 'System Design'].map(function(tag, i) {
        return (
          <div key={tag + '-' + i} style={{
            display: 'flex', padding: '4px 12px', borderRadius: 20,
            background: 'rgba(255, 255, 255, 0.05)', border: '1px solid rgba(255, 255, 255, 0.12)',
            color: 'rgba(240, 235, 255, 0.95)', fontSize: 11, fontWeight: 600,
          }}>{tag}</div>
        );
      })}
    </div>
  </div>
</div>
```

```aura width=860 height=130
(function() {
  var repos = String((github && github.stats && github.stats.totalRepos) || 25);
  var commits = String((github && github.stats && github.stats.totalCommits) || '1,500+');

  var stats = [
    { label: 'Repositories', value: repos, color: '#a78bfa', sub: 'Public & Private' },
    { label: 'Contributions', value: commits, color: '#34d399', sub: 'Commits & Reviews' },
    { label: 'Core Ecosystem', value: 'Flutter · React · FastAPI', color: '#38bdf8', sub: 'Mobile, Web & Backend' },
    { label: 'Specialization', value: 'AI Integrations & Products', color: '#f472b6', sub: 'LLMs & Modern UX' },
  ];

  return (
    <div style={{
      width: '100%', height: '100%',
      background: '#080811',
      display: 'flex', alignItems: 'center', justifyContent: 'center',
      fontFamily: 'Inter, sans-serif', borderRadius: 18,
      border: '1px solid rgba(139, 92, 246, 0.22)',
      position: 'relative', overflow: 'hidden',
      padding: '0 8px'
    }}>

      <style>{`
        @keyframes stat-glow-a { 0%, 100% { transform: translateX(0px); opacity: 0.5; } 50% { transform: translateX(180px); opacity: 0.85; } }
        @keyframes stat-glow-b { 0%, 100% { transform: translateX(0px); opacity: 0.45; } 50% { transform: translateX(-160px); opacity: 0.8; } }
        #st-g1 { animation: stat-glow-a 10s ease-in-out infinite; }
        #st-g2 { animation: stat-glow-b 12s ease-in-out infinite; }
      `}</style>

      <svg width="860" height="130" style={{ position: 'absolute', top: 0, left: 0 }}>
        <defs>
          <radialGradient id="sg-1" cx="50%" cy="50%" r="50%">
            <stop offset="0%" stopColor="rgba(139, 92, 246, 0.45)" />
            <stop offset="50%" stopColor="rgba(109, 40, 217, 0.18)" />
            <stop offset="70%" stopColor="rgba(109, 40, 217, 0)" />
          </radialGradient>
          <radialGradient id="sg-2" cx="50%" cy="50%" r="50%">
            <stop offset="0%" stopColor="rgba(6, 182, 212, 0.4)" />
            <stop offset="50%" stopColor="rgba(14, 116, 144, 0.15)" />
            <stop offset="70%" stopColor="rgba(14, 116, 144, 0)" />
          </radialGradient>
        </defs>
        <ellipse id="st-g1" cx="220" cy="130" rx="220" ry="120" fill="url(#sg-1)" />
        <ellipse id="st-g2" cx="640" cy="130" rx="240" ry="130" fill="url(#sg-2)" />
      </svg>

      {stats.map(function(s, i) {
        return (
          <div key={s.label} style={{
            flex: i >= 2 ? 1.4 : 1, display: 'flex', flexDirection: 'column',
            alignItems: 'center', justifyContent: 'center',
            padding: '12px 10px',
            borderRight: i < stats.length - 1 ? '1px solid rgba(255, 255, 255, 0.08)' : 'none',
            gap: 4
          }}>
            <div style={{ display: 'flex', fontSize: i >= 2 ? 18 : 26, fontWeight: 800, color: s.color, lineHeight: 1.1, textAlign: 'center' }}>
              {s.value}
            </div>
            <div style={{ display: 'flex', fontSize: 10, color: 'rgba(215, 210, 240, 0.5)', fontWeight: 700, letterSpacing: '1.2px', textTransform: 'uppercase' }}>
              {s.label}
            </div>
            <div style={{ display: 'flex', fontSize: 10, color: 'rgba(255, 255, 255, 0.35)', fontWeight: 500 }}>
              {s.sub}
            </div>
          </div>
        );
      })}
    </div>
  );
})()
```

```aura width=860 height=230
(function() {
  var projects = [
    {
      title: 'Pennora',
      tag: 'FINTECH APP',
      color: '#a78bfa',
      desc: 'Smart spare-change micro-investing platform democratizing wealth creation with automated portfolio balancing.',
      tech: 'Flutter · Firebase · Provider',
    },
    {
      title: 'Smart Trip Planner',
      tag: 'AI TRAVEL',
      color: '#38bdf8',
      desc: 'Intelligent trip planning application generating tailored schedules & recommendations via Google Gemini AI.',
      tech: 'Flutter · Gemini AI · Dart',
    },
    {
      title: 'PrepGenius',
      tag: 'EDTECH PLATFORM',
      color: '#34d399',
      desc: 'Full-featured learning web application with solved previous papers, curated video playlists & interactive quizzes.',
      tech: 'React.js · JavaScript · Modern UI',
    },
  ];

  return (
    <div style={{
      width: '100%', height: '100%',
      background: '#080811',
      display: 'flex', flexDirection: 'column',
      fontFamily: 'Inter, sans-serif', padding: '18px 24px',
      borderRadius: 18, border: '1px solid rgba(139, 92, 246, 0.22)',
      position: 'relative', overflow: 'hidden', gap: 14
    }}>

      <style>{`
        @keyframes pr-orb-float { 0%, 100% { transform: translateY(0px); opacity: 0.45; } 50% { transform: translateY(-25px); opacity: 0.8; } }
        #pr-g1 { animation: pr-orb-float 9s ease-in-out infinite; }
      `}</style>

      <svg width="860" height="230" style={{ position: 'absolute', top: 0, left: 0 }}>
        <defs>
          <radialGradient id="pg-1" cx="50%" cy="50%" r="50%">
            <stop offset="0%" stopColor="rgba(139, 92, 246, 0.4)" />
            <stop offset="60%" stopColor="rgba(109, 40, 217, 0.1)" />
            <stop offset="75%" stopColor="rgba(109, 40, 217, 0)" />
          </radialGradient>
        </defs>
        <ellipse id="pr-g1" cx="430" cy="220" rx="380" ry="170" fill="url(#pg-1)" />
      </svg>

      <div style={{ display: 'flex', alignItems: 'center' }}>
        <div style={{ display: 'flex', fontSize: 11, fontWeight: 700, color: 'rgba(167, 139, 250, 0.85)', letterSpacing: '2.5px' }}>
          FEATURED PROJECTS & ARCHITECTURE
        </div>
      </div>

      <div style={{ display: 'flex', gap: 14, flex: 1 }}>
        {projects.map(function(p) {
          return (
            <div key={p.title} style={{
              flex: 1, display: 'flex', flexDirection: 'column',
              background: 'rgba(255, 255, 255, 0.035)',
              borderRadius: 14, padding: '14px 16px',
              border: '1px solid rgba(255, 255, 255, 0.09)',
              borderTop: '2px solid ' + p.color,
              justifyContent: 'space-between'
            }}>
              <div style={{ display: 'flex', flexDirection: 'column', gap: 6 }}>
                <div style={{ display: 'flex', fontSize: 10, fontWeight: 700, color: p.color, letterSpacing: '1px' }}>
                  {p.tag}
                </div>
                <div style={{ display: 'flex', fontSize: 16, fontWeight: 700, color: '#ffffff' }}>
                  {p.title}
                </div>
                <div style={{ display: 'flex', fontSize: 12, color: 'rgba(220, 215, 245, 0.8)', lineHeight: 1.38 }}>
                  {p.desc}
                </div>
              </div>
              <div style={{
                display: 'flex', fontSize: 11, fontWeight: 600,
                color: 'rgba(255, 255, 255, 0.55)', marginTop: 8,
                paddingTop: 8, borderTop: '1px solid rgba(255, 255, 255, 0.06)'
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

```aura width=860 height=190
(function() {
  var categories = [
    {
      title: 'Mobile & Frontend',
      color: '#a78bfa',
      items: ['Flutter', 'Dart', 'React.js', 'Next.js', 'TypeScript', 'Tailwind CSS']
    },
    {
      title: 'Backend & AI',
      color: '#38bdf8',
      items: ['FastAPI', 'Python', 'Google Gemini AI', 'Firebase', 'Node.js', 'REST APIs']
    },
    {
      title: 'Architecture & Tools',
      color: '#34d399',
      items: ['System Design', 'YOLO / CV', 'Git & GitHub', 'Docker', 'State Management']
    },
  ];

  return (
    <div style={{
      width: '100%', height: '100%',
      background: '#080811',
      display: 'flex', flexDirection: 'column',
      fontFamily: 'Inter, sans-serif', padding: '18px 28px', gap: 12,
      borderRadius: 18, border: '1px solid rgba(139, 92, 246, 0.22)',
      position: 'relative', overflow: 'hidden',
    }}>

      <style>{`
        @keyframes tech-glow-pulse { 0%, 100% { opacity: 0.35; } 50% { opacity: 0.75; } }
        #tg-1 { animation: tech-glow-pulse 8s ease-in-out infinite; }
      `}</style>

      <svg width="860" height="190" style={{ position: 'absolute', top: 0, left: 0 }}>
        <defs>
          <radialGradient id="t-g1" cx="50%" cy="50%" r="50%">
            <stop offset="0%" stopColor="rgba(6, 182, 212, 0.45)" />
            <stop offset="50%" stopColor="rgba(14, 116, 144, 0.15)" />
            <stop offset="70%" stopColor="rgba(14, 116, 144, 0)" />
          </radialGradient>
        </defs>
        <ellipse id="tg-1" cx="720" cy="170" rx="220" ry="140" fill="url(#t-g1)" />
      </svg>

      <div style={{ display: 'flex', fontSize: 11, fontWeight: 700, color: 'rgba(167, 139, 250, 0.85)', letterSpacing: '2.5px' }}>
        TECH STACK & CAPABILITIES
      </div>

      <div style={{ display: 'flex', flexDirection: 'column', gap: 10 }}>
        {categories.map(function(cat) {
          return (
            <div key={cat.title} style={{ display: 'flex', alignItems: 'center', gap: 14 }}>
              <div style={{ display: 'flex', fontSize: 11, fontWeight: 700, color: cat.color, letterSpacing: '0.8px', width: 140 }}>
                {cat.title}
              </div>
              <div style={{ display: 'flex', flexWrap: 'wrap', gap: 7, flex: 1 }}>
                {cat.items.map(function(item) {
                  return (
                    <div key={item} style={{
                      display: 'flex', padding: '4px 12px', borderRadius: 8,
                      background: cat.color + '15', border: '1px solid ' + cat.color + '35',
                      color: 'rgba(245, 240, 255, 0.95)', fontSize: 12, fontWeight: 600,
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
  backgroundColor="#131126"
  width={130}
  height={44}
  gradientStops={[
    { offset: '0%', color: '#ffffff' },
    { offset: '15%', color: '#1a103c' },
    { offset: '50%', color: '#a78bfa' },
    { offset: '60%', color: '#ffffff' },
    { offset: '85%', color: '#1a103c' },
    { offset: '100%', color: '#6d28d9' },
  ]}
/>
```

```aura width=120 height=44 link="https://github.com/LordNydorf" inline align=center
<SocialMediaButton
  icon="https://cdn.simpleicons.org/github/ffffff"
  text="GitHub"
  backgroundColor="#141414"
  width={120}
  height={44}
  gradientStops={[
    { offset: '0%', color: '#ffffff' },
    { offset: '10%', color: '#111111' },
    { offset: '50%', color: '#eeeeee' },
    { offset: '60%', color: '#ffffff' },
    { offset: '80%', color: '#111111' },
    { offset: '100%', color: '#555555' },
  ]}
/>
```

```aura width=120 height=44 link="https://x.com/r_hxt_" inline align=center
<SocialMediaButton
  icon="https://cdn.simpleicons.org/x/ffffff"
  text="X.com"
  backgroundColor="#141414"
  width={120}
  height={44}
  gradientStops={[
    { offset: '0%', color: '#ffffff' },
    { offset: '10%', color: '#111111' },
    { offset: '50%', color: '#eeeeee' },
    { offset: '60%', color: '#ffffff' },
    { offset: '80%', color: '#111111' },
    { offset: '100%', color: '#555555' },
  ]}
/>
```

```aura width=110 height=44 link="mailto:rohitkrishnanofficial@gmail.com" inline align=center
<SocialMediaButton
  icon="https://cdn.simpleicons.org/gmail/EA4335"
  text="Email"
  backgroundColor="#2b0a0a"
  width={110}
  height={44}
  gradientStops={[
    { offset: '0%', color: '#ffffff' },
    { offset: '10%', color: '#111111' },
    { offset: '50%', color: '#eeeeee' },
    { offset: '60%', color: '#EA4335' },
    { offset: '80%', color: '#111111' },
    { offset: '100%', color: '#555555' },
  ]}
/>
```

```aura width=860 height=24 link="https://collectioneur.github.io/readme-aura/"
<div style={{ display: 'flex', justifyContent: 'center', alignItems: 'center', width: '100%', height: '100%', padding: 0, margin: 0 }}>
  <span style={{ fontSize: 12, lineHeight: 1, color: 'rgba(150, 140, 200, 0.55)', fontWeight: 500, letterSpacing: '0.4px' }}>powered by readme-aura · satori</span>
</div>
```
