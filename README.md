
<!-- @dsCard group="Portfolio" viewport="1280x760" name="Portfolio site — full page" subtitle="Hero, about, skills, featured work, stats, connect" -->
<!-- @startingPoint section="Portfolio" subtitle="Data-analyst portfolio landing page" viewport="1280x760" -->
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Supraja K — Data Analyst</title>
<link rel="preconnect" href="https://fonts.googleapis.com" />
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Fira+Code:wght@400;500;600;700&family=IBM+Plex+Sans:ital,wght@0,400;0,500;0,600;0,700;1,400&display=swap" />
<style>
/* ── Tokens ── */
:root {
  --navy-950: #07090f;
  --navy-900: #0a0e17;
  --navy-850: #0d1220;
  --navy-800: #11182a;
  --navy-750: #161e33;
  --navy-700: #1c2333;
  --navy-600: #2a3349;
  --navy-500: #3a465f;

  --cyan-300: #7fe6ff;
  --cyan-400: #2ad0f0;
  --cyan-500: #00b4d8;
  --cyan-600: #0090b0;
  --cyan-700: #006d86;
  --cyan-glow: rgba(0,180,216,0.28);

  --text-hi:  #ffffff;
  --text-mid: #c3cee0;
  --text-low: #8b9cbe;
  --text-dim: #5b6a8a;

  --viz-cyan:   #00b4d8;
  --viz-coral:  #ff6b6b;
  --viz-amber:  #f2c811;
  --viz-blue:   #4d77cf;
  --viz-snow:   #29b5e8;
  --viz-violet: #9d7bff;
  --viz-mint:   #3dd7a6;

  --status-up:   #3dd7a6;
  --status-down: #ff6b6b;
  --status-warn: #f2c811;
  --status-info: #00b4d8;

  --bg-page:       var(--navy-900);
  --bg-raised:     var(--navy-850);
  --surface-card:  var(--navy-800);
  --surface-hover: var(--navy-750);
  --surface-inset: var(--navy-950);

  --border-subtle: var(--navy-700);
  --border-strong: var(--navy-600);
  --border-accent: var(--cyan-500);

  --text-heading: var(--text-hi);
  --text-body:    var(--text-mid);
  --text-muted:   var(--text-low);
  --text-faint:   var(--text-dim);

  --accent:         var(--cyan-500);
  --accent-hover:   var(--cyan-400);
  --accent-press:   var(--cyan-600);
  --accent-contrast:#07090f;

  --font-mono:    'Fira Code', 'SF Mono', ui-monospace, Menlo, Consolas, monospace;
  --font-sans:    'IBM Plex Sans', system-ui, -apple-system, 'Segoe UI', sans-serif;
  --font-display: var(--font-mono);

  --fw-regular: 400;
  --fw-medium:  500;
  --fw-semibold:600;
  --fw-bold:    700;

  --fs-display:   3.5rem;
  --fs-h1:        2.5rem;
  --fs-h2:        1.875rem;
  --fs-h3:        1.375rem;
  --fs-h4:        1.125rem;
  --fs-body:      1rem;
  --fs-sm:        0.875rem;
  --fs-xs:        0.75rem;
  --fs-mono-stat: 2.75rem;

  --lh-tight:   1.1;
  --lh-snug:    1.3;
  --lh-normal:  1.55;
  --lh-relaxed: 1.7;

  --ls-tight:  -0.02em;
  --ls-normal:  0;
  --ls-wide:    0.04em;
  --ls-label:   0.12em;

  --space-0: 0;
  --space-1: 0.25rem;
  --space-2: 0.5rem;
  --space-3: 0.75rem;
  --space-4: 1rem;
  --space-5: 1.5rem;
  --space-6: 2rem;
  --space-7: 3rem;
  --space-8: 4rem;
  --space-9: 6rem;

  --radius-xs:  4px;
  --radius-sm:  6px;
  --radius-md:  10px;
  --radius-lg:  14px;
  --radius-pill:999px;

  --shadow-sm:   0 1px 2px rgba(0,0,0,0.4);
  --shadow-md:   0 6px 20px rgba(0,0,0,0.45);
  --shadow-lg:   0 18px 44px rgba(0,0,0,0.55);
  --shadow-glow: 0 0 0 1px var(--cyan-500), 0 0 24px var(--cyan-glow);

  --ease-out:    cubic-bezier(0.22, 1, 0.36, 1);
  --ease-in-out: cubic-bezier(0.65, 0, 0.35, 1);
  --dur-fast: 120ms;
  --dur-base: 200ms;
  --dur-slow: 360ms;

  --container-max:  1120px;
  --container-wide: 1320px;
}

