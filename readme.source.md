```aura width=860 height=260
<div style={{
  width: '100%', height: '100%', background: '#08080f',
  display: 'flex', alignItems: 'center', fontFamily: 'Inter, sans-serif',
  position: 'relative', overflow: 'hidden', borderRadius: 16,
  border: '1px solid rgba(139, 92, 246, 0.22)'
}}>

  <style>{`
    @keyframes float-slow {
      0%, 100% { transform: translateX(0px) translateY(0px); opacity: 0.75; }
      50% { transform: translateX(280px) translateY(-15px); opacity: 1.1; }
    }
    @keyframes float-medium {
      0%, 100% { transform: translateX(0px) translateY(0px); opacity: 0.65; }
      50% { transform: translateX(-220px) translateY(18px); opacity: 1.0; }
    }
    @keyframes float-fast {
      0%, 100% { transform: translateX(0px); opacity: 0.85; }
      50% { transform: translateX(180px); opacity: 0.55; }
    }
    @keyframes float-diagonal {
      0%, 100% { transform: translate(0px, 0px); opacity: 0.7; }
      50% { transform: translate(240px, 20px); opacity: 0.95; }
    }
    @keyframes ring-pulse {
      0%, 100% { opacity: 0.08; transform: scale(1); }
      50% { opacity: 0.22; transform: scale(1.05); }
    }
    #glow-1 { animation: float-slow 10s ease-in-out infinite; }
    #glow-2 { animation: float-medium 13s ease-in-out infinite; }
    #glow-3 { animation: float-fast 9s ease-in-out infinite; }
    #glow-4 { animation: float-slow 12s ease-in-out infinite reverse; }
    #glow-5 { animation: float-diagonal 11s ease-in-out infinite; }
    #glow-6 { animation: float-medium 15s ease-in-out infinite reverse; }
    #ring-1 { animation: ring-pulse 8s ease-in-out infinite; }
    #ring-2 { animation: ring-pulse 8s ease-in-out infinite 2s; }
  `}</style>

  <svg width="860" height="260" style={{ position: 'absolute', top: 0, left: 0 }}>
    <defs>
      <radialGradient id="h-g1" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(139, 92, 246, 0.7)" />
        <stop offset="45%" stopColor="rgba(109, 40, 217, 0.3)" />
        <stop offset="70%" stopColor="rgba(109, 40, 217, 0)" />
      </radialGradient>
      <radialGradient id="h-g2" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(6, 182, 212, 0.6)" />
        <stop offset="50%" stopColor="rgba(14, 116, 144, 0.22)" />
        <stop offset="70%" stopColor="rgba(14, 116, 144, 0)" />
      </radialGradient>
      <radialGradient id="h-g3" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(79, 70, 229, 0.55)" />
        <stop offset="50%" stopColor="rgba(67, 56, 202, 0.2)" />
        <stop offset="70%" stopColor="rgba(67, 56, 202, 0)" />
      </radialGradient>
      <radialGradient id="h-g4" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(16, 185, 129, 0.4)" />
        <stop offset="60%" stopColor="rgba(16, 185, 129, 0.1)" />
        <stop offset="75%" stopColor="rgba(16, 185, 129, 0)" />
      </radialGradient>
      <radialGradient id="h-g5" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(244, 63, 94, 0.45)" />
        <stop offset="55%" stopColor="rgba(244, 63, 94, 0.15)" />
        <stop offset="70%" stopColor="rgba(244, 63, 94, 0)" />
      </radialGradient>
    </defs>

    <ellipse id="glow-1" cx="160" cy="240" rx="260" ry="190" fill="url(#h-g1)" />
    <ellipse id="glow-2" cx="360" cy="250" rx="220" ry="160" fill="url(#h-g2)" />
    <ellipse id="glow-3" cx="580" cy="240" rx="200" ry="150" fill="url(#h-g3)" />
    <ellipse id="glow-4" cx="740" cy="250" rx="170" ry="130" fill="url(#h-g4)" />
    <ellipse id="glow-5" cx="300" cy="50"  rx="180" ry="130" fill="url(#h-g5)" />
    <ellipse id="glow-6" cx="680" cy="60"  rx="190" ry="140" fill="url(#h-g1)" />

    <circle id="ring-1" cx="720" cy="130" r="80"  fill="none" stroke="rgba(255,255,255,0.7)" strokeWidth="0.8" />
    <circle id="ring-2" cx="720" cy="130" r="130" fill="none" stroke="rgba(255,255,255,0.5)" strokeWidth="0.8" />
  </svg>

  <div style={{
    position: 'absolute', left: 42, top: 46, width: 104, height: 104,
    borderRadius: 52, background: 'linear-gradient(135deg, #8b5cf6, #06b6d4, #10b981)',
    display: 'flex', alignItems: 'center', justifyContent: 'center'
  }}>
    <img
      src={(github && github.user && github.user.avatarUrl) || 'https://github.com/LordNydorf.png'}
      width={96}
      height={96}
      style={{ borderRadius: 48 }}
    />
  </div>

  <div style={{ display: 'flex', flexDirection: 'column', marginLeft: 172, marginRight: 36, gap: 7 }}>
    <div style={{ display: 'flex', alignItems: 'center', gap: 10 }}>
      <div style={{
        display: 'flex', padding: '3px 10px', borderRadius: 12,
        background: 'rgba(139, 92, 246, 0.18)', border: '1px solid rgba(167, 139, 250, 0.35)',
        color: '#c4b5fd', fontSize: 11, fontWeight: 700, letterSpacing: '1.2px'
      }}>
        FOUNDING ENGINEER
      </div>
      <div style={{ display: 'flex', fontSize: 12, color: 'rgba(255, 255, 255, 0.45)', fontWeight: 500 }}>
        📍 Kochi, Kerala, India
      </div>
    </div>

    <div style={{ display: 'flex', fontSize: 36, fontWeight: 800, color: '#ffffff', letterSpacing: '-0.8px', lineHeight: 1.1 }}>
      {(github && github.user && (github.user.name || github.user.login)) || 'Rohit Krishnan'}
    </div>

    <div style={{ display: 'flex', fontSize: 14, color: 'rgba(220, 215, 255, 0.88)', fontWeight: 500, letterSpacing: '0.2px' }}>
      {(github && github.user && github.user.bio) || 'Founding Engineer | Flutter, React, FastAPI, AI integration | Building 0 -> 1 products.'}
    </div>

    <div style={{ display: 'flex', gap: 8, marginTop: 4, flexWrap: 'wrap' }}>
      {['Flutter / Dart', 'React & Next.js', 'FastAPI & Python', 'AI & Gemini', '@2DoPros'].map(function(tag, i) {
        return (
          <div key={tag + '-' + i} style={{
            display: 'flex', padding: '4px 12px', borderRadius: 20,
            background: 'rgba(255, 255, 255, 0.05)', border: '1px solid rgba(255, 255, 255, 0.12)',
            color: 'rgba(235, 230, 255, 0.9)', fontSize: 11, fontWeight: 600,
          }}>{tag}</div>
        );
      })}
    </div>
  </div>
</div>
```

