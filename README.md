<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Supraja Kanathala — Data Analyst</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&family=Inter:wght@400;500;600&family=JetBrains+Mono:wght@400;500;600&display=swap" rel="stylesheet">
<style>
  :root {
    --bg: #0d1117;
    --bg-soft: #131a24;
    --card: #161e2b;
    --border: #232d3b;
    --text: #e6edf3;
    --muted: #8b98a9;
    --accent: #4dd0c5;
    --accent-warm: #f2b757;
    --line: rgba(77, 208, 197, 0.12);
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  html { scroll-behavior: smooth; }

  body {
    background: var(--bg);
    background-image:
      radial-gradient(circle at 18% 8%, rgba(77,208,197,0.06), transparent 40%),
      radial-gradient(circle at 85% 30%, rgba(242,183,87,0.05), transparent 40%);
    color: var(--text);
    font-family: 'Inter', sans-serif;
    line-height: 1.6;
    -webkit-font-smoothing: antialiased;
  }

  .wrap { max-width: 940px; margin: 0 auto; padding: 0 24px; }

  /* Hero */
  header {
    padding: 96px 0 64px;
    border-bottom: 1px solid var(--border);
    position: relative;
  }

  .tag {
    font-family: 'JetBrains Mono', monospace;
    font-size: 13px;
    color: var(--accent);
    letter-spacing: 0.5px;
    margin-bottom: 20px;
    display: inline-block;
  }

  h1 {
    font-family: 'Space Grotesk', sans-serif;
    font-size: clamp(38px, 7vw, 68px);
    font-weight: 700;
    line-height: 1.05;
    letter-spacing: -1.5px;
    margin-bottom: 18px;
  }

  .role {
    font-family: 'Space Grotesk', sans-serif;
    font-size: clamp(18px, 3vw, 24px);
    font-weight: 500;
    color: var(--muted);
    margin-bottom: 28px;
  }

  .role .hl { color: var(--text); }

  .location {
    font-family: 'JetBrains Mono', monospace;
    font-size: 14px;
    color: var(--muted);
  }

  /* Sections */
  section { padding: 64px 0; border-bottom: 1px solid var(--border); }

  .eyebrow {
    font-family: 'JetBrains Mono', monospace;
    font-size: 13px;
    color: var(--accent);
    letter-spacing: 1px;
    text-transform: uppercase;
    margin-bottom: 28px;
    display: flex;
    align-items: center;
    gap: 12px;
  }
  .eyebrow::after {
    content: "";
    flex: 1;
    height: 1px;
    background: var(--border);
  }

  h2 {
    font-family: 'Space Grotesk', sans-serif;
    font-size: 28px;
    font-weight: 600;
    margin-bottom: 18px;
    letter-spacing: -0.5px;
  }

  .lede { color: var(--muted); font-size: 17px; max-width: 660px; }
  .lede strong { color: var(--text); font-weight: 600; }

  /* Tech stack */
  .stack-group { margin-bottom: 32px; }
  .stack-group:last-child { margin-bottom: 0; }

  .stack-label {
    font-family: 'Space Grotesk', sans-serif;
    font-size: 16px;
    font-weight: 600;
    margin-bottom: 14px;
    color: var(--text);
  }

  .chips { display: flex; flex-wrap: wrap; gap: 10px; }

  .chip {
    font-family: 'JetBrains Mono', monospace;
    font-size: 13px;
    font-weight: 500;
    letter-spacing: 0.5px;
    text-transform: uppercase;
    color: #fff;
    padding: 9px 16px;
    border-radius: 7px;
    transition: transform 0.15s ease, box-shadow 0.15s ease;
  }
  .chip:hover { transform: translateY(-2px); box-shadow: 0 6px 16px rgba(0,0,0,0.35); }

  /* chip colors matched to your badges */
  .c-python   { background: #3776AB; }
  .c-sql      { background: #4479A1; }
  .c-pyspark  { background: #E25A1C; }
  .c-powerbi  { background: #F2C811; color: #1a1a1a; }
  .c-tableau  { background: #E97627; }
  .c-ssis     { background: #A4262C; }
  .c-dbt      { background: #FF694B; }
  .c-gcloud   { background: #4285F4; }
  .c-bigquery { background: #669DF6; }
  .c-azure    { background: #0078D4; }
  .c-snowflake{ background: #29B5E8; }
  .c-git      { background: #F05032; }

  /* Highlights */
  .grid { display: grid; grid-template-columns: 1fr 1fr; gap: 18px; }

  .card {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 26px;
    transition: border-color 0.2s ease;
  }
  .card:hover { border-color: var(--line); }

  .card .num {
    font-family: 'JetBrains Mono', monospace;
    font-size: 13px;
    color: var(--accent);
    margin-bottom: 12px;
    display: block;
  }
  .card h3 {
    font-family: 'Space Grotesk', sans-serif;
    font-size: 19px;
    font-weight: 600;
    margin-bottom: 8px;
  }
  .card p { color: var(--muted); font-size: 15px; }

  /* Goals list */
  .goals { list-style: none; }
  .goals li {
    padding: 14px 0;
    border-bottom: 1px solid var(--border);
    color: var(--muted);
    display: flex;
    gap: 14px;
    align-items: baseline;
  }
  .goals li:last-child { border-bottom: none; }
  .goals .idx {
    font-family: 'JetBrains Mono', monospace;
    font-size: 13px;
    color: var(--accent-warm);
    min-width: 28px;
  }

  /* Connect */
  .links { display: flex; flex-wrap: wrap; gap: 14px; margin-top: 8px; }
  .link {
    font-family: 'JetBrains Mono', monospace;
    font-size: 14px;
    color: var(--text);
    text-decoration: none;
    padding: 12px 20px;
    border: 1px solid var(--border);
    border-radius: 8px;
    transition: all 0.18s ease;
  }
  .link:hover { border-color: var(--accent); color: var(--accent); }
  .link:focus-visible { outline: 2px solid var(--accent); outline-offset: 3px; }

  footer {
    padding: 44px 0 64px;
    text-align: center;
    color: var(--muted);
    font-family: 'JetBrains Mono', monospace;
    font-size: 14px;
  }

  @media (max-width: 600px) {
    .grid { grid-template-columns: 1fr; }
    header { padding: 64px 0 48px; }
    section { padding: 48px 0; }
  }

  @media (prefers-reduced-motion: reduce) {
    * { transition: none !important; scroll-behavior: auto; }
  }
</style>
</head>
<body>

<header>
  <div class="wrap">
    <span class="tag">// data analyst · business intelligence</span>
    <h1>Supraja Kanathala</h1>
    <p class="role">Turning data into decisions, and <span class="hl">learning to make machines learn.</span></p>
    <p class="location">📍 Waterloo, Ontario, Canada</p>
  </div>
</header>

<section id="about">
  <div class="wrap">
    <p class="eyebrow">About</p>
    <h2>What I do</h2>
    <p class="lede">I have around five years of analytics experience across <strong>retail</strong> and <strong>pharmaceutical</strong> domains. I build reporting pipelines, dashboards, and models that cut through noise and get teams to answers faster. I'm now extending that foundation toward machine learning and AI engineering.</p>
  </div>
</section>

<section id="stack">
  <div class="wrap">
    <p class="eyebrow">Tech Stack</p>
    <h2>Tools I work with</h2>

    <div class="stack-group">
      <p class="stack-label">Programming &amp; Querying</p>
      <div class="chips">
        <span class="chip c-python">Python</span>
        <span class="chip c-sql">SQL</span>
        <span class="chip c-pyspark">PySpark</span>
      </div>
    </div>

    <div class="stack-group">
      <p class="stack-label">Data Analysis &amp; Visualization</p>
      <div class="chips">
        <span class="chip c-powerbi">Power BI</span>
        <span class="chip c-tableau">Tableau</span>
      </div>
    </div>

    <div class="stack-group">
      <p class="stack-label">Tools &amp; Environment</p>
      <div class="chips">
        <span class="chip c-ssis">SSIS</span>
        <span class="chip c-dbt">dbt</span>
        <span class="chip c-gcloud">Google Cloud</span>
        <span class="chip c-bigquery">BigQuery</span>
        <span class="chip c-azure">Azure</span>
        <span class="chip c-snowflake">Snowflake</span>
        <span class="chip c-git">Git</span>
      </div>
    </div>
  </div>
</section>

<section id="work">
  <div class="wrap">
    <p class="eyebrow">Highlights</p>
    <h2>Work that moved the needle</h2>
    <div class="grid">
      <div class="card">
        <span class="num">01 / retail</span>
        <h3>Seasonal demand forecasting</h3>
        <p>Built forecasting analysis at Kal Tire to anticipate seasonal demand and support smarter inventory planning.</p>
      </div>
      <div class="card">
        <span class="num">02 / pharma</span>
        <h3>Faster reporting cycle</h3>
        <p>Reduced a multi-day reporting cycle to under one day at Ranbaxy Pharma (now Sun Pharma) by streamlining the data flow.</p>
      </div>
    </div>
  </div>
</section>

<section id="goals">
  <div class="wrap">
    <p class="eyebrow">2026</p>
    <h2>What I'm focused on</h2>
    <ul class="goals">
      <li><span class="idx">01</span><span>Build hands-on data and ML projects with real business value</span></li>
      <li><span class="idx">02</span><span>Strengthen my Python and SQL foundations</span></li>
      <li><span class="idx">03</span><span>Ship interactive dashboards that tell a clear story</span></li>
      <li><span class="idx">04</span><span>Grow into an AI/ML engineering role</span></li>
    </ul>
  </div>
</section>

<section id="connect">
  <div class="wrap">
    <p class="eyebrow">Connect</p>
    <h2>Let's talk</h2>
    <div class="links">
      <a class="link" href="https://www.linkedin.com/in/suprajakanathala" target="_blank" rel="noopener">LinkedIn ↗</a>
      <a class="link" href="https://github.com/YOUR_USERNAME" target="_blank" rel="noopener">GitHub ↗</a>
      <a class="link" href="mailto:your-email@example.com">Email ↗</a>
    </div>
  </div>
</section>

<footer>
  <div class="wrap">
    "Learning, building, and growing one project at a time."
  </div>
</footer>

</body>
</html>