/* ── Base ── */
*, *::before, *::after { box-sizing: border-box; }
html, body { margin: 0; }
body {
  background: var(--bg-page);
  color: var(--text-body);
  font-family: var(--font-sans);
  font-size: var(--fs-body);
  line-height: var(--lh-normal);
  -webkit-font-smoothing: antialiased;
  text-rendering: optimizeLegibility;
}
::selection { background: var(--cyan-glow); color: var(--text-hi); }

/* ── Animations ── */
@keyframes blink { 0%, 100% { opacity: 1 } 50% { opacity: 0 } }
@keyframes wave  { 0%, 60%, 100% { transform: rotate(0) } 15% { transform: rotate(16deg) } 30% { transform: rotate(-8deg) } 45% { transform: rotate(16deg) } }

/* ── Dotted console grid backdrop ── */
body::before {
  content: '';
  position: fixed;
  inset: 0;
  pointer-events: none;
  z-index: 0;
  background-image: radial-gradient(circle, rgba(0,180,216,0.05) 1px, transparent 1px);
  background-size: 32px 32px;
}
#app { position: relative; z-index: 1; }
</style>
</head>
<body>
<div id="app"></div>

<script src="https://unpkg.com/react@18.3.1/umd/react.development.js" integrity="sha384-hD6/rw4ppMLGNu3tX5cjIb+uRZ7UkRJ6BPkLpg4hAu/6onKUg4lLsHAs9EBPT82L" crossorigin="anonymous"></script>
<script src="https://unpkg.com/react-dom@18.3.1/umd/react-dom.development.js" integrity="sha384-u6aeetuaXnQ38mYT8rp6sbXaQe3NL9t+IBXmnYxwkUI2Hw4bsp2Wvmx4yRQF1uAm" crossorigin="anonymous"></script>
<script src="https://unpkg.com/@babel/standalone@7.29.0/babel.min.js" integrity="sha384-m08KidiNqLdpJqLq95G/LEi8Qvjl/xUYll3QILypMoQ65QorJ9Lvtp2RXYGBFj1y" crossorigin="anonymous"></script>

<!-- ── Core design-system components ── -->
<script type="text/babel">
/* Badge — shields.io-style two-tone chip */
function Badge({ label, value, color = 'var(--accent)', icon = null, style = {} }) {
  const base = {
    display: 'inline-flex', alignItems: 'center',
    fontFamily: 'var(--font-mono)', fontSize: 11, fontWeight: 600,
    letterSpacing: '0.04em', textTransform: 'uppercase', lineHeight: 1,
    borderRadius: 'var(--radius-xs)', overflow: 'hidden',
    border: '1px solid var(--border-subtle)',
  };
  if (value != null && value !== '') {
    return (
      <span style={{ ...base, ...style }}>
        <span style={{ display: 'inline-flex', alignItems: 'center', gap: 5, padding: '5px 8px', background: 'var(--navy-950)', color: 'var(--text-low)' }}>
          {icon}{label}
        </span>
        <span style={{ padding: '5px 8px', background: color, color: 'var(--accent-contrast)' }}>{value}</span>
      </span>
    );
  }
  return (
    <span style={{ ...base, borderRadius: 'var(--radius-pill)', padding: '5px 10px', gap: 5, background: 'var(--navy-950)', color, ...style }}>
      {icon}{label}
    </span>
  );
}