```aura width=860 height=130
(function() {
  var repos = String((github && github.stats && github.stats.totalRepos) || 12);
  var stars = String((github && github.stats && github.stats.totalStars) || 0);
  var commits = String((github && github.stats && github.stats.totalCommits) || '150+');

  var stats = [
    { label: 'Repositories', value: repos, color: '#a78bfa' },
    { label: 'Total Stars', value: stars, color: '#38bdf8' },
    { label: 'Contributions', value: commits, color: '#34d399' },
    { label: 'Specialization', value: '0 → 1 Products', color: '#f59e0b' },
  ];

  return (
    <div style={{
      width: '100%', height: '100%',
      background: '#08080f',
      display: 'flex', alignItems: 'center', justifyContent: 'center',
      fontFamily: 'Inter, sans-serif', borderRadius: 16,
      border: '1px solid rgba(139, 92, 246, 0.18)',
      position: 'relative', overflow: 'hidden',
    }}>

      <style>{`
        @keyframes stat-orb-a { 0%, 100% { transform: translateX(0px); opacity: 0.6; } 50% { transform: translateX(200px); opacity: 0.9; } }
        @keyframes stat-orb-b { 0%, 100% { transform: translateX(0px); opacity: 0.5; } 50% { transform: translateX(-180px); opacity: 0.85; } }
        #st-g1 { animation: stat-orb-a 9s ease-in-out infinite; }
        #st-g2 { animation: stat-orb-b 11s ease-in-out infinite; }
      `}</style>

      <svg width="860" height="130" style={{ position: 'absolute', top: 0, left: 0 }}>
        <defs>
          <radialGradient id="sg-1" cx="50%" cy="50%" r="50%">
            <stop offset="0%" stopColor="rgba(139, 92, 246, 0.5)" />
            <stop offset="50%" stopColor="rgba(109, 40, 217, 0.2)" />
            <stop offset="70%" stopColor="rgba(109, 40, 217, 0)" />
          </radialGradient>
          <radialGradient id="sg-2" cx="50%" cy="50%" r="50%">
            <stop offset="0%" stopColor="rgba(6, 182, 212, 0.45)" />
            <stop offset="50%" stopColor="rgba(14, 116, 144, 0.18)" />
            <stop offset="70%" stopColor="rgba(14, 116, 144, 0)" />
          </radialGradient>
        </defs>
        <ellipse id="st-g1" cx="220" cy="130" rx="200" ry="120" fill="url(#sg-1)" />
        <ellipse id="st-g2" cx="640" cy="130" rx="220" ry="130" fill="url(#sg-2)" />
      </svg>

      {stats.map(function(s, i) {
        return (
          <div key={s.label} style={{
            flex: 1, display: 'flex', flexDirection: 'column',
            alignItems: 'center', justifyContent: 'center',
            padding: '14px 8px',
            borderRight: i < stats.length - 1 ? '1px solid rgba(255, 255, 255, 0.07)' : 'none',
            gap: 6
          }}>
            <div style={{ display: 'flex', fontSize: 26, fontWeight: 800, color: s.color, lineHeight: 1 }}>
              {s.value}
            </div>
            <div style={{ display: 'flex', fontSize: 11, color: 'rgba(210, 205, 235, 0.55)', fontWeight: 600, letterSpacing: '1.2px' }}>
              {s.label.toUpperCase()}
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
      tag: 'FINTECH · FLUTTER',
      color: '#a78bfa',
      desc: 'Sophisticated micro-investing platform democratizing wealth building via automated spare change investing.',
      tech: 'Flutter · Firebase · Architecture',
    },
    {
      title: 'Smart Trip Planner',
      tag: 'AI · GEMINI',
      color: '#38bdf8',
      desc: 'AI-powered travel planner that generates personalized itineraries using Google Gemini AI.',
      tech: 'Flutter · Gemini AI · Dart',
    },
    {
      title: 'PrepGenius',
      tag: 'EDTECH · WEB',
      color: '#34d399',
      desc: 'Exam preparation & CS learning web application with solved past papers and interactive quizzes.',
      tech: 'React.js · JavaScript · Web',
    },
  ];

  return (
    <div style={{
      width: '100%', height: '100%',
      background: '#08080f',
      display: 'flex', flexDirection: 'column',
      fontFamily: 'Inter, sans-serif', padding: '18px 24px',
      borderRadius: 16, border: '1px solid rgba(139, 92, 246, 0.18)',
      position: 'relative', overflow: 'hidden', gap: 12
    }}>

      <style>{`
        @keyframes pr-orb { 0%, 100% { transform: translateY(0px); opacity: 0.5; } 50% { transform: translateY(-20px); opacity: 0.85; } }
        #pr-g1 { animation: pr-orb 8s ease-in-out infinite; }
      `}</style>

      <svg width="860" height="230" style={{ position: 'absolute', top: 0, left: 0 }}>
        <defs>
          <radialGradient id="pg-1" cx="50%" cy="50%" r="50%">
            <stop offset="0%" stopColor="rgba(139, 92, 246, 0.4)" />
            <stop offset="60%" stopColor="rgba(109, 40, 217, 0.1)" />
            <stop offset="75%" stopColor="rgba(109, 40, 217, 0)" />
          </radialGradient>
        </defs>
        <ellipse id="pr-g1" cx="430" cy="220" rx="360" ry="160" fill="url(#pg-1)" />
      </svg>

      <div style={{ display: 'flex', alignItems: 'center', justifyContent: 'space-between' }}>
        <div style={{ display: 'flex', fontSize: 11, fontWeight: 700, color: 'rgba(167, 139, 250, 0.8)', letterSpacing: '2.5px' }}>
          FEATURED PROJECTS & PRODUCTS
        </div>
        <div style={{ display: 'flex', fontSize: 11, color: 'rgba(255, 255, 255, 0.4)', fontWeight: 500 }}>
          Crafted with care 🚀
        </div>
      </div>

      <div style={{ display: 'flex', gap: 14, flex: 1 }}>
        {projects.map(function(p) {
          return (
            <div key={p.title} style={{
              flex: 1, display: 'flex', flexDirection: 'column',
              background: 'rgba(255, 255, 255, 0.03)',
              borderRadius: 12, padding: '14px 16px',
              border: '1px solid rgba(255, 255, 255, 0.08)',
              justifyContent: 'space-between'
            }}>
              <div style={{ display: 'flex', flexDirection: 'column', gap: 6 }}>
                <div style={{ display: 'flex', fontSize: 10, fontWeight: 700, color: p.color, letterSpacing: '1px' }}>
                  {p.tag}
                </div>
                <div style={{ display: 'flex', fontSize: 16, fontWeight: 700, color: '#ffffff' }}>
                  {p.title}
                </div>
                <div style={{ display: 'flex', fontSize: 12, color: 'rgba(215, 210, 240, 0.75)', lineHeight: 1.35 }}>
                  {p.desc}
                </div>
              </div>
              <div style={{
                display: 'flex', fontSize: 11, fontWeight: 600,
                color: 'rgba(255, 255, 255, 0.5)', marginTop: 8,
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
      background: '#08080f',
      display: 'flex', flexDirection: 'column',
      fontFamily: 'Inter, sans-serif', padding: '18px 28px', gap: 12,
      borderRadius: 16, border: '1px solid rgba(139, 92, 246, 0.18)',
      position: 'relative', overflow: 'hidden',
    }}>

      <style>{`
        @keyframes tech-glow { 0%, 100% { opacity: 0.4; } 50% { opacity: 0.8; } }
        #tg-1 { animation: tech-glow 7s ease-in-out infinite; }
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

      <div style={{ display: 'flex', fontSize: 11, fontWeight: 700, color: 'rgba(167, 139, 250, 0.8)', letterSpacing: '2.5px' }}>
        TECH STACK & CORE CAPABILITIES
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
                      background: cat.color + '14', border: '1px solid ' + cat.color + '33',
                      color: 'rgba(240, 235, 255, 0.9)', fontSize: 12, fontWeight: 600,
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
