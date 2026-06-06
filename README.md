<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>WHOOP 4.0 — UGC Ad Content Pack</title>
<link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=DM+Sans:ital,wght@0,300;0,400;0,600;1,300&family=JetBrains+Mono:wght@400;700&display=swap" rel="stylesheet">
<style>
  :root {
    --black: #080808;
    --white: #f5f5f0;
    --red: #ff2d2d;
    --red-dim: #8b1a1a;
    --gray: #1a1a1a;
    --gray2: #2a2a2a;
    --muted: #666;
    --accent: #c8f135;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    background: var(--black);
    color: var(--white);
    font-family: 'DM Sans', sans-serif;
    font-size: 15px;
    line-height: 1.6;
  }

  /* HEADER */
  header {
    border-bottom: 1px solid #222;
    padding: 40px 48px 32px;
    display: flex;
    justify-content: space-between;
    align-items: flex-end;
    gap: 24px;
    flex-wrap: wrap;
  }

  .brand-label {
    font-family: 'JetBrains Mono', monospace;
    font-size: 11px;
    color: var(--red);
    letter-spacing: 3px;
    text-transform: uppercase;
    margin-bottom: 8px;
  }

  header h1 {
    font-family: 'Bebas Neue', sans-serif;
    font-size: clamp(48px, 8vw, 96px);
    line-height: 0.9;
    letter-spacing: 2px;
    color: var(--white);
  }

  header h1 span { color: var(--red); }

  .meta-box {
    background: var(--gray);
    border: 1px solid #333;
    padding: 20px 24px;
    min-width: 220px;
  }

  .meta-row {
    display: flex;
    justify-content: space-between;
    gap: 32px;
    margin-bottom: 8px;
  }

  .meta-row:last-child { margin-bottom: 0; }

  .meta-key {
    font-family: 'JetBrains Mono', monospace;
    font-size: 10px;
    color: var(--muted);
    letter-spacing: 2px;
    text-transform: uppercase;
  }

  .meta-val {
    font-size: 13px;
    font-weight: 600;
    color: var(--accent);
  }

  /* MAIN */
  main {
    max-width: 1100px;
    margin: 0 auto;
    padding: 48px 48px 80px;
  }

  /* SECTION HEADER */
  .section-label {
    display: flex;
    align-items: center;
    gap: 16px;
    margin-bottom: 32px;
    margin-top: 64px;
  }

  .section-label:first-child { margin-top: 0; }

  .section-num {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 64px;
    color: var(--red-dim);
    line-height: 1;
    opacity: 0.5;
  }

  .section-title {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 28px;
    letter-spacing: 3px;
    color: var(--white);
    text-transform: uppercase;
  }

  .section-sub {
    font-size: 13px;
    color: var(--muted);
    margin-top: 2px;
    font-style: italic;
  }

  /* PRODUCT BRIEF */
  .brief-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 2px;
    background: #222;
    border: 1px solid #222;
  }

  .brief-cell {
    background: var(--black);
    padding: 20px 24px;
  }

  .brief-cell h4 {
    font-family: 'JetBrains Mono', monospace;
    font-size: 10px;
    letter-spacing: 2px;
    color: var(--red);
    text-transform: uppercase;
    margin-bottom: 8px;
  }

  .brief-cell p, .brief-cell li {
    font-size: 14px;
    color: #ccc;
    line-height: 1.7;
  }

  .brief-cell ul { padding-left: 16px; }

  /* PROMPT SYSTEM */
  .prompt-card {
    background: var(--gray);
    border: 1px solid #2a2a2a;
    border-left: 3px solid var(--red);
    margin-bottom: 16px;
    overflow: hidden;
  }

  .prompt-head {
    padding: 16px 24px;
    background: #111;
    display: flex;
    justify-content: space-between;
    align-items: center;
    border-bottom: 1px solid #2a2a2a;
  }

  .prompt-name {
    font-family: 'JetBrains Mono', monospace;
    font-size: 12px;
    letter-spacing: 1px;
    color: var(--accent);
  }

  .prompt-tag {
    font-size: 11px;
    background: #1e1e1e;
    border: 1px solid #333;
    color: var(--muted);
    padding: 3px 10px;
    border-radius: 2px;
    font-family: 'JetBrains Mono', monospace;
  }

  .prompt-body {
    padding: 20px 24px;
    font-family: 'JetBrains Mono', monospace;
    font-size: 13px;
    line-height: 1.8;
    color: #bbb;
    white-space: pre-wrap;
  }

  .prompt-body .var { color: var(--accent); }
  .prompt-body .inst { color: #888; font-style: italic; }

  /* HOOKS */
  .hooks-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 16px;
  }

  .hook-card {
    border: 1px solid #2a2a2a;
    padding: 24px;
    position: relative;
    background: var(--gray);
  }

  .hook-num {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 48px;
    color: var(--red);
    opacity: 0.15;
    position: absolute;
    top: 12px;
    right: 16px;
    line-height: 1;
  }

  .hook-type {
    font-family: 'JetBrains Mono', monospace;
    font-size: 10px;
    letter-spacing: 2px;
    color: var(--red);
    text-transform: uppercase;
    margin-bottom: 12px;
  }

  .hook-text {
    font-size: 16px;
    font-weight: 600;
    color: var(--white);
    line-height: 1.5;
    margin-bottom: 10px;
  }

  .hook-why {
    font-size: 12px;
    color: var(--muted);
    font-style: italic;
  }

  /* AD SCRIPTS */
  .script-card {
    border: 1px solid #2a2a2a;
    margin-bottom: 24px;
    background: var(--gray);
  }

  .script-header {
    background: #0f0f0f;
    padding: 16px 24px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    border-bottom: 1px solid #2a2a2a;
    flex-wrap: wrap;
    gap: 8px;
  }

  .script-title {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 20px;
    letter-spacing: 2px;
    color: var(--white);
  }

  .tags { display: flex; gap: 8px; flex-wrap: wrap; }

  .tag {
    font-size: 10px;
    font-family: 'JetBrains Mono', monospace;
    padding: 4px 10px;
    border-radius: 2px;
    letter-spacing: 1px;
  }

  .tag-platform { background: #1a2a1a; color: #7dd87d; border: 1px solid #2a3a2a; }
  .tag-duration { background: #1a1a2a; color: #7d7ddd; border: 1px solid #2a2a3a; }
  .tag-tone { background: #2a1a1a; color: var(--red); border: 1px solid #3a2a2a; }

  .script-body { padding: 24px; }

  .script-section { margin-bottom: 20px; }
  .script-section:last-child { margin-bottom: 0; }

  .script-section-label {
    font-family: 'JetBrains Mono', monospace;
    font-size: 10px;
    letter-spacing: 2px;
    color: var(--muted);
    text-transform: uppercase;
    margin-bottom: 8px;
    display: flex;
    align-items: center;
    gap: 8px;
  }

  .script-section-label::after {
    content: '';
    flex: 1;
    height: 1px;
    background: #2a2a2a;
  }

  .script-text {
    font-size: 15px;
    color: #ddd;
    line-height: 1.8;
  }

  .hook-highlight {
    color: var(--accent);
    font-weight: 600;
  }

  .cta-box {
    background: var(--red);
    color: var(--white);
    padding: 12px 20px;
    font-weight: 600;
    font-size: 14px;
    display: inline-block;
    margin-top: 4px;
  }

  /* PLATFORM TABLE */
  table {
    width: 100%;
    border-collapse: collapse;
    margin-top: 8px;
  }

  th {
    font-family: 'JetBrains Mono', monospace;
    font-size: 10px;
    letter-spacing: 2px;
    color: var(--muted);
    text-transform: uppercase;
    text-align: left;
    padding: 12px 16px;
    border-bottom: 1px solid #2a2a2a;
    background: #111;
  }

  td {
    padding: 14px 16px;
    font-size: 14px;
    color: #ccc;
    border-bottom: 1px solid #1a1a1a;
    vertical-align: top;
  }

  tr:last-child td { border-bottom: none; }
  tr:nth-child(even) td { background: #0f0f0f; }

  td:first-child {
    font-family: 'JetBrains Mono', monospace;
    font-size: 12px;
    color: var(--accent);
    white-space: nowrap;
  }

  /* GITHUB README SECTION */
  .readme-block {
    background: #0d1117;
    border: 1px solid #30363d;
    padding: 28px 32px;
    font-family: 'JetBrains Mono', monospace;
    font-size: 13px;
    line-height: 1.9;
    color: #c9d1d9;
    white-space: pre-wrap;
  }

  .readme-block .md-h1 { color: #79c0ff; font-size: 16px; font-weight: 700; }
  .readme-block .md-h2 { color: #79c0ff; }
  .readme-block .md-h3 { color: #d2a8ff; }
  .readme-block .md-bold { color: #ffa657; }
  .readme-block .md-code { color: #7ee787; background: #161b22; padding: 1px 6px; border-radius: 3px; }

  /* DIVIDER */
  .divider {
    height: 1px;
    background: linear-gradient(90deg, var(--red) 0%, transparent 60%);
    margin: 48px 0;
  }

  /* FOOTER */
  footer {
    border-top: 1px solid #222;
    padding: 24px 48px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: 12px;
  }

  footer p {
    font-family: 'JetBrains Mono', monospace;
    font-size: 11px;
    color: var(--muted);
    letter-spacing: 1px;
  }

  .footer-logo {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 20px;
    color: var(--red);
    letter-spacing: 3px;
  }

  @media (max-width: 640px) {
    header, main, footer { padding-left: 24px; padding-right: 24px; }
    .brief-grid, .hooks-grid { grid-template-columns: 1fr; }
    header { flex-direction: column; align-items: flex-start; }
  }
</style>
</head>
<body>

<header>
  <div>
    <div class="brand-label">Task 2 — Prompt Engineering // UGC Ad Pack</div>
    <h1>WHOOP<span>4.0</span><br>AD PACK</h1>
  </div>
  <div class="meta-box">
    <div class="meta-row">
      <span class="meta-key">Product</span>
      <span class="meta-val">WHOOP 4.0</span>
    </div>
    <div class="meta-row">
      <span class="meta-key">Category</span>
      <span class="meta-val">Fitness Tech</span>
    </div>
    <div class="meta-row">
      <span class="meta-key">Hooks</span>
      <span class="meta-val">5 Variants</span>
    </div>
    <div class="meta-row">
      <span class="meta-key">Scripts</span>
      <span class="meta-val">3 Full Scripts</span>
    </div>
    <div class="meta-row">
      <span class="meta-key">Platforms</span>
      <span class="meta-val">IG / YT / TT</span>
    </div>
  </div>
</header>

<main>

  <!-- PRODUCT BRIEF -->
  <div class="section-label">
    <div class="section-num">01</div>
    <div>
      <div class="section-title">Product Brief</div>
      <div class="section-sub">Know the product before writing a single word</div>
    </div>
  </div>

  <div class="brief-grid">
    <div class="brief-cell">
      <h4>Product</h4>
      <p>WHOOP 4.0 — screenless wearable health tracker worn on the wrist or bicep</p>
    </div>
    <div class="brief-cell">
      <h4>Price / Model</h4>
      <p>$0 device + $30/month membership. No screen, no distractions — data on app only</p>
    </div>
    <div class="brief-cell">
      <h4>Core Problem It Solves</h4>
      <ul>
        <li>You train hard but feel exhausted anyway</li>
        <li>You sleep 8 hrs but still wake up drained</li>
        <li>You don't know when to push vs. rest</li>
        <li>Overtraining leads to injury & burnout</li>
      </ul>
    </div>
    <div class="brief-cell">
      <h4>Key Features</h4>
      <ul>
        <li>Daily Recovery Score (0–100%)</li>
        <li>HRV & resting heart rate tracking</li>
        <li>Sleep performance & debt tracking</li>
        <li>Strain Coach for workouts</li>
        <li>5-day battery, waterproof</li>
      </ul>
    </div>
    <div class="brief-cell">
      <h4>Target Audience</h4>
      <ul>
        <li>Gym-goers 22–40</li>
        <li>Athletes & sports enthusiasts</li>
        <li>Biohackers & health optimizers</li>
        <li>Busy professionals losing sleep to stress</li>
      </ul>
    </div>
    <div class="brief-cell">
      <h4>Emotional Outcome</h4>
      <p>Feel in control of your body. Stop guessing. Know exactly what your body can handle — and perform at your best, every single day.</p>
    </div>
  </div>

  <div class="divider"></div>

  <!-- MASTER PROMPT -->
  <div class="section-label">
    <div class="section-num">02</div>
    <div>
      <div class="section-title">Master Prompt System</div>
      <div class="section-sub">Reusable prompt — swap variables for any brand</div>
    </div>
  </div>

  <div class="prompt-card">
    <div class="prompt-head">
      <span class="prompt-name">PROMPT_01 — Hook Generator</span>
      <span class="prompt-tag">reusable</span>
    </div>
    <div class="prompt-body">You are a UGC ad scriptwriter for D2C brands. Generate <span class="var">[NUMBER]</span> short, attention-grabbing hooks for a <span class="var">[PLATFORM]</span> ad promoting <span class="var">[PRODUCT NAME]</span>.

Product: <span class="var">[PRODUCT NAME]</span>
Core Problem: <span class="var">[MAIN PAIN POINT]</span>
Target Audience: <span class="var">[AUDIENCE DESCRIPTION]</span>
Tone: <span class="var">[authentic / relatable / urgent / curiosity-driven]</span>

Rules:
- Each hook must be under 8 seconds when spoken aloud
- Sound like a real person talking, NOT a brand
- No salesy language or buzzwords
- Use one of these hook styles per variant:
  • Pain-point opener ("I used to...")
  • Shocking stat or claim ("Did you know...")
  • Controversial take ("Nobody talks about...")
  • Direct question to viewer ("Are you actually recovering?")
  • Transformation tease ("I went from... to...")

Output format: numbered list, hook text only, no explanations.</div>
  </div>

  <div class="prompt-card">
    <div class="prompt-head">
      <span class="prompt-name">PROMPT_02 — Full Ad Script Generator</span>
      <span class="prompt-tag">reusable</span>
    </div>
    <div class="prompt-body">You are a UGC content creator writing a short ad script. Write a <span class="var">[DURATION]</span>-second script for <span class="var">[PLATFORM]</span> promoting <span class="var">[PRODUCT NAME]</span>.

Use this structure:
1. HOOK (0–3 sec): <span class="var">[CHOSEN HOOK]</span>
2. PROBLEM (3–10 sec): Describe the pain point personally and specifically
3. DISCOVERY (10–20 sec): How you found the product (natural, not forced)
4. SOLUTION (20–35 sec): What the product does, using simple language
5. PROOF (35–45 sec): One specific result or stat
6. CTA (45–[END] sec): Clear, low-friction call to action

Tone rules:
- First person ("I", "me", "my")
- Conversational, casual — like texting a friend
- No corporate speak, no "game-changer", no "revolutionary"
- Platform: <span class="var">[PLATFORM]</span> — adjust energy accordingly

Product details: <span class="var">[PASTE PRODUCT BRIEF]</span></div>
  </div>

  <div class="prompt-card">
    <div class="prompt-head">
      <span class="prompt-name">PROMPT_03 — Platform Adapter</span>
      <span class="prompt-tag">reusable</span>
    </div>
    <div class="prompt-body">Take this UGC ad script and rewrite it for <span class="var">[TARGET PLATFORM]</span>.

Original script: <span class="var">[PASTE SCRIPT]</span>

Platform-specific rules for <span class="var">[TARGET PLATFORM]</span>:
- Instagram Reels: Snappy, hook in first 1 sec, trending audio vibe, 15–30 sec
- YouTube Shorts: Slightly longer context ok, punchline delivery, 30–45 sec
- TikTok: Most casual, trending formats ok, jump cuts assumed, 15–25 sec
- Facebook Ads: Slightly more explanation, older audience, 30–60 sec

Keep the core message identical. Change only: pacing, energy, slang level, and CTA wording.
Output: full rewritten script only.</div>
  </div>

  <div class="divider"></div>

  <!-- HOOKS -->
  <div class="section-label">
    <div class="section-num">03</div>
    <div>
      <div class="section-title">Generated Hooks</div>
      <div class="section-sub">5 hooks for WHOOP 4.0 — each a different angle</div>
    </div>
  </div>

  <div class="hooks-grid">
    <div class="hook-card">
      <div class="hook-num">01</div>
      <div class="hook-type">Pain-Point Opener</div>
      <div class="hook-text">"I was working out 6 days a week and somehow getting weaker."</div>
      <div class="hook-why">Triggers identity crisis in gym-goers. Highly relatable.</div>
    </div>
    <div class="hook-card">
      <div class="hook-num">02</div>
      <div class="hook-type">Shocking Claim</div>
      <div class="hook-text">"Your 8 hours of sleep might actually be destroying your recovery."</div>
      <div class="hook-why">Challenges a common belief — forces the viewer to keep watching.</div>
    </div>
    <div class="hook-card">
      <div class="hook-num">03</div>
      <div class="hook-type">Controversial Take</div>
      <div class="hook-text">"Nobody tells you that training harder is the reason you're not progressing."</div>
      <div class="hook-why">Contrarian angle — appeals to frustrated gym-goers.</div>
    </div>
    <div class="hook-card">
      <div class="hook-num">04</div>
      <div class="hook-type">Direct Question</div>
      <div class="hook-text">"What if your body is literally telling you to rest — and you're not listening?"</div>
      <div class="hook-why">Creates self-reflection. Viewer feels seen.</div>
    </div>
    <div class="hook-card" style="grid-column: 1 / -1;">
      <div class="hook-num">05</div>
      <div class="hook-type">Transformation Tease</div>
      <div class="hook-text">"I went from waking up exhausted every day to knowing exactly how much my body can handle — this is what changed it."</div>
      <div class="hook-why">Classic before/after format. Strong curiosity gap drives watch time.</div>
    </div>
  </div>

  <div class="divider"></div>

  <!-- AD SCRIPTS -->
  <div class="section-label">
    <div class="section-num">04</div>
    <div>
      <div class="section-title">Full Ad Scripts</div>
      <div class="section-sub">3 complete scripts — problem → solution → CTA</div>
    </div>
  </div>

  <!-- Script 1 -->
  <div class="script-card">
    <div class="script-header">
      <div class="script-title">Script 01 — The Overtrainer</div>
      <div class="tags">
        <span class="tag tag-platform">Instagram Reels</span>
        <span class="tag tag-duration">30 sec</span>
        <span class="tag tag-tone">Relatable</span>
      </div>
    </div>
    <div class="script-body">
      <div class="script-section">
        <div class="script-section-label">Hook (0–3s)</div>
        <div class="script-text"><span class="hook-highlight">"I was working out 6 days a week and somehow getting weaker."</span></div>
      </div>
      <div class="script-section">
        <div class="script-section-label">Problem (3–10s)</div>
        <div class="script-text">I was tired all the time. I thought I just needed to push harder. More volume, more intensity — nothing was working. I didn't realize I was literally destroying my body faster than it could recover.</div>
      </div>
      <div class="script-section">
        <div class="script-section-label">Discovery (10–18s)</div>
        <div class="script-text">Then my friend showed me his WHOOP data. His recovery score that morning was 22% — and he skipped the gym because of it. I thought that was insane. But it got me curious.</div>
      </div>
      <div class="script-section">
        <div class="script-section-label">Solution (18–27s)</div>
        <div class="script-text">WHOOP tracks your HRV, sleep quality, and strain every single day. It gives you a recovery score — basically tells you exactly how much your body can handle today. Green means push. Red means recover.</div>
      </div>
      <div class="script-section">
        <div class="script-section-label">CTA (27–30s)</div>
        <div class="script-text"><div class="cta-box">Link in bio — first month free. Try it.</div></div>
      </div>
    </div>
  </div>

  <!-- Script 2 -->
  <div class="script-card">
    <div class="script-header">
      <div class="script-title">Script 02 — The Bad Sleeper</div>
      <div class="tags">
        <span class="tag tag-platform">YouTube Shorts</span>
        <span class="tag tag-duration">45 sec</span>
        <span class="tag tag-tone">Personal Story</span>
      </div>
    </div>
    <div class="script-body">
      <div class="script-section">
        <div class="script-section-label">Hook (0–3s)</div>
        <div class="script-text"><span class="hook-highlight">"Your 8 hours of sleep might actually be destroying your recovery."</span></div>
      </div>
      <div class="script-section">
        <div class="script-section-label">Problem (3–12s)</div>
        <div class="script-text">I was sleeping a solid 8 hours every night and still waking up feeling like garbage. Dragging myself to the gym, no energy in my workouts. I just assumed I was getting old at 27. That's wild, right?</div>
      </div>
      <div class="script-section">
        <div class="script-section-label">Discovery + Solution (12–35s)</div>
        <div class="script-text">I started tracking with WHOOP and found out my sleep efficiency was like 68%. I was spending 8 hours in bed but only actually getting quality sleep for 5. It also showed my HRV was tanking — meaning my nervous system was constantly stressed. Once I saw the data, I made tiny changes — no alcohol 3 hours before bed, earlier dinner — and my recovery scores went from 40% to consistently hitting 80%+.</div>
      </div>
      <div class="script-section">
        <div class="script-section-label">Proof (35–42s)</div>
        <div class="script-text">In 6 weeks, my gym performance went up noticeably. Not because I trained more — because I finally understood when to rest.</div>
      </div>
      <div class="script-section">
        <div class="script-section-label">CTA (42–45s)</div>
        <div class="script-text"><div class="cta-box">Check the link below. The first month is free — no excuses.</div></div>
      </div>
    </div>
  </div>

  <!-- Script 3 -->
  <div class="script-card">
    <div class="script-header">
      <div class="script-title">Script 03 — The Biohacker</div>
      <div class="tags">
        <span class="tag tag-platform">TikTok</span>
        <span class="tag tag-duration">20 sec</span>
        <span class="tag tag-tone">Curiosity / Data</span>
      </div>
    </div>
    <div class="script-body">
      <div class="script-section">
        <div class="script-section-label">Hook (0–3s)</div>
        <div class="script-text"><span class="hook-highlight">"What if your body is literally telling you to rest — and you're not listening?"</span></div>
      </div>
      <div class="script-section">
        <div class="script-section-label">Core (3–15s)</div>
        <div class="script-text">WHOOP reads your HRV every morning and gives you a recovery score out of 100. The lower it is, the harder your body is working just to exist. I used to ignore rest days — now I take them based on data, not guilt. And I've had zero injuries this year.</div>
      </div>
      <div class="script-section">
        <div class="script-section-label">CTA (15–20s)</div>
        <div class="script-text"><div class="cta-box">Link in bio. First month on them.</div></div>
      </div>
    </div>
  </div>

  <div class="divider"></div>

  <!-- PLATFORM GUIDE -->
  <div class="section-label">
    <div class="section-num">05</div>
    <div>
      <div class="section-title">Platform Adaptation Guide</div>
      <div class="section-sub">Same message, different energy per platform</div>
    </div>
  </div>

  <table>
    <thead>
      <tr>
        <th>Platform</th>
        <th>Duration</th>
        <th>Tone</th>
        <th>Hook Speed</th>
        <th>CTA Style</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>Instagram Reels</td>
        <td>15–30 sec</td>
        <td>Aspirational, clean</td>
        <td>Under 1 second</td>
        <td>"Link in bio"</td>
      </tr>
      <tr>
        <td>TikTok</td>
        <td>15–25 sec</td>
        <td>Raw, casual, trend-aware</td>
        <td>Instant — first word</td>
        <td>"Check it out rn"</td>
      </tr>
      <tr>
        <td>YouTube Shorts</td>
        <td>30–55 sec</td>
        <td>Storytelling, more detail ok</td>
        <td>Under 3 seconds</td>
        <td>"Link below"</td>
      </tr>
      <tr>
        <td>Facebook Ads</td>
        <td>30–60 sec</td>
        <td>Slightly more formal, educational</td>
        <td>Under 5 seconds</td>
        <td>"Click the link to learn more"</td>
      </tr>
    </tbody>
  </table>

  <div class="divider"></div>

  <!-- README -->
  <div class="section-label">
    <div class="section-num">06</div>
    <div>
      <div class="section-title">GitHub README</div>
      <div class="section-sub">Copy this into your repo's README.md</div>
    </div>
  </div>

  <div class="readme-block"><span class="md-h1"># WHOOP 4.0 — UGC Ad Content Pack</span>
<span class="md-h3">Built for: Future Interns Task 2 — Prompt Engineering</span>

---

<span class="md-h2">## Overview</span>

This repo contains a reusable AI prompt system for generating
UGC-style ad scripts. Built around WHOOP 4.0 fitness tracker,
but the prompt templates work for any D2C product or brand.

<span class="md-h2">## Folder Structure</span>

<span class="md-code">prompts/</span>        → 3 master prompt templates (hook, script, platform adapter)
<span class="md-code">outputs/</span>        → 5 hooks + 3 full ad scripts (generated)
<span class="md-code">docs/</span>           → Platform guide + product brief

<span class="md-h2">## How to Use the Prompts</span>

1. Open <span class="md-code">prompts/hook-generator.txt</span>
2. Replace all <span class="md-bold">[VARIABLE]</span> fields with your product info
3. Paste into Claude / ChatGPT / Gemini
4. Generate 5+ hooks, pick the best 2–3
5. Run <span class="md-code">prompts/script-generator.txt</span> with chosen hook
6. Adapt for platforms using <span class="md-code">prompts/platform-adapter.txt</span>

<span class="md-h2">## Key Features of This System</span>

✓ Authentic UGC tone (not salesy)
✓ Problem → Solution → CTA framework
✓ Platform-specific outputs
✓ Fully reusable for any brand
✓ Multiple hook angles per product

<span class="md-h2">## Product Chosen</span>

<span class="md-bold">WHOOP 4.0</span> — Fitness recovery tracker
Target audience: gym-goers, athletes, biohackers
Core problem solved: overtraining, poor recovery, sleep inefficiency</div>

</main>

<footer>
  <p>UGC AD CONTENT PACK — WHOOP 4.0 // TASK 2 PROMPT ENGINEERING</p>
  <div class="footer-logo">FUTURE INTERNS</div>
</footer>

</body>
</html>