/* Avatar — initials or image with optional cyan ring */
function Avatar({ src = null, initials = '', size = 48, ring = false, style = {} }) {
  return (
    <span style={{
      display: 'inline-flex', alignItems: 'center', justifyContent: 'center',
      width: size, height: size, borderRadius: '50%', flex: 'none',
      fontFamily: 'var(--font-mono)', fontWeight: 600, fontSize: size * 0.36,
      color: 'var(--accent)', background: 'var(--surface-card)',
      border: ring ? '2px solid var(--accent)' : '1px solid var(--border-strong)',
      boxShadow: ring ? '0 0 0 4px color-mix(in srgb, var(--accent) 14%, transparent)' : 'none',
      overflow: 'hidden', letterSpacing: '0.02em', ...style,
    }}>
      {src ? <img src={src} alt={initials} style={{ width: '100%', height: '100%', objectFit: 'cover' }} /> : initials}
    </span>
  );
}

/* Tag — compact mono chip for skills */
function Tag({ children, dot = false, active = false, style = {} }) {
  return (
    <span style={{
      display: 'inline-flex', alignItems: 'center', gap: 7,
      padding: '5px 11px', fontFamily: 'var(--font-mono)', fontSize: 12,
      fontWeight: 500, lineHeight: 1,
      color: active ? 'var(--text-hi)' : 'var(--text-muted)',
      background: active ? 'color-mix(in srgb, var(--accent) 12%, transparent)' : 'var(--surface-inset)',
      border: '1px solid ' + (active ? 'color-mix(in srgb, var(--accent) 50%, transparent)' : 'var(--border-subtle)'),
      borderRadius: 'var(--radius-pill)', ...style,
    }}>
      {dot && <span style={{ width: 6, height: 6, borderRadius: '50%', background: 'var(--accent)', boxShadow: '0 0 8px var(--cyan-glow)' }} />}
      {children}
    </span>
  );
}

/* Card — base surface with optional emphasis + hover lift */
function Card({ children, emphasis = false, hover = false, padding = 'var(--space-5)', as: As = 'div', style = {}, ...rest }) {
  const [h, setH] = React.useState(false);
  return (
    <As
      onMouseEnter={hover ? () => setH(true) : undefined}
      onMouseLeave={hover ? () => setH(false) : undefined}
      style={{
        background: 'var(--surface-card)',
        border: '1px solid ' + (emphasis ? 'color-mix(in srgb, var(--accent) 40%, transparent)' : (h ? 'var(--border-strong)' : 'var(--border-subtle)')),
        borderRadius: 'var(--radius-lg)',
        padding,
        boxShadow: emphasis
          ? 'var(--shadow-md), 0 0 24px color-mix(in srgb, var(--accent) 12%, transparent)'
          : (h ? 'var(--shadow-lg)' : 'var(--shadow-sm)'),
        transform: h ? 'translateY(-3px)' : 'none',
        transition: 'transform var(--dur-base) var(--ease-out), box-shadow var(--dur-base) var(--ease-out), border-color var(--dur-base) var(--ease-out)',
        ...style,
      }}
      {...rest}
    >
      {children}
    </As>
  );
}

/* StatCard — headline metric tile */
function StatCard({ label, value, delta = null, direction = 'up', caption = '', accent = 'var(--accent)', style = {} }) {
  const deltaColor = direction === 'down' ? 'var(--status-down)' : 'var(--status-up)';
  const arrow = direction === 'down' ? '▾' : '▴';
  return (
    <div style={{
      position: 'relative', background: 'var(--surface-card)',
      border: '1px solid var(--border-subtle)', borderRadius: 'var(--radius-lg)',
      padding: 'var(--space-5)', overflow: 'hidden', ...style,
    }}>
      <div style={{ position: 'absolute', top: 0, left: 0, width: 3, height: '100%', background: accent }} />
      <div style={{ fontFamily: 'var(--font-mono)', fontSize: 11, fontWeight: 500, letterSpacing: '0.12em', textTransform: 'uppercase', color: 'var(--text-muted)' }}>{label}</div>
      <div style={{ fontFamily: 'var(--font-mono)', fontWeight: 600, color: 'var(--text-hi)', fontSize: 'var(--fs-mono-stat)', lineHeight: 1.05, margin: '10px 0 6px', letterSpacing: '-0.01em' }}>{value}</div>
      <div style={{ display: 'flex', alignItems: 'center', gap: 8 }}>
        {delta != null && (
          <span style={{ fontFamily: 'var(--font-mono)', fontSize: 12, fontWeight: 600, color: deltaColor, display: 'inline-flex', alignItems: 'center', gap: 3 }}>{arrow} {delta}</span>
        )}
        {caption && <span style={{ fontSize: 12, color: 'var(--text-faint)' }}>{caption}</span>}
      </div>
    </div>
  );
}

