<title>Draaimolen Planner</title>
<style>
  /* ---------------------------------------------------------
     Draaimolen 2026 — Interactive Timetable
     Design plan:
     Color   — near-black ground with six stage-light hues
               (magenta / periwinkle / violet / acid-green /
               amber / cyan) standing in for each stage's own
               lighting rig, plus one lime signature accent
               and a warm amber "note" reserved for overlaps —
               legible, not alarming.
     Type    — Unbounded (poster-weight display) for the
               festival wordmark and section titles, Archivo
               for UI text, JetBrains Mono for every clock
               figure so times line up like a running order.
     Layout  — a sticky-header/sticky-column schedule grid,
               time running left→right like a real stage
               plan, with a persistent "my schedule" strip
               that surfaces saves and clashes at a glance.
     --------------------------------------------------------- */

  @import url('https://fonts.googleapis.com/css2?family=Unbounded:wght@500;700;900&family=Archivo:wght@400;500;600;700&family=JetBrains+Mono:wght@400;500;700&display=swap');

  :root{
    --bg: #f3f1f6;
    --bg-grain-opacity: 0.02;
    --surface: #ffffff;
    --surface-2: #ece9f2;
    --surface-3: #e2ddec;
    --border: #d9d3e3;
    --text: #16131c;
    --text-dim: #5c5566;
    --text-faint: #948da1;

    --accent: #7a9400;
    --accent-ink: #ffffff;
    --accent-soft: #eaf2c8;

    --danger: #c22f3c;
    --danger-soft: #fbe1e2;
    --danger-ink: #ffffff;

    --note: #8a5a00;
    --note-soft: #faedd2;
    --note-ink: #5c3b00;

    --stage-strobe: #c81e73;
    --stage-moon:   #4257c9;
    --stage-aura:   #7a3fc9;
    --stage-forest: #3f8f1f;
    --stage-pit:    #b25400;
    --stage-tunnel: #0d8e8a;

    --shadow: 0 12px 32px -16px rgba(22,19,28,0.28);
    --glow-1: transparent;
    --glow-2: transparent;
  }

  @media (prefers-color-scheme: dark){
    :root:not([data-theme="light"]){
      --bg: #0a0a0d;
      --bg-grain-opacity: 0.05;
      --surface: #151319;
      --surface-2: #1c1a22;
      --surface-3: #262330;
      --border: #322e3c;
      --text: #f4f1f8;
      --text-dim: #ada5b8;
      --text-faint: #726b80;

      --accent: #d7f24a;
      --accent-ink: #14170a;
      --accent-soft: #262d0e;

      --danger: #ff5064;
      --danger-soft: #3a1620;
      --danger-ink: #1a0509;

      --note: #f2b705;
      --note-soft: #3a2d0d;
      --note-ink: #f7dfa0;

      --stage-strobe: #ff4fa3;
      --stage-moon:   #9db4ff;
      --stage-aura:   #b884ff;
      --stage-forest: #8bd450;
      --stage-pit:    #ff9f40;
      --stage-tunnel: #3ddbd9;

      --shadow: 0 20px 44px -18px rgba(0,0,0,0.65);
      --glow-1: #c81e73;
      --glow-2: #0d8e8a;
    }
  }

  :root[data-theme="dark"]{
    --bg: #0a0a0d;
    --bg-grain-opacity: 0.05;
    --surface: #151319;
    --surface-2: #1c1a22;
    --surface-3: #262330;
    --border: #322e3c;
    --text: #f4f1f8;
    --text-dim: #ada5b8;
    --text-faint: #726b80;

    --accent: #d7f24a;
    --accent-ink: #14170a;
    --accent-soft: #262d0e;

    --danger: #ff5064;
    --danger-soft: #3a1620;
    --danger-ink: #1a0509;

    --note: #f2b705;
    --note-soft: #3a2d0d;
    --note-ink: #f7dfa0;

    --stage-strobe: #ff4fa3;
    --stage-moon:   #9db4ff;
    --stage-aura:   #b884ff;
    --stage-forest: #8bd450;
    --stage-pit:    #ff9f40;
    --stage-tunnel: #3ddbd9;

    --shadow: 0 20px 44px -18px rgba(0,0,0,0.65);
    --glow-1: #c81e73;
    --glow-2: #0d8e8a;
  }

  *{ box-sizing: border-box; }
  html{ color-scheme: light dark; }

  body{
    margin: 0;
    background: var(--bg);
    color: var(--text);
    font-family: 'Archivo', -apple-system, BlinkMacSystemFont, sans-serif;
    position: relative;
    min-height: 100%;
  }

  body::before{
    content: "";
    position: fixed;
    inset: 0;
    pointer-events: none;
    z-index: 0;
    opacity: var(--bg-grain-opacity);
    background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='120' height='120'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.85' numOctaves='2' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)'/%3E%3C/svg%3E");
  }

  body::after{
    content: "";
    position: fixed;
    inset: -10% -10% auto -10%;
    height: 60vh;
    pointer-events: none;
    z-index: 0;
    background:
      radial-gradient(38rem 20rem at 12% 0%, color-mix(in srgb, var(--glow-1) 16%, transparent), transparent 70%),
      radial-gradient(34rem 18rem at 88% 8%, color-mix(in srgb, var(--glow-2) 14%, transparent), transparent 70%);
  }

  h1, h2, h3{ font-family: 'Unbounded', 'Archivo', sans-serif; text-wrap: balance; margin: 0; }

  .mono{ font-family: 'JetBrains Mono', ui-monospace, monospace; font-variant-numeric: tabular-nums; }

  .wrap{
    position: relative;
    z-index: 1;
    max-width: 78rem;
    margin: 0 auto;
    padding: 2.25rem 1.5rem 4rem;
  }

  /* ---------- header ---------- */
  header.top{
    display: flex;
    flex-wrap: wrap;
    align-items: flex-end;
    justify-content: space-between;
    gap: 1.5rem 2rem;
    margin-bottom: 1.75rem;
  }
  .brand-eyebrow{
    display: inline-flex;
    align-items: center;
    gap: .5rem;
    font-family: 'JetBrains Mono', monospace;
    font-size: .7rem;
    letter-spacing: .14em;
    text-transform: uppercase;
    color: var(--text-faint);
    margin-bottom: .6rem;
  }
  .brand-eyebrow .dot{
    width: .5rem; height: .5rem; border-radius: 50%;
    background: var(--accent);
    box-shadow: 0 0 0 3px color-mix(in srgb, var(--accent) 25%, transparent);
  }
  h1.title{
    font-size: clamp(1.9rem, 4.4vw, 3rem);
    font-weight: 900;
    letter-spacing: .01em;
    line-height: .98;
  }
  h1.title em{
    font-style: normal;
    color: var(--accent);
  }
  .subtitle{
    max-width: 34rem;
    color: var(--text-dim);
    font-size: .97rem;
    line-height: 1.55;
    margin-top: .6rem;
  }

  .day-switch{
    display: inline-flex;
    padding: .3rem;
    background: var(--surface-2);
    border: 1px solid var(--border);
    border-radius: 999px;
    gap: .25rem;
    flex-shrink: 0;
  }
  .day-switch button{
    appearance: none;
    border: none;
    background: transparent;
    color: var(--text-dim);
    font-family: 'Archivo', sans-serif;
    font-weight: 700;
    font-size: .88rem;
    padding: .6rem 1.3rem;
    border-radius: 999px;
    cursor: pointer;
    transition: background .15s ease, color .15s ease;
  }
  .day-switch button .d{
    display: block;
    font-family: 'JetBrains Mono', monospace;
    font-weight: 400;
    font-size: .68rem;
    letter-spacing: .06em;
    color: var(--text-faint);
    margin-top: .1rem;
  }
  .day-switch button[aria-pressed="true"]{
    background: var(--text);
    color: var(--bg);
  }
  .day-switch button[aria-pressed="true"] .d{ color: color-mix(in srgb, var(--bg) 55%, var(--text-dim)); }
  .day-switch button:focus-visible{ outline: 2px solid var(--accent); outline-offset: 2px; }

  /* ---------- legend ---------- */
  .legend{
    display: flex;
    flex-wrap: wrap;
    gap: .5rem .9rem;
    margin-bottom: 1.5rem;
  }
  .legend-item{
    display: inline-flex;
    align-items: center;
    gap: .45rem;
    font-size: .74rem;
    font-weight: 600;
    letter-spacing: .03em;
    text-transform: uppercase;
    color: var(--text-dim);
  }
  .legend-swatch{
    width: .62rem; height: .62rem;
    border-radius: 3px;
    background: var(--sc);
    box-shadow: 0 0 0 1px color-mix(in srgb, var(--sc) 55%, transparent);
  }

  /* ---------- my schedule strip ---------- */
  .schedule-bar{
    position: sticky;
    top: .75rem;
    z-index: 20;
    display: flex;
    align-items: center;
    gap: 1rem;
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 1rem;
    padding: .85rem 1.1rem;
    box-shadow: var(--shadow);
    margin-bottom: 1.5rem;
  }
  .schedule-bar .stat{
    display: flex;
    align-items: baseline;
    gap: .4rem;
    font-family: 'JetBrains Mono', monospace;
  }
  .schedule-bar .stat b{ font-size: 1.35rem; color: var(--text); }
  .schedule-bar .stat span{ font-size: .72rem; color: var(--text-faint); text-transform: uppercase; letter-spacing: .08em; }
  .schedule-bar .stat.clash b{ color: var(--note); }
  .schedule-bar .sep{ width: 1px; align-self: stretch; background: var(--border); }
  .schedule-bar .hint{
    flex: 1;
    color: var(--text-dim);
    font-size: .85rem;
    min-width: 12rem;
  }
  .schedule-bar button.toggle-drawer{
    appearance: none;
    cursor: pointer;
    border: 1px solid var(--border);
    background: var(--surface-2);
    color: var(--text);
    font-family: 'Archivo', sans-serif;
    font-weight: 700;
    font-size: .82rem;
    padding: .55rem 1rem;
    border-radius: .6rem;
    display: inline-flex;
    align-items: center;
    gap: .4rem;
  }
  .schedule-bar button.toggle-drawer:hover{ background: var(--surface-3); }
  .schedule-bar button.toggle-drawer:focus-visible{ outline: 2px solid var(--accent); outline-offset: 2px; }
  .schedule-bar button.toggle-drawer svg{ transition: transform .18s ease; }
  .schedule-bar[data-open="true"] button.toggle-drawer svg{ transform: rotate(180deg); }

  .drawer{
    overflow: hidden;
    max-height: 0;
    transition: max-height .22s ease;
    margin: -0.75rem 0 1.5rem;
  }
  .drawer[data-open="true"]{ max-height: 40rem; }
  .drawer-inner{
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 1rem;
    padding: .5rem;
    display: grid;
    gap: .35rem;
  }
  .drawer-empty{
    padding: 1.6rem 1rem;
    text-align: center;
    color: var(--text-faint);
    font-size: .88rem;
  }
  .drawer-tabs{
    display: flex;
    gap: .3rem;
    padding: .3rem .3rem .5rem;
  }
  .drawer-tabs button{
    flex: 1;
    appearance: none;
    cursor: pointer;
    border: 1px solid var(--border);
    background: var(--surface-2);
    color: var(--text-dim);
    font-family: 'Archivo', sans-serif;
    font-weight: 700;
    font-size: .8rem;
    padding: .55rem .6rem;
    border-radius: .55rem;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: .4rem;
  }
  .drawer-tabs button .count{
    font-family: 'JetBrains Mono', monospace;
    font-weight: 400;
    font-size: .72rem;
    color: var(--text-faint);
    background: var(--surface);
    border-radius: 999px;
    padding: .05rem .45rem;
  }
  .drawer-tabs button[aria-pressed="true"]{
    background: var(--text);
    color: var(--bg);
    border-color: var(--text);
  }
  .drawer-tabs button[aria-pressed="true"] .count{ background: color-mix(in srgb, var(--bg) 80%, var(--text-dim)); color: var(--bg); }
  .drawer-tabs button:focus-visible{ outline: 2px solid var(--accent); outline-offset: 2px; }
  /* ---- favourites agenda: a compact, vertical timetable ---- */
  .agenda-wrap{ padding: .2rem .3rem .3rem; }
  .agenda-scroll{
    max-height: 24rem;
    overflow-y: auto;
    overflow-x: hidden;
    border: 1px solid var(--border);
    border-radius: .75rem;
    background: var(--surface-2);
  }
  .agenda{
    position: relative;
    display: grid;
    grid-template-columns: 54px 1fr;
  }
  .agenda-ruler{ position: relative; }
  .agenda-ruler .tick{
    position: absolute;
    right: .6rem;
    left: 0;
    text-align: right;
    font-family: 'JetBrains Mono', monospace;
    font-size: .64rem;
    color: var(--text-faint);
    transform: translateY(-50%);
  }
  .agenda-lanes{
    position: relative;
    border-left: 1px solid var(--border);
    background-image: repeating-linear-gradient(
      to bottom,
      color-mix(in srgb, var(--border) 60%, transparent) 0,
      color-mix(in srgb, var(--border) 60%, transparent) 1px,
      transparent 1px,
      transparent var(--hour-h)
    );
  }
  .agenda-block{
    position: absolute;
    border-radius: .55rem;
    border: 1.5px solid color-mix(in srgb, var(--sc) 55%, var(--border));
    background: color-mix(in srgb, var(--sc) 16%, var(--surface));
    padding: .4rem .6rem;
    overflow: hidden;
  }
  .agenda-block .name{
    font-weight: 700;
    font-size: .78rem;
    line-height: 1.2;
    padding-right: 1.1rem;
    display: -webkit-box;
    -webkit-line-clamp: 2;
    -webkit-box-orient: vertical;
    overflow: hidden;
  }
  .agenda-block .meta{
    display: flex;
    align-items: center;
    gap: .35rem;
    margin-top: .22rem;
    font-family: 'JetBrains Mono', monospace;
    font-size: .64rem;
    color: var(--text-dim);
    white-space: nowrap;
  }
  .agenda-block .meta .dot{ width: .42rem; height: .42rem; border-radius: 50%; background: var(--sc); flex-shrink: 0; }
  .agenda-block .same-time{
    display: inline-flex;
    align-items: center;
    gap: .25rem;
    margin-top: .3rem;
    background: var(--note-soft);
    color: var(--note-ink);
    font-size: .6rem;
    font-weight: 700;
    letter-spacing: .02em;
    text-transform: uppercase;
    padding: .14rem .45rem;
    border-radius: 999px;
    width: fit-content;
  }
  .agenda-block[data-clash="true"]{
    border-color: var(--note);
    box-shadow: 0 0 0 1.5px color-mix(in srgb, var(--note) 40%, transparent);
  }
  .agenda-block button.remove{
    position: absolute;
    top: .35rem; right: .35rem;
    width: 1.3rem; height: 1.3rem;
    border-radius: 50%;
    border: none;
    background: color-mix(in srgb, var(--surface) 55%, transparent);
    color: var(--text-faint);
    font-size: .82rem;
    line-height: 1;
    cursor: pointer;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  .agenda-block button.remove:hover{ background: var(--surface-3); color: var(--text); }

  /* ---------- timetable grid ---------- */
  .day-panel[hidden]{ display: none; }

  .tt-shell{
    border: 1px solid var(--border);
    border-radius: 1rem;
    overflow: hidden;
    box-shadow: var(--shadow);
    background: var(--surface);
  }

  .tt-scroll{
    overflow: auto;
    max-height: min(72vh, 640px);
  }

  .tt-grid{
    display: grid;
    grid-template-columns: 148px var(--track-w);
    width: max-content;
  }

  .corner{
    position: sticky;
    top: 0; left: 0;
    z-index: 5;
    background: var(--surface-2);
    border-right: 1px solid var(--border);
    border-bottom: 1px solid var(--border);
    display: flex;
    align-items: flex-end;
    padding: .5rem .8rem;
    font-family: 'JetBrains Mono', monospace;
    font-size: .65rem;
    letter-spacing: .08em;
    text-transform: uppercase;
    color: var(--text-faint);
  }

  .ruler{
    position: sticky;
    top: 0;
    z-index: 4;
    background: var(--surface-2);
    border-bottom: 1px solid var(--border);
    position: relative;
    height: 40px;
    background-image: repeating-linear-gradient(
      to right,
      color-mix(in srgb, var(--border) 70%, transparent) 0,
      color-mix(in srgb, var(--border) 70%, transparent) 1px,
      transparent 1px,
      transparent var(--hour-w)
    );
  }
  .ruler .tick{
    position: absolute;
    top: 0; bottom: 0;
    display: flex;
    align-items: center;
    padding-left: .5rem;
    font-family: 'JetBrains Mono', monospace;
    font-size: .72rem;
    color: var(--text-dim);
    white-space: nowrap;
  }

  .stage-label{
    position: sticky;
    left: 0;
    z-index: 3;
    background: var(--surface);
    border-right: 1px solid var(--border);
    border-bottom: 1px solid var(--border);
    display: flex;
    align-items: center;
    gap: .55rem;
    padding: 0 .9rem;
  }
  .stage-label .bar{ width: 4px; align-self: stretch; margin: .9rem 0; border-radius: 2px; background: var(--sc); }
  .stage-label .name{ font-weight: 700; font-size: .84rem; letter-spacing: .02em; }

  .stage-track{
    position: relative;
    border-bottom: 1px solid var(--border);
    background-image: repeating-linear-gradient(
      to right,
      color-mix(in srgb, var(--border) 45%, transparent) 0,
      color-mix(in srgb, var(--border) 45%, transparent) 1px,
      transparent 1px,
      transparent var(--hour-w)
    );
  }
  .stage-track:nth-child(4n + 2){ background-color: color-mix(in srgb, var(--surface-2) 35%, transparent); }

  .act{
    position: absolute;
    top: 8px; bottom: 8px;
    border-radius: .55rem;
    border: 1.5px solid color-mix(in srgb, var(--sc) 55%, var(--border));
    background: color-mix(in srgb, var(--sc) 15%, var(--surface));
    color: var(--text);
    padding: .5rem .6rem .45rem;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    gap: .25rem;
    cursor: pointer;
    text-align: left;
    font-family: 'Archivo', sans-serif;
    overflow: hidden;
    transition: transform .12s ease, box-shadow .12s ease, background .12s ease;
  }
  .act:hover{ transform: translateY(-2px); box-shadow: 0 8px 18px -8px rgba(0,0,0,.35); }
  .act:focus-visible{ outline: 2px solid var(--accent); outline-offset: 2px; }

  .act .name{
    font-weight: 700;
    font-size: .8rem;
    line-height: 1.2;
    display: -webkit-box;
    -webkit-line-clamp: 3;
    -webkit-box-orient: vertical;
    overflow: hidden;
  }
  .act .foot{
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: .4rem;
  }
  .act .time{
    font-family: 'JetBrains Mono', monospace;
    font-size: .68rem;
    color: var(--text-dim);
    white-space: nowrap;
  }
  .act .star{
    width: 1.15rem; height: 1.15rem;
    flex-shrink: 0;
    color: var(--text-faint);
  }
  .act .star svg{ display:block; width: 100%; height: 100%; }

  .act[data-saved="true"]{
    background: color-mix(in srgb, var(--sc) 32%, var(--surface));
    border-color: var(--sc);
    box-shadow: 0 0 0 2px color-mix(in srgb, var(--sc) 45%, transparent);
  }
  .act[data-saved="true"] .star{ color: var(--sc); }

  .act[data-clash="true"]{
    border-color: var(--note);
    border-style: dashed;
    box-shadow: 0 0 0 2px color-mix(in srgb, var(--note) 38%, transparent);
  }
  .act[data-clash="true"] .star{ color: var(--note); }

  .act .warn{
    display: none;
    align-items: center;
    gap: .25rem;
    font-size: .6rem;
    font-weight: 700;
    text-transform: uppercase;
    letter-spacing: .03em;
    color: var(--note-ink);
    background: var(--note-soft);
    padding: .12rem .4rem;
    border-radius: 999px;
    width: fit-content;
  }
  .act[data-clash="true"] .warn{ display: inline-flex; }

  footer.foot{
    margin-top: 2.5rem;
    padding-top: 1.5rem;
    border-top: 1px solid var(--border);
    display: flex;
    flex-wrap: wrap;
    gap: .5rem 1.5rem;
    justify-content: space-between;
    color: var(--text-faint);
    font-size: .78rem;
    line-height: 1.6;
  }
  footer.foot a{ color: inherit; }

  @media (max-width: 640px){
    .wrap{ padding: 1.4rem 1rem 3rem; }
    header.top{ flex-direction: column; align-items: stretch; }
    .day-switch{ align-self: flex-start; }
    .schedule-bar{ flex-wrap: wrap; top: .5rem; }
    .schedule-bar .hint{ order: 5; width: 100%; }
  }

  @media (prefers-reduced-motion: reduce){
    *{ transition: none !important; animation: none !important; }
  }
</style>

<div class="wrap">

  <header class="top">
    <div>
      <div class="brand-eyebrow"><span class="dot"></span> Draaimolen Festival · 2026</div>
      <h1 class="title">Your <em>timetable</em>,<br>overlap‑aware.</h1>
      <p class="subtitle">Tap any set across both days to save it. If two of your picks happen at the same time, they're marked automatically, so you always know at a glance.</p>
    </div>
    <div class="day-switch" role="tablist" aria-label="Festival day">
      <button type="button" data-day="0" role="tab" aria-pressed="true">Friday<span class="d">12:00 – 00:30</span></button>
      <button type="button" data-day="1" role="tab" aria-pressed="false">Saturday<span class="d">12:00 – 00:30</span></button>
    </div>
  </header>

  <div class="legend" id="legend"></div>

  <div class="schedule-bar" id="scheduleBar" data-open="false">
    <div class="stat"><b id="savedCount">0</b><span>saved</span></div>
    <div class="sep"></div>
    <div class="stat clash"><b id="clashCount">0</b><span>overlapping</span></div>
    <p class="hint" id="scheduleHint">Tap a set below to start building your weekend.</p>
    <button type="button" class="toggle-drawer" id="drawerToggle" aria-expanded="false">
      My schedule
      <svg width="12" height="8" viewBox="0 0 12 8" fill="none"><path d="M1 1.5L6 6.5L11 1.5" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg>
    </button>
  </div>

  <div class="drawer" id="drawer">
    <div class="drawer-inner" id="drawerInner"></div>
  </div>

  <div id="panels"></div>

  <footer class="foot">
    <span>Times reflect the published Friday/Saturday running order — Draaimolen can always shuffle a set on the day, so double‑check on site.</span>
    <span>Source: draaimolen.nu</span>
  </footer>

</div>

<script>
(function(){
  "use strict";

  var STAGES = [
    { name: "Strobe",       key: "strobe" },
    { name: "Moon",         key: "moon" },
    { name: "Aura",         key: "aura" },
    { name: "Forest Rave",  key: "forest" },
    { name: "The Pit",      key: "pit" },
    { name: "Tunnel",       key: "tunnel" }
  ];
  var DAYS = ["Friday", "Saturday"];

  // [day, stageIdx, artist, startMin, endMin] — startMin/endMin are minutes
  // since 00:00, with the 12:00–00:30 show day running 720 → 1470.
  var ACTS = [
    [0,0,"Lola Edo",720,870],
    [0,0,"Mi-EL b2b Soft Break",870,990],
    [0,0,"Leonce b2b Oceanic",990,1110],
    [0,0,"Namasenda (Live)",1110,1155],
    [0,0,"Angel D'lite b2b Kim Ann Foxman",1155,1290],
    [0,0,"Shygirl (Live)",1290,1350],
    [0,0,"The Secret Guest",1350,1470],

    [0,1,"The Necks (Live) — Set 1",780,855],
    [0,1,"The Necks (Live) — Set 2",885,960],
    [0,1,"Cola Ren & K-LONE (Live)",960,1020],
    [0,1,"Cosmo b2b Marie K",1020,1140],
    [0,1,"Kevin Saunderson b2b Surusinghe",1140,1260],
    [0,1,"Datapunk (Hybrid) presented by Anthony Rother",1260,1350],
    [0,1,"Carl H b2b Naone",1350,1470],

    [0,2,"Annebel b2b Carré",720,900],
    [0,2,"OJOO (Hybrid)",900,960],
    [0,2,"Dials (Live)",960,1005],
    [0,2,"Shannen SP",1005,1140],
    [0,2,"James K (Live)",1140,1200],
    [0,2,"DJ Firmeza x DJ Lycox x DJ Narciso",1200,1320],
    [0,2,"Commodo x Hans Arsen (Live)",1320,1380],
    [0,2,"RE:NI b2b Simo Cell",1380,1470],

    [0,3,"Harrison Heat",720,870],
    [0,3,"Michelle Manetti",870,960],
    [0,3,"Colored Craig",960,1050],
    [0,3,"Dimitri",1050,1140],
    [0,3,"DJ Nobu",1140,1260],
    [0,3,"Eris Drew b2b Objekt",1260,1380],
    [0,3,"Introspekt b2b Jeremy Sylvester",1380,1470],

    [0,4,"Colombian Drone Mafia & Debit (Hybrid)",720,840],
    [0,4,"Nadah El Shazly ft. 3Phaz (Live)",840,900],
    [0,4,"Kelman Duran (Live)",900,960],
    [0,4,"Wheel of Fortune (CCL x Marylou x Nono Gigsta x Rroxymore)",960,1140],
    [0,4,"Weird Baile",1140,1230],
    [0,4,"Hyperverbena (Hybrid)",1230,1290],
    [0,4,"DJRUM x Riko Dan",1290,1380],
    [0,4,"Low Jack b2b R3IGN Drops",1380,1470],

    [0,5,"Varuna Agosti",720,900],
    [0,5,"Eversines (Live)",900,960],
    [0,5,"Isabel Soto b2b Jin Synth",960,1080],
    [0,5,"Doltz. (Live)",1080,1140],
    [0,5,"Darwin b2b Mama Snake",1140,1260],
    [0,5,"The Secret Live Act",1260,1350],
    [0,5,"Talismann b2b Wallis",1350,1470],

    [1,0,"Bennet b2b Beste Hira",720,990],
    [1,0,"Deetron (Live)",990,1050],
    [1,0,"Donato Dozzy b2b Job Jobse",1050,1200],
    [1,0,"Nene H (Live)",1200,1260],
    [1,0,"DJ G2G b2b SPFDJ",1260,1350],
    [1,0,"Lena Willikens b2b ¥ØU$UK€ ¥UK1MAT$U",1350,1470],

    [1,1,"Carmen Villain b2b Hitam",720,930],
    [1,1,"Ben Vince (Live)",930,990],
    [1,1,"Full Circle",990,1140],
    [1,1,"Adam Marshall & Ricardo Tobar present Labrador (Live)",1140,1200],
    [1,1,"André Galluzzi b2b Lea Occhi",1200,1320],
    [1,1,"OK EG (Live)",1320,1380],
    [1,1,"Adiel b2b Garçon",1380,1470],

    [1,2,"Batu",720,990],
    [1,2,"Devon Rexi meets John T. Gast (Live)",990,1050],
    [1,2,"EMA b2b Verity",1050,1170],
    [1,2,"Metrist (Live)",1170,1230],
    [1,2,"Goth-Trad",1230,1320],
    [1,2,"Polygonia, Simon Popp (Live)",1320,1380],
    [1,2,"Fadi Mohem b2b Richard Akingbehin",1380,1470],

    [1,3,"Rumi de Baires",720,840],
    [1,3,"Garage Girls",840,960],
    [1,3,"Ābnamā b2b Faited",960,1080],
    [1,3,"BASHKKA b2b Jerome Sydenham",1080,1200],
    [1,3,"Fred P (Live)",1200,1260],
    [1,3,"Octo Octa b2b Virginia",1260,1380],
    [1,3,"Sandrien",1380,1470],

    [1,4,"DJ Lomalinda b2b Phillip Jondo",720,870],
    [1,4,"MMM",870,990],
    [1,4,"DJ Haram & Sha Ray (Live)",990,1050],
    [1,4,"DJ Ramon Sucesso",1050,1110],
    [1,4,"French II (Live)",1110,1170],
    [1,4,"DNGDNGDNG & Phran: Sonido Underground (Hybrid)",1170,1260],
    [1,4,"Bitter Babe b2b Carista",1260,1380],
    [1,4,"DJ Playero",1380,1470],

    [1,5,"Ræza",720,870],
    [1,5,"Mari Sakurai",870,990],
    [1,5,"Delano Legito b2b Shinedoe",990,1110],
    [1,5,"Rod b2b Rolando",1110,1230],
    [1,5,"Altinbas (Live)",1230,1290],
    [1,5,"Kangding Ray x Lumus present Snelweg (Live)",1290,1350],
    [1,5,"Amoral b2b Jasmín",1350,1470]
  ];

  var DAY_START = 720, DAY_END = 1470;
  var SLOT_MIN = 15, SLOT_W = 64, HOUR_W = SLOT_W * 4;

  document.documentElement.style.setProperty('--track-w', ((DAY_END - DAY_START) / SLOT_MIN * SLOT_W) + 'px');
  document.documentElement.style.setProperty('--hour-w', HOUR_W + 'px');

  function px(min){ return (min - DAY_START) / SLOT_MIN * SLOT_W; }
  function fmt(min){
    var h = Math.floor(min / 60) % 24, m = min % 60;
    return (h < 10 ? '0' + h : h) + ':' + (m < 10 ? '0' + m : m);
  }
  function actId(a){ return a[0] + '-' + a[1] + '-' + a[3]; }

  var STAR = '<svg viewBox="0 0 20 20" fill="none" stroke="currentColor" stroke-width="1.6" stroke-linejoin="round"><path d="M10 2.5l2.35 4.9 5.4.72-3.9 3.78.95 5.4L10 14.8l-4.8 2.5.95-5.4-3.9-3.78 5.4-.72L10 2.5z" fill="currentColor" fill-opacity="0"/></svg>';
  var STAR_FILLED = '<svg viewBox="0 0 20 20" fill="currentColor"><path d="M10 2.5l2.35 4.9 5.4.72-3.9 3.78.95 5.4L10 14.8l-4.8 2.5.95-5.4-3.9-3.78 5.4-.72L10 2.5z"/></svg>';
  var OVERLAP_ICON = '<svg width="9" height="9" viewBox="0 0 20 20" fill="none"><circle cx="8" cy="10" r="6.2" stroke="currentColor" stroke-width="1.7"/><circle cx="13.5" cy="10" r="6.2" stroke="currentColor" stroke-width="1.7"/></svg>';

  var STORAGE_KEY = 'draaimolen-2026-saved-sets';
  var saved = loadSaved();

  function loadSaved(){
    try{
      var raw = localStorage.getItem(STORAGE_KEY);
      if (!raw) return new Set();
      var arr = JSON.parse(raw);
      if (!Array.isArray(arr)) return new Set();
      return new Set(arr);
    } catch(e){ return new Set(); }
  }
  function persistSaved(){
    try{ localStorage.setItem(STORAGE_KEY, JSON.stringify(Array.from(saved))); } catch(e){}
  }

  function clashIdsForDay(day){
    var mine = ACTS.filter(function(a){ return a[0] === day && saved.has(actId(a)); })
                   .sort(function(a,b){ return a[3] - b[3]; });
    var clashes = new Set();
    for (var i = 0; i < mine.length; i++){
      for (var j = i + 1; j < mine.length; j++){
        if (mine[j][3] < mine[i][4]) {
          clashes.add(actId(mine[i]));
          clashes.add(actId(mine[j]));
        } else break;
      }
    }
    return clashes;
  }

  // ---------- build legend ----------
  var legendEl = document.getElementById('legend');
  legendEl.innerHTML = STAGES.map(function(s){
    return '<span class="legend-item"><span class="legend-swatch" style="--sc:var(--stage-' + s.key + ')"></span>' + s.name + '</span>';
  }).join('');

  // ---------- build grids ----------
  var panelsEl = document.getElementById('panels');
  var trackEls = {}; // day -> [stageIdx] -> track element
  var actEls = {};   // id -> element(s)

  DAYS.forEach(function(dayName, dayIdx){
    var panel = document.createElement('div');
    panel.className = 'day-panel';
    panel.hidden = dayIdx !== 0;
    panel.dataset.day = dayIdx;

    var shell = document.createElement('div');
    shell.className = 'tt-shell';
    var scroll = document.createElement('div');
    scroll.className = 'tt-scroll';
    var grid = document.createElement('div');
    grid.className = 'tt-grid';

    // corner
    var corner = document.createElement('div');
    corner.className = 'corner';
    corner.textContent = dayName;
    grid.appendChild(corner);

    // ruler
    var ruler = document.createElement('div');
    ruler.className = 'ruler';
    for (var m = DAY_START; m <= DAY_END; m += 60){
      var tick = document.createElement('div');
      tick.className = 'tick';
      tick.style.left = px(m) + 'px';
      tick.textContent = fmt(m);
      ruler.appendChild(tick);
    }
    grid.appendChild(ruler);

    trackEls[dayIdx] = [];
    STAGES.forEach(function(stage, stageIdx){
      var label = document.createElement('div');
      label.className = 'stage-label';
      label.innerHTML = '<span class="bar" style="--sc:var(--stage-' + stage.key + ')"></span><span class="name">' + stage.name + '</span>';
      grid.appendChild(label);

      var track = document.createElement('div');
      track.className = 'stage-track';
      track.style.height = '96px';
      grid.appendChild(track);
      trackEls[dayIdx][stageIdx] = track;
    });

    scroll.appendChild(grid);
    shell.appendChild(scroll);
    panel.appendChild(shell);
    panelsEl.appendChild(panel);
  });

  ACTS.forEach(function(a){
    var id = actId(a);
    var stage = STAGES[a[1]];
    var track = trackEls[a[0]][a[1]];
    var btn = document.createElement('button');
    btn.type = 'button';
    btn.className = 'act';
    btn.style.setProperty('--sc', 'var(--stage-' + stage.key + ')');
    btn.style.left = px(a[3]) + 'px';
    btn.style.width = Math.max(px(a[4]) - px(a[3]) - 6, 46) + 'px';
    btn.dataset.id = id;
    btn.setAttribute('aria-pressed', 'false');
    btn.setAttribute('aria-label', a[2] + ', ' + stage.name + ', ' + DAYS[a[0]] + ' ' + fmt(a[3]) + '–' + fmt(a[4]));
    btn.title = a[2] + ' · ' + stage.name + ' · ' + fmt(a[3]) + '–' + fmt(a[4]);
    btn.innerHTML =
      '<span class="name">' + a[2] + '</span>' +
      '<span class="warn">' + OVERLAP_ICON + ' Same time</span>' +
      '<span class="foot"><span class="time">' + fmt(a[3]) + '–' + fmt(a[4]) + '</span><span class="star">' + STAR + '</span></span>';
    btn.addEventListener('click', function(){ toggleSave(id); });
    track.appendChild(btn);
    actEls[id] = btn;
  });

  function toggleSave(id){
    if (saved.has(id)) saved.delete(id); else saved.add(id);
    persistSaved();
    renderAll();
  }

  // ---------- day switch ----------
  var dayButtons = Array.prototype.slice.call(document.querySelectorAll('.day-switch button'));
  var panelEls = Array.prototype.slice.call(document.querySelectorAll('.day-panel'));
  var currentDay = 0;
  dayButtons.forEach(function(btn){
    btn.addEventListener('click', function(){
      currentDay = parseInt(btn.dataset.day, 10);
      dayButtons.forEach(function(b){ b.setAttribute('aria-pressed', b === btn ? 'true' : 'false'); });
      panelEls.forEach(function(p){ p.hidden = parseInt(p.dataset.day, 10) !== currentDay; });
    });
  });

  // ---------- schedule bar + drawer ----------
  var savedCountEl = document.getElementById('savedCount');
  var clashCountEl = document.getElementById('clashCount');
  var scheduleHint = document.getElementById('scheduleHint');
  var scheduleBar = document.getElementById('scheduleBar');
  var drawer = document.getElementById('drawer');
  var drawerToggle = document.getElementById('drawerToggle');
  var drawerInner = document.getElementById('drawerInner');
  var drawerOpen = false;
  var drawerDay = 0;

  drawerToggle.addEventListener('click', function(){
    drawerOpen = !drawerOpen;
    drawer.dataset.open = String(drawerOpen);
    scheduleBar.dataset.open = String(drawerOpen);
    drawerToggle.setAttribute('aria-expanded', String(drawerOpen));
  });

  function renderAll(){
    var allClashes = {};
    var totalClash = 0;
    DAYS.forEach(function(dn, di){
      var c = clashIdsForDay(di);
      allClashes[di] = c;
      totalClash += c.size;
    });

    ACTS.forEach(function(a){
      var id = actId(a);
      var el = actEls[id];
      var isSaved = saved.has(id);
      var isClash = allClashes[a[0]].has(id);
      el.dataset.saved = String(isSaved);
      el.dataset.clash = String(isClash);
      el.setAttribute('aria-pressed', String(isSaved));
      var starEl = el.querySelector('.star');
      starEl.innerHTML = isSaved ? STAR_FILLED : STAR;
    });

    savedCountEl.textContent = String(saved.size);
    clashCountEl.textContent = String(totalClash / 2 || 0);

    if (saved.size === 0){
      scheduleHint.textContent = 'Tap a set below to start building your weekend.';
    } else if (totalClash > 0){
      scheduleHint.textContent = 'A couple of your picks land at the same time — see which ones below.';
    } else {
      scheduleHint.textContent = "You're set — nothing on your list overlaps.";
    }

    renderDrawer(allClashes);
  }

  var AGENDA_PX_PER_MIN = 1.7;
  var AGENDA_PAD = 16;

  // Lays saved sets out on a shared vertical clock, the same way the main
  // grid lays them out horizontally — sets that overlap simply land in
  // side-by-side lanes at the same height, so the overlap is something you
  // see, not just something you're told.
  function buildAgenda(dayActs, clashSet){
    if (dayActs.length === 0) return '';

    var sorted = dayActs.slice().sort(function(a, b){ return a[3] - b[3]; });
    var tMin = Math.floor(sorted[0][3] / 60) * 60;
    var tMax = Math.ceil(Math.max.apply(null, sorted.map(function(a){ return a[4]; })) / 60) * 60;
    if (tMax - tMin < 60) tMax = tMin + 60;

    // Greedy interval partitioning: walk sets in start order, drop each
    // into the first lane that's free by then, else open a new lane.
    var laneEnds = [];
    var laneOf = {};
    sorted.forEach(function(a){
      var id = actId(a);
      var lane = laneEnds.findIndex(function(end){ return end <= a[3]; });
      if (lane === -1){ lane = laneEnds.length; laneEnds.push(a[4]); }
      else { laneEnds[lane] = a[4]; }
      laneOf[id] = lane;
    });
    var totalLanes = Math.max(laneEnds.length, 1);

    var ticks = '';
    for (var m = tMin; m <= tMax; m += 60){
      ticks += '<div class="tick" style="top:' + (AGENDA_PAD + (m - tMin) * AGENDA_PX_PER_MIN) + 'px">' + fmt(m) + '</div>';
    }

    var blocks = sorted.map(function(a){
      var id = actId(a);
      var stage = STAGES[a[1]];
      var top = AGENDA_PAD + (a[3] - tMin) * AGENDA_PX_PER_MIN;
      var height = Math.max((a[4] - a[3]) * AGENDA_PX_PER_MIN - 4, 42);
      var leftPct = laneOf[id] / totalLanes * 100;
      var widthPct = 100 / totalLanes;
      var isClash = clashSet.has(id);
      return '<div class="agenda-block" data-clash="' + isClash + '" style="--sc:var(--stage-' + stage.key + ');' +
          'top:' + top + 'px;height:' + height + 'px;left:calc(' + leftPct + '% + 4px);width:calc(' + widthPct + '% - 8px)">' +
        '<button type="button" class="remove" data-id="' + id + '" aria-label="Remove ' + a[2].replace(/"/g,'&quot;') + '">×</button>' +
        '<div class="name">' + a[2] + '</div>' +
        '<div class="meta"><span class="dot"></span>' + stage.name + ' · ' + fmt(a[3]) + '–' + fmt(a[4]) + '</div>' +
        (isClash ? '<div class="same-time">' + OVERLAP_ICON + ' Same time</div>' : '') +
      '</div>';
    }).join('');

    var totalHeight = AGENDA_PAD * 2 + (tMax - tMin) * AGENDA_PX_PER_MIN;
    return '<div class="agenda-wrap"><div class="agenda-scroll"><div class="agenda" style="height:' + totalHeight + 'px; --hour-h:' + (60 * AGENDA_PX_PER_MIN) + 'px">' +
      '<div class="agenda-ruler">' + ticks + '</div>' +
      '<div class="agenda-lanes">' + blocks + '</div>' +
    '</div></div></div>';
  }

  function renderDrawer(allClashes){
    var counts = DAYS.map(function(dayName, dayIdx){
      return ACTS.filter(function(a){ return a[0] === dayIdx && saved.has(actId(a)); }).length;
    });

    var tabsHtml = '<div class="drawer-tabs" role="tablist" aria-label="Favourited sets by day">' +
      DAYS.map(function(dayName, dayIdx){
        return '<button type="button" role="tab" data-day="' + dayIdx + '" aria-pressed="' + (drawerDay === dayIdx) + '">' +
          dayName + '<span class="count">' + counts[dayIdx] + '</span></button>';
      }).join('') + '</div>';

    var dayActs = ACTS.filter(function(a){ return a[0] === drawerDay && saved.has(actId(a)); });

    var bodyHtml = dayActs.length === 0
      ? '<div class="drawer-empty">No ' + DAYS[drawerDay] + ' sets saved yet. Tap sets in the ' + DAYS[drawerDay] + ' grid to add them here.</div>'
      : buildAgenda(dayActs, allClashes[drawerDay]);

    drawerInner.innerHTML = tabsHtml + bodyHtml;

    Array.prototype.slice.call(drawerInner.querySelectorAll('.drawer-tabs button')).forEach(function(btn){
      btn.addEventListener('click', function(){
        drawerDay = parseInt(btn.dataset.day, 10);
        renderAll();
      });
    });
    Array.prototype.slice.call(drawerInner.querySelectorAll('.remove')).forEach(function(btn){
      btn.addEventListener('click', function(){ toggleSave(btn.dataset.id); });
    });
  }

  renderAll();
})();
</script>