/* Meter — horizontal progress bar */
function Meter({ label = '', value = 0, max = 100, display = null, color = 'var(--accent)', style = {} }) {
  const pct = Math.max(0, Math.min(100, (value / max) * 100));
  return (
    <div style={{ display: 'flex', flexDirection: 'column', gap: 8, ...style }}>
      {(label || display) && (
        <div style={{ display: 'flex', justifyContent: 'space-between', alignItems: 'baseline', fontFamily: 'var(--font-mono)', fontSize: 12 }}>
          <span style={{ color: 'var(--text-body)', fontWeight: 500 }}>{label}</span>
          <span style={{ color: 'var(--text-muted)' }}>{display != null ? display : Math.round(pct) + '%'}</span>
        </div>
      )}
      <div style={{ height: 6, borderRadius: 'var(--radius-pill)', background: 'var(--surface-inset)', overflow: 'hidden', border: '1px solid var(--border-subtle)' }}>
        <div style={{ width: pct + '%', height: '100%', borderRadius: 'var(--radius-pill)', background: color, boxShadow: '0 0 10px color-mix(in srgb, ' + color + ' 60%, transparent)', transition: 'width var(--dur-slow) var(--ease-out)' }} />
      </div>
    </div>
  );
}

window.__DS = { Badge, Avatar, Tag, Card, StatCard, Meter };
</script>

<!-- ── Portfolio: Nav + Hero ── -->
<script type="text/babel">
const LOGO_SVG = `data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='180' height='48' viewBox='0 0 180 48' fill='none'%3E%3Crect width='180' height='48' rx='8' fill='%230a0e17'/%3E%3Ctext x='14' y='32' font-family='Fira Code%2C monospace' font-size='22' font-weight='700' fill='%2300b4d8'%3E%3E%3C/text%3E%3Ctext x='38' y='32' font-family='Fira Code%2C monospace' font-size='22' font-weight='700' fill='%23ffffff' letter-spacing='1'%3ESK%3C/text%3E%3Ctext x='78' y='32' font-family='Fira Code%2C monospace' font-size='22' font-weight='500' fill='%238b9cbe'%3E.data%3C/text%3E%3Crect x='160' y='16' width='11' height='20' fill='%2300b4d8'/%3E%3C/svg%3E`;

function PortBtn({ children, onClick, variant = 'primary' }) {
  const [h, setH] = React.useState(false);
  const v = variant === 'primary'
    ? { background: h ? 'var(--accent-hover)' : 'var(--accent)', color: 'var(--accent-contrast)', border: '1px solid var(--accent)', boxShadow: h ? 'var(--shadow-glow)' : 'none' }
    : { background: 'transparent', color: h ? 'var(--text-hi)' : 'var(--text-body)', border: '1px solid ' + (h ? 'var(--accent)' : 'var(--border-strong)') };
  return (
    <button onClick={onClick} onMouseEnter={() => setH(true)} onMouseLeave={() => setH(false)}
      style={{ fontFamily: 'var(--font-mono)', fontSize: 12, fontWeight: 600, letterSpacing: '0.02em', padding: '8px 14px', borderRadius: 'var(--radius-sm)', cursor: 'pointer', transition: 'all .2s', whiteSpace: 'nowrap', ...v }}>
      {children}
    </button>
  );
}

function PortfolioNav({ onCopyEmail, copied }) {
  const [hovered, setHovered] = React.useState(null);
  const items = ['about', 'skills', 'work', 'connect'];
  const link = { fontFamily: 'var(--font-mono)', fontSize: 13, textDecoration: 'none', letterSpacing: '0.02em', transition: 'color .2s' };
  return (
    <header style={{ position: 'sticky', top: 0, zIndex: 20, background: 'color-mix(in srgb, var(--bg-page) 82%, transparent)', backdropFilter: 'blur(12px)', borderBottom: '1px solid var(--border-subtle)' }}>
      <div style={{ maxWidth: 'var(--container-max)', margin: '0 auto', padding: '16px 28px', display: 'flex', alignItems: 'center', justifyContent: 'space-between' }}>
        <img src={LOGO_SVG} alt="SK.data" height="30" />
        <nav style={{ display: 'flex', gap: 26, alignItems: 'center' }}>
          {items.map(i => (
            <a key={i} href={'#' + i}
              style={{ ...link, color: hovered === i ? 'var(--accent)' : 'var(--text-muted)' }}
              onMouseEnter={() => setHovered(i)} onMouseLeave={() => setHovered(null)}>
              <span style={{ color: 'var(--accent)' }}>/</span>{i}
            </a>
          ))}
          <PortBtn onClick={onCopyEmail}>{copied ? 'copied ✓' : 'kanathalasupraja@gmail.com'}</PortBtn>
        </nav>
      </div>
    </header>
  );
}

function PortfolioHero() {
  const { Badge, Avatar } = window.__DS;
  const phrases = ['Data Analyst | Data Engineer', 'Turning Raw Data into Real Decisions', 'Python • SQL • Power BI • Cloud', 'Open to Work 🚀'];
  const [pi, setPi] = React.useState(0);
  const [txt, setTxt] = React.useState('');
  const [del, setDel] = React.useState(false);

  React.useEffect(() => {
    const full = phrases[pi];
    let t;
    if (!del && txt.length < full.length)       t = setTimeout(() => setTxt(full.slice(0, txt.length + 1)), 55);
    else if (!del && txt.length === full.length) t = setTimeout(() => setDel(true), 1400);
    else if (del && txt.length > 0)              t = setTimeout(() => setTxt(full.slice(0, txt.length - 1)), 28);
    else { setDel(false); setPi((pi + 1) % phrases.length); }
    return () => clearTimeout(t);
  }, [txt, del, pi]);

  return (
    <section style={{ maxWidth: 'var(--container-max)', margin: '0 auto', padding: '92px 28px 64px', display: 'grid', gridTemplateColumns: '1.45fr 1fr', gap: 56, alignItems: 'center' }}>
      <div>
        <div style={{ fontFamily: 'var(--font-mono)', fontSize: 13, letterSpacing: '0.12em', textTransform: 'uppercase', color: 'var(--text-muted)', marginBottom: 22 }}>
          <span style={{ color: 'var(--accent)' }}>&gt;</span> Toronto, Canada 🇨🇦
        </div>
        <h1 style={{ fontFamily: 'var(--font-mono)', fontWeight: 700, fontSize: 52, lineHeight: 1.08, letterSpacing: '-0.02em', color: 'var(--text-hi)', margin: 0 }}>
          Hi, I'm Supraja <span style={{ display: 'inline-block', animation: 'wave 2.2s ease-in-out infinite', transformOrigin: '70% 70%' }}>👋</span>
        </h1>
        <div style={{ fontFamily: 'var(--font-mono)', fontSize: 21, color: 'var(--accent)', margin: '20px 0 28px', minHeight: 30, fontWeight: 600 }}>
          {txt}
          <span style={{ display: 'inline-block', width: 10, height: 22, background: 'var(--accent)', verticalAlign: '-3px', marginLeft: 3, boxShadow: '0 0 10px var(--cyan-glow)', animation: 'blink 1s step-end infinite' }} />
        </div>
        <p style={{ fontSize: 17, lineHeight: 1.65, color: 'var(--text-mid)', maxWidth: 520, margin: '0 0 32px' }}>
          A data analyst and aspiring data engineer who spends hours inside a dataset just to find the one pattern nobody noticed.
        </p>
        <div style={{ display: 'flex', gap: 12 }}>
          <PortBtn>View Featured Project</PortBtn>
          <PortBtn variant="secondary">GitHub ↗</PortBtn>
        </div>
      </div>
      <div style={{ display: 'flex', flexDirection: 'column', alignItems: 'center', gap: 18 }}>
        <Avatar initials="SK" size={150} ring />
        <div style={{ display: 'flex', gap: 8, flexWrap: 'wrap', justifyContent: 'center' }}>
          <Badge label="Status" value="open to work" color="var(--status-up)" />
          <Badge label="Exp" value="retail · pharma" color="var(--viz-cyan)" />
        </div>
      </div>
    </section>
  );
}
</script>

<!-- ── Portfolio: About + Skills + Work + Stats ── -->
<script type="text/babel">
function SectionHead({ id, label, title }) {
  return (
    <div id={id} style={{ marginBottom: 28, scrollMarginTop: 80 }}>
      <div style={{ fontFamily: 'var(--font-mono)', fontSize: 12, letterSpacing: '0.14em', textTransform: 'uppercase', color: 'var(--text-muted)', marginBottom: 10 }}>
        <span style={{ color: 'var(--accent)' }}>&gt;</span> {label}
      </div>
      <h2 style={{ fontFamily: 'var(--font-mono)', fontWeight: 700, fontSize: 30, color: 'var(--text-hi)', margin: 0, letterSpacing: '-0.02em' }}>{title}</h2>
    </div>
  );
}

function PortfolioAbout() {
  const { Card } = window.__DS;
  const rows = [
    ['working on',  'personal data projects to build a strong, real-world portfolio'],
    ['learning',    'advanced SQL, Python for data, and cloud data tools (AWS, GCP)'],
    ['worked as',   'a Data Analyst in retail and pharma, across Canada and India'],
    ['ask me about','SQL, Python, Power BI, Excel, data cleaning, and dashboards'],
  ];
  return (
    <section style={{ maxWidth: 'var(--container-max)', margin: '0 auto', padding: '36px 28px' }}>
      <SectionHead id="about" label="About" title="A bit about me" />
      <Card>
        <div style={{ display: 'flex', flexDirection: 'column' }}>
          {rows.map(([k, v], i) => (
            <div key={k} style={{ display: 'flex', gap: 20, padding: '15px 0', borderBottom: i < rows.length - 1 ? '1px solid var(--border-subtle)' : 'none', alignItems: 'baseline' }}>
              <span style={{ fontFamily: 'var(--font-mono)', fontSize: 12, color: 'var(--accent)', minWidth: 130, letterSpacing: '0.04em' }}>{k}</span>
              <span style={{ fontSize: 15.5, color: 'var(--text-mid)', lineHeight: 1.55 }}>{v}</span>
            </div>
          ))}
        </div>
      </Card>
    </section>
  );
}

function PortfolioSkills() {
  const { Card, Tag, Meter } = window.__DS;
  const tools = ['Python','R','PostgreSQL','MySQL','MongoDB','AWS','Azure','GCP','Docker','Git','GitHub','Tableau','Snowflake','dbt','Spark','Pandas','NumPy'];
  const meters = [
    ['SQL',      92, 'var(--viz-cyan)'],
    ['Excel',    88, 'var(--viz-amber)'],
    ['Power BI', 84, 'var(--viz-snow)'],
    ['Python',   76, 'var(--viz-violet)'],
  ];
  return (
    <section style={{ maxWidth: 'var(--container-max)', margin: '0 auto', padding: '36px 28px' }}>
      <SectionHead id="skills" label="Stack" title="Languages & tools" />
      <div style={{ display: 'grid', gridTemplateColumns: '1.3fr 1fr', gap: 18 }}>
        <Card>
          <div style={{ fontFamily: 'var(--font-mono)', fontSize: 11, letterSpacing: '0.12em', textTransform: 'uppercase', color: 'var(--text-faint)', marginBottom: 16 }}>toolbox</div>
          <div style={{ display: 'flex', flexWrap: 'wrap', gap: 9 }}>
            {tools.map(t => <Tag key={t}>{t}</Tag>)}
          </div>
        </Card>
        <Card>
          <div style={{ fontFamily: 'var(--font-mono)', fontSize: 11, letterSpacing: '0.12em', textTransform: 'uppercase', color: 'var(--text-faint)', marginBottom: 18 }}>proficiency</div>
          <div style={{ display: 'flex', flexDirection: 'column', gap: 16 }}>
            {meters.map(([l, v, c]) => <Meter key={l} label={l} value={v} color={c} />)}
          </div>
        </Card>
      </div>
    </section>
  );
}

function PortfolioWork() {
  const { Card, Badge } = window.__DS;
  return (
    <section style={{ maxWidth: 'var(--container-max)', margin: '0 auto', padding: '36px 28px' }}>
      <SectionHead id="work" label="Featured Project" title="What I've shipped" />
      <div style={{ display: 'grid', gridTemplateColumns: '1.4fr 1fr', gap: 18 }}>
        <Card emphasis hover as="a" href="https://github.com/SuprajaK-1999" style={{ textDecoration: 'none', display: 'block' }}>
          <div style={{ fontSize: 30, marginBottom: 14 }}>📊</div>
          <div style={{ fontFamily: 'var(--font-mono)', fontSize: 20, fontWeight: 600, color: 'var(--text-hi)', marginBottom: 10 }}>Sales Data Analysis</div>
          <p style={{ fontSize: 15, lineHeight: 1.65, color: 'var(--text-mid)', margin: '0 0 18px', maxWidth: 460 }}>
            End-to-end sales analysis in Excel. Data cleaning, pivot tables, and dashboards that surface revenue trends, top products, and seasonal patterns.
          </p>
          <div style={{ display: 'flex', gap: 8, flexWrap: 'wrap' }}>
            <Badge label="Excel" color="var(--viz-amber)" />
            <Badge label="Analysis" color="var(--viz-cyan)" />
            <Badge label="View" value="on GitHub" color="var(--viz-snow)" />
          </div>
        </Card>
        <Card>
          <div style={{ fontSize: 30, marginBottom: 14 }}>🔧</div>
          <div style={{ fontFamily: 'var(--font-mono)', fontSize: 20, fontWeight: 600, color: 'var(--text-hi)', marginBottom: 10 }}>More coming soon</div>
          <p style={{ fontSize: 15, lineHeight: 1.65, color: 'var(--text-muted)', margin: '0 0 18px' }}>
            Currently building projects in Python, SQL, and cloud pipelines. This space is filling up fast.
          </p>
          <div style={{ display: 'flex', gap: 8, flexWrap: 'wrap' }}>
            <Badge label="Python" value="in progress" color="var(--viz-violet)" />
            <Badge label="SQL"    value="in progress" color="var(--viz-cyan)" />
          </div>
        </Card>
      </div>
    </section>
  );
}

function PortfolioStats() {
  const { StatCard } = window.__DS;
  return (
    <section style={{ maxWidth: 'var(--container-max)', margin: '0 auto', padding: '36px 28px' }}>
      <SectionHead label="GitHub Stats" title="By the numbers" />
      <div style={{ display: 'grid', gridTemplateColumns: 'repeat(4, 1fr)', gap: 16 }}>
        <StatCard label="Repositories"   value="12"  delta="2 new"  direction="up" caption="this quarter" />
        <StatCard label="Current Streak" value="18d" delta="active" direction="up" accent="var(--viz-snow)" />
        <StatCard label="Top Language"   value="SQL" caption="42% of commits" accent="var(--viz-amber)" />
        <StatCard label="Contributions"  value="640" delta="11%"    direction="up" accent="var(--viz-violet)" />
      </div>
    </section>
  );
}
</script>

<!-- ── Portfolio: Connect + Footer ── -->
<script type="text/babel">
function PortfolioConnect({ onCopyEmail, copied }) {
  const { Card } = window.__DS;
  const links = [
    ['Gmail',    'kanathalasupraja@gmail.com',    'var(--viz-coral)'],
    ['GitHub',   'github.com/SuprajaK-1999',      'var(--text-mid)'],
    ['LinkedIn', 'linkedin.com/in/supraja-k',     'var(--viz-snow)'],
  ];
  const [h, setH] = React.useState(null);
  return (
    <section id="connect" style={{ maxWidth: 'var(--container-max)', margin: '0 auto', padding: '40px 28px 24px', scrollMarginTop: 80 }}>
      <Card padding="var(--space-7)" style={{ textAlign: 'center', background: 'var(--bg-raised)' }}>
        <div style={{ fontFamily: 'var(--font-mono)', fontSize: 12, letterSpacing: '0.14em', textTransform: 'uppercase', color: 'var(--text-muted)', marginBottom: 14 }}>
          <span style={{ color: 'var(--accent)' }}>&gt;</span> Connect
        </div>
        <h2 style={{ fontFamily: 'var(--font-mono)', fontWeight: 700, fontSize: 30, color: 'var(--text-hi)', margin: '0 0 14px', letterSpacing: '-0.02em' }}>Let's talk data</h2>
        <p style={{ fontSize: 16, color: 'var(--text-muted)', maxWidth: 460, margin: '0 auto 28px', lineHeight: 1.6 }}>
          Open to data analyst and data engineering roles. The fastest way to reach me is email.
        </p>
        <div style={{ display: 'flex', gap: 12, justifyContent: 'center', flexWrap: 'wrap' }}>
          {links.map(([k, v, c]) => (
            <button key={k}
              onClick={k === 'Gmail' ? onCopyEmail : undefined}
              onMouseEnter={() => setH(k)}
              onMouseLeave={() => setH(null)}
              style={{ display: 'flex', flexDirection: 'column', alignItems: 'flex-start', gap: 5, padding: '13px 18px', background: 'var(--surface-inset)', border: '1px solid ' + (h === k ? c : 'var(--border-subtle)'), borderRadius: 'var(--radius-md)', cursor: 'pointer', transition: 'all .2s', minWidth: 180 }}>
              <span style={{ fontFamily: 'var(--font-mono)', fontSize: 11, letterSpacing: '0.1em', textTransform: 'uppercase', color: c }}>{k}</span>
              <span style={{ fontFamily: 'var(--font-mono)', fontSize: 13, color: 'var(--text-mid)' }}>
                {k === 'Gmail' && copied ? 'copied to clipboard ✓' : v}
              </span>
            </button>
          ))}
        </div>
      </Card>
      <div style={{ textAlign: 'center', marginTop: 36, paddingTop: 22, borderTop: '1px solid var(--border-subtle)', paddingBottom: 40 }}>
        <p style={{ fontFamily: 'var(--font-mono)', fontSize: 13, color: 'var(--text-faint)', fontStyle: 'italic', margin: 0 }}>
          "Data is not just numbers. It's the language of better decisions."
        </p>
      </div>
    </section>
  );
}
</script>

<!-- ── App mount ── -->
<script type="text/babel">
function App() {
  const [copied, setCopied] = React.useState(false);
  const copyEmail = () => {
    navigator.clipboard && navigator.clipboard.writeText('kanathalasupraja@gmail.com');
    setCopied(true);
    setTimeout(() => setCopied(false), 1800);
  };
  return (
    <React.Fragment>
      <PortfolioNav onCopyEmail={copyEmail} copied={copied} />
      <main>
        <PortfolioHero />
        <PortfolioAbout />
        <PortfolioSkills />
        <PortfolioWork />
        <PortfolioStats />
        <PortfolioConnect onCopyEmail={copyEmail} copied={copied} />
      </main>
    </React.Fragment>
  );
}

ReactDOM.createRoot(document.getElementById('app')).render(<App />);
</script>
</body>
</html>
