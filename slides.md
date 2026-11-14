---
theme: seriph
title: The Soccer Similarity Score
aspectRatio: 1.7777777778
class: soccer-question
layout: default
---

<main class="question-slide">
  <p class="question-setup">If Arsenal are so boring...</p>
  <div class="question-accent" aria-hidden="true"></div>
  <p v-click.fade-in class="research-question">Which other teams play like them?</p>
</main>

<style>
.soccer-question {
  color: #343434;
  background: #f7f5f0;
}

.soccer-question .question-slide {
  box-sizing: border-box;
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 3rem 5rem;
  text-align: center;
}

.soccer-question .question-setup {
  margin: 0;
  color: #77736e;
  font-family: Inter, 'Aptos', Arial, sans-serif;
  font-size: clamp(1.35rem, 2.3vw, 1.85rem);
  font-style: italic;
  letter-spacing: 0.005em;
  line-height: 1.35;
}

.soccer-question .question-accent {
  width: 2.4rem;
  height: 3px;
  margin: 1.2rem 0;
  border-radius: 2px;
  background: #c8102e;
}

.soccer-question .research-question {
  max-width: 90%;
  margin: 0;
  color: #282a2d;
  font-family: Georgia, 'Times New Roman', serif;
  font-size: clamp(2.8rem, 5.5vw, 4.6rem);
  font-weight: 500;
  letter-spacing: -0.035em;
  line-height: 1.1;
}

@media (max-width: 700px) {
  .soccer-question .question-slide {
    padding: 2rem 1.5rem;
  }

  .soccer-question .research-question {
    max-width: 100%;
  }
}
</style>

---
class: soccer-measure
layout: default
---

<main class="measure-slide">
  <h1>Can We Measure Playing Style?</h1>

  <section class="style-traits" aria-label="Soccer characteristics">
    <article v-click.fade-in class="style-trait">
      <svg viewBox="0 0 240 140" aria-hidden="true">
        <defs>
          <marker id="press-arrow" viewBox="0 0 10 10" refX="8" refY="5" markerWidth="6" markerHeight="6" orient="auto">
            <path class="arrowhead" d="M0 0l10 5-10 5z" />
          </marker>
        </defs>
        <rect class="pitch" x="8" y="8" width="224" height="124" rx="2" />
        <path class="field-line" d="M120 8v124M120 51a21 21 0 1 0 0 42 21 21 0 1 0 0-42" />
        <path class="pressure-arrow" d="M63 43l30 16" marker-end="url(#press-arrow)" />
        <path class="pressure-arrow" d="M63 97l30-16" marker-end="url(#press-arrow)" />
        <circle class="player-defending" cx="55" cy="39" r="8" />
        <circle class="player-defending" cx="55" cy="101" r="8" />
        <circle class="player-opposing" cx="104" cy="70" r="8" />
        <circle class="ball" cx="116" cy="70" r="3.5" />
      </svg>
      <span>Pressing</span>
    </article>
    <article v-click.fade-in class="style-trait">
      <svg viewBox="0 0 240 140" aria-hidden="true">
        <defs>
          <marker id="pass-arrow" viewBox="0 0 10 10" refX="8" refY="5" markerWidth="6" markerHeight="6" orient="auto">
            <path class="arrowhead" d="M0 0l10 5-10 5z" />
          </marker>
        </defs>
        <rect class="pitch" x="8" y="8" width="224" height="124" rx="2" />
        <path class="field-line" d="M120 8v124M120 51a21 21 0 1 0 0 42 21 21 0 1 0 0-42" />
        <path class="pass-arrow" d="M54 93Q77 69 98 52" marker-end="url(#pass-arrow)" />
        <path class="pass-arrow" d="M116 49Q143 52 169 82" marker-end="url(#pass-arrow)" />
        <circle class="player-team" cx="48" cy="99" r="8" />
        <circle class="player-team" cx="105" cy="47" r="8" />
        <circle class="player-team" cx="176" cy="89" r="8" />
        <circle class="ball" cx="60" cy="96" r="3.5" />
      </svg>
      <span>Passing</span>
    </article>
    <article v-click.fade-in class="style-trait">
      <svg viewBox="0 0 240 140" aria-hidden="true">
        <defs>
          <marker id="chance-arrow" viewBox="0 0 10 10" refX="8" refY="5" markerWidth="6" markerHeight="6" orient="auto">
            <path class="arrowhead" d="M0 0l10 5-10 5z" />
          </marker>
          <marker id="shot-arrow" viewBox="0 0 10 10" refX="8" refY="5" markerWidth="6" markerHeight="6" orient="auto">
            <path class="arrowhead" d="M0 0l10 5-10 5z" />
          </marker>
        </defs>
        <rect class="pitch" x="8" y="8" width="224" height="124" rx="2" />
        <path class="field-line" d="M120 8v124M120 51a21 21 0 1 0 0 42 21 21 0 1 0 0-42M192 43h40v54h-40zM210 56h22v28h-22z" />
        <path class="pass-arrow" d="M68 92Q103 69 139 52" marker-end="url(#chance-arrow)" />
        <path class="shot-arrow" d="M156 51Q183 57 211 69" marker-end="url(#shot-arrow)" />
        <circle class="player-team" cx="61" cy="97" r="8" />
        <circle class="player-team" cx="147" cy="49" r="8" />
        <circle class="ball" cx="72" cy="90" r="3.5" />
      </svg>
      <span>Shot Creation</span>
    </article>
  </section>

  <div v-click.fade-in class="data-takeaway">
    <svg class="takeaway-arrow" viewBox="0 0 36 32" aria-hidden="true"><path d="M18 2v22M8 15l10 10 10-10" /></svg>
    <p>Compare teams using data</p>
  </div>
</main>

<style>
.soccer-measure {
  color: #282a2d;
  background: #f7f5f0;
}

.soccer-measure .measure-slide {
  box-sizing: border-box;
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 2.5rem 4rem;
  text-align: center;
}

.soccer-measure h1 {
  margin: 0 0 2.8rem;
  color: #282a2d;
  font-family: Georgia, 'Times New Roman', serif;
  font-size: clamp(2.25rem, 4.2vw, 3.35rem);
  font-weight: 500;
  letter-spacing: -0.035em;
  line-height: 1.1;
}

.soccer-measure .style-traits {
  width: min(100%, 1080px);
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: clamp(0.75rem, 2.3vw, 2.4rem);
  align-items: start;
}

.soccer-measure .style-trait {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: flex-start;
  gap: 0.7rem;
  color: #34363a;
  font-family: Inter, 'Aptos', Arial, sans-serif;
  font-size: clamp(1.3rem, 2.1vw, 1.65rem);
  font-weight: 500;
}

.soccer-measure .style-trait svg {
  display: block;
  width: min(100%, 18rem);
  height: auto;
  fill: none;
  stroke: #b6b2ab;
  stroke-linecap: round;
  stroke-linejoin: round;
  stroke-width: 1.6;
}

.soccer-measure .pitch {
  fill: #f1efe9;
  stroke: #b8b4ad;
}

.soccer-measure .field-line {
  fill: none;
  stroke: #c9c5be;
  stroke-width: 1.4;
}

.soccer-measure .player-team,
.soccer-measure .player-defending {
  fill: #c8102e;
  stroke: #f7f5f0;
  stroke-width: 1.5;
}

.soccer-measure .player-opposing {
  fill: #34363a;
  stroke: #f7f5f0;
  stroke-width: 1.5;
}

.soccer-measure .ball {
  fill: #fffdf8;
  stroke: #34363a;
  stroke-width: 1.5;
}

.soccer-measure .pressure-arrow,
.soccer-measure .pass-arrow,
.soccer-measure .shot-arrow {
  fill: none;
  stroke: #c8102e;
  stroke-width: 2;
}

.soccer-measure .pass-arrow {
  stroke-dasharray: 4 4;
}

.soccer-measure .shot-arrow {
  stroke-width: 2.6;
}

.soccer-measure .arrowhead {
  fill: #c8102e;
  stroke: none;
}

.soccer-measure .data-takeaway {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: 1.15rem;
}

.soccer-measure .takeaway-arrow {
  width: 1.6rem;
  height: 1.4rem;
  margin-bottom: 0.25rem;
  fill: none;
  stroke: #c8102e;
  stroke-linecap: round;
  stroke-linejoin: round;
  stroke-width: 2;
}

.soccer-measure .data-takeaway p {
  margin: 0;
  color: #282a2d;
  font-family: Georgia, 'Times New Roman', serif;
  font-size: clamp(1.85rem, 3.1vw, 2.5rem);
  font-weight: 500;
  letter-spacing: -0.02em;
}

@media (max-width: 700px) {
  .soccer-measure .measure-slide {
    padding: 2rem 1.3rem;
  }

  .soccer-measure h1 {
    margin-bottom: 2.4rem;
  }

  .soccer-measure .style-traits {
    gap: 0.75rem;
  }

  .soccer-measure .style-trait {
    font-size: 1.05rem;
  }
}
</style>

---
class: soccer-data-loss
layout: default
---

<main class="data-loss-slide">
  <header class="data-loss-heading">
    <h1>The Data Disappeared</h1>
    <div class="heading-accent" aria-hidden="true"></div>
  </header>
  <section class="stats-comparison" aria-label="Advanced statistics available from FBref before and after the data removal">
    <div class="stats-panel before-panel">
      <h2>Before</h2>
      <div class="stat-list">
        <div class="stat-row"><span class="status-mark available" aria-hidden="true">✓</span><span>Expected goals</span></div>
        <div class="stat-row"><span class="status-mark available" aria-hidden="true">✓</span><span>Defensive pressures</span></div>
        <div class="stat-row"><span class="status-mark available" aria-hidden="true">✓</span><span>Possession</span></div>
      </div>
    </div>
    <svg class="comparison-arrow" viewBox="0 0 48 32" aria-hidden="true"><path d="M3 16h38M29 5l12 11-12 11" /></svg>
    <div class="stats-panel after-panel">
      <h2 v-click.fade-in="3">After</h2>
      <div v-click.fade-in="3" class="stat-list removed-list">
        <div class="stat-row"><span class="status-mark removed" aria-hidden="true">×</span><span>Expected goals</span></div>
        <div class="stat-row"><span class="status-mark removed" aria-hidden="true">×</span><span>Defensive pressures</span></div>
        <div class="stat-row"><span class="status-mark removed" aria-hidden="true">×</span><span>Possession</span></div>
      </div>
    </div>
  </section>
  <section class="data-timeline" aria-label="Research project timeline">
    <div class="timeline-rail" aria-hidden="true"></div>
    <div class="timeline-events">
      <article v-click.fade-in="1" class="timeline-event approved-event">
        <span class="timeline-marker available" aria-hidden="true">✓</span>
        <div class="event-date">Late November 2025</div>
        <div class="event-label">Project approved!</div>
      </article>
      <article v-click.fade-in="2" class="timeline-event removed-event">
        <span class="timeline-marker removed" aria-hidden="true">×</span>
        <div class="event-date">Early 2026</div>
        <div class="event-label">Advanced data removed</div>
      </article>
    </div>
  </section>
</main>

<style>
.soccer-data-loss {
  color: #282a2d;
  background: #f7f5f0;
}

.soccer-data-loss .data-loss-slide {
  box-sizing: border-box;
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: flex-start;
  padding: 2.1rem 3.5rem 1.55rem;
  text-align: center;
}

.soccer-data-loss .data-loss-heading h1 {
  margin: 0;
  color: #282a2d;
  font-family: Georgia, 'Times New Roman', serif;
  font-size: clamp(2.2rem, 4.2vw, 3.35rem);
  font-weight: 500;
  letter-spacing: -0.035em;
  line-height: 1.1;
}

.soccer-data-loss .heading-accent {
  width: 2.25rem;
  height: 3px;
  margin: 0.8rem auto 1.35rem;
  border-radius: 2px;
  background: #c8102e;
}

.soccer-data-loss .stats-comparison {
  width: min(100%, 980px);
  display: grid;
  grid-template-columns: minmax(0, 1fr) 3.2rem minmax(0, 1fr);
  align-items: center;
  gap: clamp(1rem, 2.3vw, 2rem);
}

.soccer-data-loss .stats-panel {
  min-height: 12.5rem;
  box-sizing: border-box;
  padding: 1.2rem 1.4rem 1.3rem;
  border: 1px solid #e1ded7;
  border-radius: 8px;
  background: rgba(255, 255, 255, 0.52);
}

.soccer-data-loss .stats-panel h2 {
  margin: 0 0 0.8rem;
  color: #34363a;
  font-family: Georgia, 'Times New Roman', serif;
  font-size: clamp(1.5rem, 2.3vw, 1.8rem);
  font-weight: 500;
}

.soccer-data-loss .stat-list {
  display: grid;
  gap: 0.45rem;
}

.soccer-data-loss .stat-row {
  display: flex;
  align-items: center;
  justify-content: flex-start;
  gap: 0.75rem;
  min-height: 2rem;
  color: #34363a;
  font-family: Inter, 'Aptos', Arial, sans-serif;
  font-size: clamp(1.08rem, 1.75vw, 1.35rem);
  text-align: left;
}

.soccer-data-loss .status-mark {
  width: 1.45rem;
  height: 1.45rem;
  flex: 0 0 1.45rem;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  box-sizing: border-box;
  border: 1.5px solid currentColor;
  border-radius: 50%;
  font-family: Arial, sans-serif;
  font-size: 0.98rem;
  font-weight: 700;
  line-height: 1;
}

.soccer-data-loss .available {
  color: #43865b;
}

.soccer-data-loss .removed {
  color: #c8102e;
}

.soccer-data-loss .comparison-arrow {
  width: 2.5rem;
  height: 1.7rem;
  fill: none;
  stroke: #c8102e;
  stroke-linecap: round;
  stroke-linejoin: round;
  stroke-width: 2;
}

.soccer-data-loss .data-timeline {
  position: relative;
  width: min(80%, 760px);
  margin-top: auto;
  padding-top: 0.35rem;
}

.soccer-data-loss .timeline-rail {
  position: absolute;
  top: 1.25rem;
  left: 25%;
  right: 25%;
  height: 2px;
  background: #d8d4cd;
}

.soccer-data-loss .timeline-events {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 1rem;
}

.soccer-data-loss .timeline-event {
  min-height: 6.7rem;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.soccer-data-loss .timeline-marker {
  z-index: 1;
  width: 1.8rem;
  height: 1.8rem;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  box-sizing: border-box;
  border: 1.5px solid currentColor;
  border-radius: 50%;
  background: #f7f5f0;
  font-family: Arial, sans-serif;
  font-size: 1.1rem;
  font-weight: 700;
  line-height: 1;
}

.soccer-data-loss .event-date {
  margin-top: 0.45rem;
  color: #77736e;
  font-family: Inter, 'Aptos', Arial, sans-serif;
  font-size: clamp(1rem, 1.65vw, 1.22rem);
  letter-spacing: 0.01em;
}

.soccer-data-loss .event-label {
  margin-top: 0.2rem;
  color: #34363a;
  font-family: Georgia, 'Times New Roman', serif;
  font-size: clamp(1.2rem, 1.9vw, 1.48rem);
}

@media (max-width: 700px) {
  .soccer-data-loss .data-loss-slide {
    padding: 1.45rem 1.2rem 1.1rem;
  }

  .soccer-data-loss .stats-comparison {
    grid-template-columns: minmax(0, 1fr) 1.8rem minmax(0, 1fr);
    gap: 0.45rem;
  }

  .soccer-data-loss .stats-panel {
    min-height: 11rem;
    padding: 0.8rem 0.65rem;
  }

  .soccer-data-loss .stat-row {
    gap: 0.35rem;
    font-size: 0.95rem;
  }

  .soccer-data-loss .status-mark {
    width: 1.2rem;
    height: 1.2rem;
    flex-basis: 1.2rem;
    font-size: 0.85rem;
  }

  .soccer-data-loss .comparison-arrow {
    width: 1.6rem;
  }

  .soccer-data-loss .data-timeline {
    width: 96%;
  }
}
</style>

<!-- Source for the removal timeline: https://www.sports-reference.com/blog/2026/01/fbref-stathead-data-update/ -->

---
class: soccer-data-workflow
layout: default
---

<main class="data-workflow-slide">
  <h1>Getting the Remaining Data Wasn't Easy Either...</h1>
  <section class="failed-approach" aria-label="Unsuccessful automated collection attempt">
    <div class="automated-label">Automated collection</div>
    <svg class="attempt-diagram" viewBox="0 0 230 82" aria-hidden="true">
      <rect class="script-page" x="8" y="12" width="48" height="58" rx="4" />
      <path class="icon-line" d="M18 24h16M18 31h12" />
      <circle class="r-badge" cx="39" cy="52" r="13" />
      <text class="r-letter" x="39" y="58" text-anchor="middle">R</text>
      <path class="attempt-arrow" d="M67 41h49m-9-8 9 8-9 8" />
      <rect class="browser-window" x="129" y="15" width="88" height="54" rx="4" />
      <path class="icon-line" d="M129 28h88M139 38h28m-28 8h50m-50 8h40" />
      <circle class="browser-dot" cx="139" cy="22" r="2" />
      <circle class="browser-dot" cx="146" cy="22" r="2" />
    </svg>
    <div class="blocked-state">
      <span class="blocked-mark" aria-hidden="true">×</span>
      <span>Blocked</span>
    </div>
  </section>

  <div class="workflow-divider" aria-hidden="true"></div>

  <section class="collection-workflow" aria-label="Manual saving and local data extraction workflow">
    <article v-click.fade-in="1" class="workflow-step">
      <svg viewBox="0 0 80 60" aria-hidden="true">
        <rect class="window-frame" x="7" y="7" width="66" height="46" rx="4" />
        <path class="icon-line" d="M7 19h66M16 13h1m6 0h1m6 0h1M16 28h28m-28 7h38m-38 7h24" />
        <path class="cursor-mark" d="M50 30l2 18 5-5 5 9 4-2-5-9 7-1z" />
      </svg>
      <span>Save webpages</span>
    </article>
    <svg v-click.fade-in="2" class="workflow-arrow" viewBox="0 0 44 24" aria-hidden="true"><path d="M3 12h34m-9-8 9 8-9 8" /></svg>
    <article v-click.fade-in="2" class="workflow-step">
      <svg viewBox="0 0 80 60" aria-hidden="true">
        <path class="document-frame" d="M20 5h27l14 14v36H20z" />
        <path class="icon-line" d="M47 5v14h14M28 30h25m-25 7h25m-25 7h18" />
        <path class="accent-line" d="M28 23h11" />
      </svg>
      <span>HTML files</span>
    </article>
    <svg v-click.fade-in="3" class="workflow-arrow" viewBox="0 0 44 24" aria-hidden="true"><path d="M3 12h34m-9-8 9 8-9 8" /></svg>
    <article v-click.fade-in="3" class="workflow-step">
      <svg viewBox="0 0 80 60" aria-hidden="true">
        <path class="document-frame" d="M14 5h30l14 14v36H14z" />
        <path class="icon-line" d="M44 5v14h14M22 32h8m-8 7h8m-8 7h8" />
        <circle class="r-badge" cx="48" cy="40" r="14" />
        <text class="r-letter" x="48" y="46" text-anchor="middle">R</text>
      </svg>
      <span>R extracts tables</span>
    </article>
    <svg v-click.fade-in="4" class="workflow-arrow" viewBox="0 0 44 24" aria-hidden="true"><path d="M3 12h34m-9-8 9 8-9 8" /></svg>
    <article v-click.fade-in="4" class="workflow-step">
      <svg viewBox="0 0 80 60" aria-hidden="true">
        <rect class="table-frame" x="10" y="8" width="60" height="44" rx="3" />
        <path class="table-grid" d="M10 22h60M10 37h60M30 22v30m20-30v30" />
        <path class="accent-line" d="M18 15h10" />
      </svg>
      <span>CSV files</span>
    </article>
  </section>
</main>

<style>
.soccer-data-workflow {
  color: #282a2d;
  background: #f7f5f0;
}

.soccer-data-workflow .data-workflow-slide {
  box-sizing: border-box;
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: flex-start;
  padding: 2rem 3rem 1.7rem;
  text-align: center;
}

.soccer-data-workflow h1 {
  max-width: 100%;
  margin: 0 0 0.8rem;
  color: #282a2d;
  font-family: Georgia, 'Times New Roman', serif;
  font-size: clamp(2rem, 3.8vw, 3.05rem);
  font-weight: 500;
  letter-spacing: -0.035em;
  line-height: 1.12;
}

.soccer-data-workflow .failed-approach {
  box-sizing: border-box;
  width: min(100%, 990px);
  min-height: 7.6rem;
  display: grid;
  grid-template-columns: minmax(11rem, 1fr) minmax(15rem, 1.25fr) minmax(8rem, 0.75fr);
  align-items: center;
  justify-items: center;
  gap: 1rem;
  padding: 0.75rem 1.4rem;
  border: 1px solid #e2ded7;
  border-radius: 8px;
  background: rgba(255, 255, 255, 0.48);
}

.soccer-data-workflow .automated-label {
  color: #34363a;
  font-family: Inter, 'Aptos', Arial, sans-serif;
  font-size: clamp(1.15rem, 1.9vw, 1.45rem);
  font-weight: 500;
}

.soccer-data-workflow .attempt-diagram {
  width: min(100%, 15rem);
  height: auto;
  overflow: visible;
}

.soccer-data-workflow .script-page,
.soccer-data-workflow .browser-window,
.soccer-data-workflow .window-frame,
.soccer-data-workflow .document-frame,
.soccer-data-workflow .table-frame {
  fill: #fbfaf7;
  stroke: #aaa69e;
  stroke-width: 1.6;
}

.soccer-data-workflow .icon-line,
.soccer-data-workflow .table-grid {
  fill: none;
  stroke: #8d8982;
  stroke-linecap: round;
  stroke-linejoin: round;
  stroke-width: 1.7;
}

.soccer-data-workflow .attempt-arrow {
  fill: none;
  stroke: #aaa69e;
  stroke-dasharray: 3 3;
  stroke-linecap: round;
  stroke-linejoin: round;
  stroke-width: 1.8;
}

.soccer-data-workflow .r-badge {
  fill: #c8102e;
}

.soccer-data-workflow .r-letter {
  fill: #fffdf8;
  font-family: Georgia, 'Times New Roman', serif;
  font-size: 18px;
  font-weight: 700;
}

.soccer-data-workflow .browser-dot {
  fill: #c8102e;
}

.soccer-data-workflow .blocked-state {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 0.55rem;
  color: #c8102e;
  font-family: Inter, 'Aptos', Arial, sans-serif;
  font-size: clamp(1.15rem, 1.9vw, 1.45rem);
  font-weight: 600;
}

.soccer-data-workflow .blocked-mark {
  width: 1.8rem;
  height: 1.8rem;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  border: 1.5px solid currentColor;
  border-radius: 50%;
  font-family: Arial, sans-serif;
  font-size: 1.3rem;
  line-height: 1;
}

.soccer-data-workflow .workflow-divider {
  width: min(78%, 860px);
  height: 1px;
  margin: 1.3rem 0 1.15rem;
  background: #dedad3;
}

.soccer-data-workflow .collection-workflow {
  width: min(100%, 1100px);
  display: grid;
  grid-template-columns: minmax(0, 1fr) 2.3rem minmax(0, 1fr) 2.3rem minmax(0, 1fr) 2.3rem minmax(0, 1fr);
  align-items: center;
  gap: clamp(0.3rem, 0.8vw, 0.75rem);
}

.soccer-data-workflow .workflow-step {
  min-width: 0;
  min-height: 9.7rem;
  box-sizing: border-box;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 0.75rem;
  padding: 0.9rem 0.5rem;
  border: 1px solid #e2ded7;
  border-radius: 8px;
  background: rgba(255, 255, 255, 0.48);
  color: #34363a;
  font-family: Inter, 'Aptos', Arial, sans-serif;
  font-size: clamp(1rem, 1.55vw, 1.25rem);
  font-weight: 500;
  line-height: 1.25;
}

.soccer-data-workflow .workflow-step svg {
  display: block;
  width: min(100%, 6rem);
  height: auto;
}

.soccer-data-workflow .workflow-step .r-badge {
  fill: #c8102e;
}

.soccer-data-workflow .cursor-mark {
  fill: #c8102e;
  stroke: #fbfaf7;
  stroke-linejoin: round;
  stroke-width: 1.1;
}

.soccer-data-workflow .accent-line {
  fill: none;
  stroke: #c8102e;
  stroke-linecap: round;
  stroke-width: 2;
}

.soccer-data-workflow .table-grid {
  stroke: #c8102e;
  stroke-width: 1.3;
}

.soccer-data-workflow .workflow-arrow {
  width: 100%;
  height: 1.3rem;
  fill: none;
  stroke: #c8102e;
  stroke-linecap: round;
  stroke-linejoin: round;
  stroke-width: 1.8;
}

@media (max-width: 700px) {
  .soccer-data-workflow .data-workflow-slide {
    padding: 1.3rem 1rem;
  }

  .soccer-data-workflow .failed-approach {
    grid-template-columns: minmax(8rem, 1fr) minmax(9rem, 1.15fr) minmax(5.5rem, 0.8fr);
    gap: 0.35rem;
    padding: 0.55rem;
  }

  .soccer-data-workflow .workflow-step {
    min-height: 8rem;
    gap: 0.4rem;
    padding: 0.55rem 0.25rem;
    font-size: 0.85rem;
  }

  .soccer-data-workflow .collection-workflow {
    grid-template-columns: minmax(0, 1fr) 1rem minmax(0, 1fr) 1rem minmax(0, 1fr) 1rem minmax(0, 1fr);
    gap: 0.2rem;
  }
}
</style>

---
class: soccer-cleaning
layout: default
---

<main class="cleaning-slide cleaning-replacement">
  <h1>The Data Still Needed Cleaning</h1>
  <section class="cleaning-panels" aria-label="Three data-cleaning problems">
    <article v-click.fade-in="1" class="cleaning-card">
      <svg class="cleaning-icon" viewBox="0 0 28 28" aria-hidden="true">
        <rect x="3" y="3" width="22" height="22" rx="3" />
        <path d="M3 10h22M3 17h22M10 3v22M17 3v22" />
        <rect class="icon-gap" x="11" y="11" width="5" height="5" rx="1" />
      </svg>
      <h2>Missing Statistics</h2>
      <svg class="mini-table" viewBox="0 0 240 124" role="img" aria-label="Light blue table grid with scattered pink missing cells">
        <rect class="table-base" x="12" y="12" width="216" height="100" rx="4" />
        <path class="table-grid" d="M12 37h216M12 62h216M12 87h216M66 12v100M120 12v100M174 12v100" />
        <rect class="table-missing" x="68" y="39" width="50" height="21" rx="2" />
        <rect class="table-missing" x="176" y="64" width="50" height="21" rx="2" />
        <rect class="table-missing" x="14" y="89" width="50" height="21" rx="2" />
      </svg>
      <p>Not tracked every season</p>
    </article>
    <article v-click.fade-in="2" class="cleaning-card">
      <svg class="cleaning-icon" viewBox="0 0 28 28" aria-hidden="true">
        <rect x="4" y="5" width="15" height="18" rx="2" />
        <rect x="9" y="3" width="15" height="18" rx="2" />
        <path d="M12 8h9M12 12h9M12 16h9" />
      </svg>
      <h2>Duplicate Variables</h2>
      <svg class="mini-table" viewBox="0 0 240 124" role="img" aria-label="Three-column grid with the middle column pink and outlined in dashed red">
        <rect class="table-base" x="12" y="12" width="216" height="100" rx="4" />
        <rect class="table-highlight" x="85" y="13" width="70" height="98" />
        <path class="table-grid" d="M12 37h216M12 62h216M12 87h216M84 12v100M156 12v100" />
        <rect class="table-duplicate-outline" x="82" y="10" width="76" height="104" rx="3" />
      </svg>
      <p>Repeated across tables</p>
    </article>
    <article v-click.fade-in="3" class="cleaning-card">
      <svg class="cleaning-icon" viewBox="0 0 28 28" aria-hidden="true">
        <rect x="3" y="5" width="22" height="18" rx="3" />
        <path d="M3 11h22M14 11v12" />
        <path class="icon-fill" d="M6 8h5M6 15h5M6 19h5" />
      </svg>
      <h2>Non-Numerical Columns</h2>
      <svg class="mini-table" viewBox="0 0 240 124" role="img" aria-label="Two-column table with Team highlighted pink and Value in light blue">
        <rect class="table-base" x="12" y="12" width="216" height="100" rx="4" />
        <rect class="table-highlight" x="13" y="13" width="106" height="98" />
        <path class="table-grid" d="M12 45h216M12 78h216M120 12v100" />
        <text class="table-label" x="26" y="34">Team</text>
        <text class="table-label" x="145" y="34">Goals</text>
      </svg>
      <p>Names, years, and labels</p>
    </article>
  </section>
  <div v-click.fade-in="4" class="cleaning-takeaway">
    <svg viewBox="0 0 24 24" aria-hidden="true">
      <circle cx="12" cy="12" r="9" />
      <path d="m7.5 12.2 3 3 6-6.4" />
    </svg>
    <span>Data is now complete and numeric only</span>
  </div>
</main>

<style>
.soccer-cleaning { color: #282a2d; background: #f7f5f0; }
.soccer-cleaning .cleaning-slide { box-sizing: border-box; width: 100%; height: 100%; display: flex; flex-direction: column; align-items: center; padding: 2rem 3rem 1.7rem; text-align: center; }
.soccer-cleaning h1 { margin: 0 0 1.8rem; color: #282a2d; font-family: Georgia, 'Times New Roman', serif; font-size: clamp(2.2rem, 4.2vw, 3.25rem); font-weight: 500; letter-spacing: -0.035em; line-height: 1.1; }
.soccer-cleaning .cleaning-panels { width: min(100%, 1120px); flex: 1; display: grid; grid-template-columns: repeat(3, minmax(0, 1fr)); align-items: stretch; gap: clamp(1rem, 2.2vw, 2rem); }
.soccer-cleaning .cleaning-card { min-width: 0; min-height: 20rem; box-sizing: border-box; display: flex; flex-direction: column; align-items: center; justify-content: center; gap: 0.8rem; padding: 1.5rem 1rem; border: 1px solid #dcd8d1; border-radius: 10px; background: #fff; }
.soccer-cleaning .cleaning-icon { width: 1.8rem; height: 1.8rem; fill: none; stroke: #c8102e; stroke-width: 1.8; stroke-linecap: round; stroke-linejoin: round; }
.soccer-cleaning .cleaning-icon .icon-gap { fill: #f7dfe3; stroke: #c8102e; }
.soccer-cleaning .cleaning-icon .icon-fill { fill: #c8102e; stroke: none; }
.soccer-cleaning .cleaning-card h2 { margin: 0; color: #34363a; font-family: Georgia, 'Times New Roman', serif; font-size: clamp(1.3rem, 1.9vw, 1.6rem); font-weight: 500; line-height: 1.15; }
.soccer-cleaning .mini-table { display: block; width: min(100%, 16.25rem); height: auto; }
.soccer-cleaning .table-base { fill: #eaf0f4; stroke: #c8d1d8; stroke-width: 1.2; }
.soccer-cleaning .table-grid { fill: none; stroke: #c4cdd4; stroke-width: 1.2; }
.soccer-cleaning .table-missing, .soccer-cleaning .table-highlight { fill: #f7dfe3; stroke: #e7b7c0; stroke-width: 0.8; }
.soccer-cleaning .table-duplicate-outline { fill: none; stroke: #c8102e; stroke-width: 1.8; stroke-dasharray: 5 4; }
.soccer-cleaning .table-label { fill: #34363a; font: 600 15px Inter, 'Aptos', Arial, sans-serif; }
.soccer-cleaning .cleaning-card p { margin: 0; color: #77736e; font-family: Inter, 'Aptos', Arial, sans-serif; font-size: clamp(1rem, 1.5vw, 1.15rem); line-height: 1.25; }
.soccer-cleaning .cleaning-takeaway { display: flex; align-items: center; justify-content: center; gap: 0.65rem; margin-top: 1.15rem; color: #34363a; font-family: Inter, 'Aptos', Arial, sans-serif; font-size: clamp(1.1rem, 1.7vw, 1.3rem); font-weight: 700; line-height: 1.2; }
.soccer-cleaning .cleaning-takeaway svg { flex: none; width: 1.5rem; height: 1.5rem; fill: none; stroke: #2e7d55; stroke-width: 2; stroke-linecap: round; stroke-linejoin: round; }
@media (max-width: 700px) {
  .soccer-cleaning .cleaning-slide { padding: 1.2rem; }
  .soccer-cleaning h1 { margin-bottom: 1rem; }
  .soccer-cleaning .cleaning-panels { gap: 0.5rem; }
  .soccer-cleaning .cleaning-card { min-height: 13rem; gap: 0.5rem; padding: 0.7rem 0.35rem; }
  .soccer-cleaning .cleaning-card h2 { font-size: 0.95rem; }
  .soccer-cleaning .mini-table { width: min(100%, 13rem); }
  .soccer-cleaning .cleaning-card p { font-size: 0.78rem; }
  .soccer-cleaning .cleaning-takeaway { margin-top: 0.6rem; font-size: 0.85rem; }
}
</style>
---
class: soccer-dataset-build
layout: default
---

<main class="dataset-build-slide">
  <h1>Constructing the Final Data Frame</h1>
  <section v-click.fade-in="1" class="build-stage season-stage" aria-label="Stacking Goalkeeping tables from three seasons">
    <div class="stage-copy">
      <h2>Combine the same table across seasons</h2>
      <p>Stack rows from each season</p>
    </div>
    <div class="season-flow">
      <div class="season-examples">
        <article class="season-example">
          <h3>2000/01 Goalkeeping</h3>
          <svg viewBox="0 0 210 46" aria-hidden="true"><rect class="mini-table" x="1" y="1" width="208" height="44" rx="3"/><path class="mini-grid" d="M1 17h208M1 32h208M70 1v44M140 1v44"/><text class="season-header" x="35" y="13">Saves</text><text class="season-header" x="105" y="13">Wins</text><text class="season-header" x="175" y="13">Losses</text><path class="mini-mark" d="M20 24h30M90 24h30M160 24h30M20 39h30M90 39h30M160 39h30"/></svg>
        </article>
        <article class="season-example">
          <h3>2001/02 Goalkeeping</h3>
          <svg viewBox="0 0 210 46" aria-hidden="true"><rect class="mini-table" x="1" y="1" width="208" height="44" rx="3"/><path class="mini-grid" d="M1 17h208M1 32h208M70 1v44M140 1v44"/><text class="season-header" x="35" y="13">Saves</text><text class="season-header" x="105" y="13">Wins</text><text class="season-header" x="175" y="13">Losses</text><path class="mini-mark" d="M20 24h30M90 24h30M160 24h30M20 39h30M90 39h30M160 39h30"/></svg>
        </article>
        <span class="season-ellipsis" aria-label="Intervening seasons">···</span>
        <article class="season-example">
          <h3>2024/25 Goalkeeping</h3>
          <svg viewBox="0 0 210 46" aria-hidden="true"><rect class="mini-table" x="1" y="1" width="208" height="44" rx="3"/><path class="mini-grid" d="M1 17h208M1 32h208M70 1v44M140 1v44"/><text class="season-header" x="35" y="13">Saves</text><text class="season-header" x="105" y="13">Wins</text><text class="season-header" x="175" y="13">Losses</text><path class="mini-mark" d="M20 24h30M90 24h30M160 24h30M20 39h30M90 39h30M160 39h30"/></svg>
        </article>
      </div>
      <svg class="flow-arrow horizontal-arrow" viewBox="0 0 54 34" aria-hidden="true"><path d="M3 17h45m-9-9 9 9-9 9"/></svg>
      <article class="combined-table">
        <h3>Combined Goalkeeping</h3>
        <svg class="combined-season-table" viewBox="0 0 210 154" aria-hidden="true"><rect class="mini-table" x="1" y="1" width="208" height="152" rx="3"/><path class="mini-grid" d="M1 17h208M1 34h208M1 51h208M1 68h208M1 85h208M1 102h208M1 119h208M1 136h208M1 153h208M70 1v152M140 1v152"/><text class="season-header" x="35" y="13">Saves</text><text class="season-header" x="105" y="13">Wins</text><text class="season-header" x="175" y="13">Losses</text><path class="mini-mark" d="M20 25h30M90 25h30M160 25h30M20 42h30M90 42h30M160 42h30M20 59h30M90 59h30M160 59h30M20 76h30M90 76h30M160 76h30M20 93h30M90 93h30M160 93h30M20 110h30M90 110h30M160 110h30M20 127h30M90 127h30M160 127h30M20 144h30M90 144h30M160 144h30"/></svg>
      </article>
    </div>
  </section>
  <section v-click.fade-in="2" class="build-stage category-stage" aria-label="Joining different statistical tables side by side">
    <div class="stage-copy">
      <h2>Combine cleaned tables with different statistics</h2>
      <p>Join columns for matching team-seasons</p>
    </div>
    <div class="category-flow">
      <div class="category-inputs">
        <article class="category-table goalkeeping-table"><h3>Goalkeeping</h3><svg viewBox="0 0 102 50" aria-hidden="true"><rect x="2" y="2" width="98" height="46" rx="3"/><path d="M2 17h98M2 32h98M35 2v46M68 2v46"/></svg></article>
        <article class="category-table shooting-table"><h3>Shooting</h3><svg viewBox="0 0 102 50" aria-hidden="true"><rect x="2" y="2" width="98" height="46" rx="3"/><path d="M2 17h98M2 32h98M35 2v46M68 2v46"/></svg></article>
        <article class="category-table other-table"><h3>Other tables</h3><svg viewBox="0 0 102 50" aria-hidden="true"><rect x="2" y="2" width="98" height="46" rx="3"/><path d="M2 17h98M2 32h98M35 2v46M68 2v46"/></svg></article>
      </div>
      <svg class="flow-arrow horizontal-arrow" viewBox="0 0 54 34" aria-hidden="true"><path d="M3 17h45m-9-9 9 9-9 9"/></svg>
      <article class="combined-wide-table">
        <h3>Combined data</h3>
        <svg viewBox="0 0 330 82" aria-hidden="true"><rect class="wide-base" x="2" y="2" width="326" height="78" rx="3"/><rect class="wide-goal" x="3" y="3" width="108" height="76" rx="2"/><rect class="wide-shot" x="112" y="3" width="108" height="76"/><rect class="wide-other" x="221" y="3" width="106" height="76" rx="2"/><path class="wide-grid" d="M2 21.5h326M2 41h326M2 60.5h326M38 2v78M74 2v78M110 2v78M146 2v78M182 2v78M218 2v78M256 2v78M292 2v78"/></svg>
      </article>
    </div>
  </section>
  <section v-click.fade-in="3" class="dataset-summary" aria-label="Final dataset size">
    <div><strong>25</strong><span>Seasons</span></div>
    <div><strong>500</strong><span>Team-Seasons</span></div>
    <div><strong>40</strong><span>Numerical Variables</span></div>
  </section>
</main>

<style>
.soccer-dataset-build { color: #282a2d; background: #f7f5f0; }
.soccer-dataset-build .dataset-build-slide { box-sizing: border-box; width: 100%; height: 100%; display: grid; grid-template-rows: auto minmax(14rem, 1.4fr) minmax(10rem, 0.72fr) auto; padding: 0.65rem 2.1rem 0.55rem; }
.soccer-dataset-build h1 { min-width: 0; margin: 0 0 0.15rem; text-align: center; color: #282a2d; font-family: Georgia, 'Times New Roman', serif; font-size: clamp(1.8rem, 3vw, 2.35rem); font-weight: 500; letter-spacing: -0.035em; line-height: 1.08; }
.soccer-dataset-build .build-stage { box-sizing: border-box; min-height: 0; display: grid; grid-template-columns: 13rem minmax(0, 1fr); align-items: center; gap: 0.9rem; padding: 0.25rem 0; border-bottom: 1px solid #e2ded7; }
.soccer-dataset-build .season-stage { position: relative; min-height: 14rem; border-bottom: 0; }
.soccer-dataset-build .season-stage::after { content: ""; position: absolute; right: 0; bottom: -1.1rem; left: 0; border-bottom: 1px solid #e2ded7; pointer-events: none; }
.soccer-dataset-build .category-stage { min-height: 10rem; }
.soccer-dataset-build .stage-copy { min-width: 0; }
.soccer-dataset-build .stage-copy h2 { margin: 0; color: #34363a; font-family: Georgia, 'Times New Roman', serif; font-size: clamp(1.05rem, 1.5vw, 1.3rem); font-weight: 500; line-height: 1.15; }
.soccer-dataset-build .stage-copy p { margin: 0.28rem 0 0; color: #77736e; font-family: Inter, 'Aptos', Arial, sans-serif; font-size: clamp(0.82rem, 1.05vw, 0.94rem); line-height: 1.2; }
.soccer-dataset-build .season-flow { min-width: 0; min-height: 0; display: grid; grid-template-columns: minmax(13rem, 1fr) 2rem minmax(10rem, 0.72fr); align-items: center; gap: 0.4rem; transform: translateY(16px); }
.soccer-dataset-build .season-examples { min-width: 0; display: flex; flex-direction: column; align-items: center; justify-content: center; gap: 0; }
.soccer-dataset-build .season-example { min-width: 0; width: min(100%, 14.5rem); text-align: center; }
.soccer-dataset-build .season-example h3,.soccer-dataset-build .combined-table h3,.soccer-dataset-build .combined-wide-table h3 { margin: 0; color: #4c4a46; font-family: Inter, 'Aptos', Arial, sans-serif; font-size: clamp(0.72rem, 1vw, 0.84rem); line-height: 1.05; }
.soccer-dataset-build .season-example svg { display: block; width: 100%; margin: 0 auto; }
.soccer-dataset-build .season-header { fill: #4c4a46; font-family: Inter, 'Aptos', Arial, sans-serif; font-size: 11px; font-weight: 600; text-anchor: middle; }
.soccer-dataset-build .season-ellipsis { flex: 0 0 auto; color: #aaa69e; font-size: 0.9rem; letter-spacing: 0.2em; line-height: 0.8; }
.soccer-dataset-build .mini-table { fill: #fbfaf7; stroke: #aaa69e; stroke-width: 1.4; }
.soccer-dataset-build .mini-grid { fill: none; stroke: #c8c4bc; stroke-width: 1; }
.soccer-dataset-build .mini-mark { fill: none; stroke: #929aa0; stroke-linecap: round; stroke-width: 1.4; }
.soccer-dataset-build .flow-arrow { display: block; fill: none; stroke: #c8102e; stroke-linecap: round; stroke-linejoin: round; stroke-width: 2; }
.soccer-dataset-build .horizontal-arrow { width: 100%; height: 2.1rem; }
.soccer-dataset-build .combined-table { text-align: center; }
.soccer-dataset-build .combined-table h3,.soccer-dataset-build .combined-wide-table h3 { margin-bottom: 0.25rem; font-family: Georgia, 'Times New Roman', serif; font-size: clamp(0.88rem, 1.2vw, 1rem); font-weight: 500; }
.soccer-dataset-build .combined-season-table { display: block; width: min(100%, 11rem); max-height: 9.5rem; margin: 0 auto; }
.soccer-dataset-build .category-flow { min-width: 0; min-height: 0; display: grid; grid-template-columns: minmax(0, 1.45fr) 2.3rem minmax(12rem, 1fr); align-items: center; gap: 0.45rem; }
.soccer-dataset-build .category-inputs { min-width: 0; display: grid; grid-template-columns: repeat(3, minmax(0, 1fr)); align-items: center; gap: 0.4rem; }
.soccer-dataset-build .category-table { min-width: 0; display: flex; flex-direction: column; align-items: center; gap: 0.28rem; }
.soccer-dataset-build .category-table h3 { margin: 0; color: #4c4a46; font-family: Inter, 'Aptos', Arial, sans-serif; font-size: clamp(0.72rem, 1vw, 0.84rem); font-weight: 500; text-align: center; line-height: 1.1; }
.soccer-dataset-build .category-table svg { display: block; width: 100%; max-width: 7.4rem; }
.soccer-dataset-build .category-table rect { stroke-width: 1.4; }
.soccer-dataset-build .category-table path { fill: none; stroke-width: 1; }
.soccer-dataset-build .goalkeeping-table rect { fill: rgba(200, 16, 46, 0.08); stroke: #c8102e; }
.soccer-dataset-build .goalkeeping-table path { stroke: #c8102e; }
.soccer-dataset-build .shooting-table rect { fill: rgba(73, 112, 137, 0.1); stroke: #497089; }
.soccer-dataset-build .shooting-table path { stroke: #497089; }
.soccer-dataset-build .other-table rect { fill: rgba(102, 130, 104, 0.1); stroke: #668268; }
.soccer-dataset-build .other-table path { stroke: #668268; }
.soccer-dataset-build .combined-wide-table { min-width: 0; text-align: center; }
.soccer-dataset-build .combined-wide-table svg { display: block; width: 100%; max-width: 20rem; margin: 0 auto; }
.soccer-dataset-build .wide-base { fill: #fbfaf7; stroke: #aaa69e; stroke-width: 1.4; }
.soccer-dataset-build .wide-goal { fill: rgba(200, 16, 46, 0.11); }
.soccer-dataset-build .wide-shot { fill: rgba(73, 112, 137, 0.12); }
.soccer-dataset-build .wide-other { fill: rgba(102, 130, 104, 0.12); }
.soccer-dataset-build .wide-grid { fill: none; stroke: #bdb9b1; stroke-width: 1; }
.soccer-dataset-build .dataset-summary { display: grid; grid-template-columns: repeat(3, minmax(0, 1fr)); align-items: center; width: min(100%, 880px); margin: 0.2rem auto 0; padding-top: 0.2rem; border-top: 1px solid #e2ded7; text-align: center; }
.soccer-dataset-build .dataset-summary div { display: flex; flex-direction: column; align-items: center; gap: 0.08rem; }
 .soccer-dataset-build .dataset-summary strong { color: #c8102e; font-family: Georgia, 'Times New Roman', serif; font-size: clamp(1.6rem, 2.8vw, 2.2rem); font-weight: 500; line-height: 1; }
.soccer-dataset-build .dataset-summary span { color: #4c4a46; font-family: Inter, 'Aptos', Arial, sans-serif; font-size: clamp(0.72rem, 1.05vw, 0.9rem); line-height: 1.15; }
@media (max-width: 700px) { .soccer-dataset-build .dataset-build-slide { grid-template-rows: auto minmax(12rem, 1.45fr) minmax(8.5rem, 0.72fr) auto; padding: 0.5rem 0.8rem 0.4rem; } .soccer-dataset-build .build-stage { grid-template-columns: 7.5rem minmax(0, 1fr); gap: 0.35rem; } .soccer-dataset-build .season-flow { grid-template-columns: minmax(9rem, 1fr) 1.25rem minmax(5.5rem, 0.65fr); gap: 0.15rem; } .soccer-dataset-build .season-example { width: min(100%, 12.5rem); } .soccer-dataset-build .season-header { font-size: 10px; } .soccer-dataset-build .combined-season-table { width: min(100%, 8rem); max-height: 8rem; } .soccer-dataset-build .category-flow { grid-template-columns: minmax(0, 1.35fr) 1.4rem minmax(6.5rem, 1fr); gap: 0.2rem; } .soccer-dataset-build .category-inputs { gap: 0.16rem; } .soccer-dataset-build .category-table { gap: 0.18rem; } .soccer-dataset-build .category-table h3 { font-size: 0.62rem; } .soccer-dataset-build .category-table svg { width: min(100%, 4.5rem); } .soccer-dataset-build .stage-copy h2 { font-size: 0.9rem; } .soccer-dataset-build .stage-copy p { font-size: 0.68rem; } .soccer-dataset-build .dataset-summary strong { font-size: 1.35rem; } .soccer-dataset-build .dataset-summary span { font-size: 0.58rem; } }
</style>
---
class: soccer-similarity-intro
layout: default
---

<main class="similarity-intro-slide">
  <h1>How Do We Measure Similarity?</h1>
  <section class="comparison-data" aria-label="Illustrative team-season data">
    <p class="data-note">Illustrative values</p>
    <table>
      <thead><tr><th scope="col">Team-Season</th><th scope="col">Goals</th><th scope="col">Shots</th><th scope="col">Passes</th></tr></thead>
      <tbody><tr><th scope="row">Team A</th><td>70</td><td>180</td><td>450</td></tr><tr><th scope="row">Team B</th><td>68</td><td>183</td><td>444</td></tr></tbody>
    </table>
  </section>
  <section class="variable-comparisons" aria-label="Team A minus Team B for each statistic">
    <article v-click.fade-in="1" class="comparison-panel">
      <h2>Goals</h2>
      <p class="calculation">70 − 68 =</p>
      <p class="difference">2</p>
    </article>
    <article v-click.fade-in="2" class="comparison-panel">
      <h2>Shots</h2>
      <p class="calculation">180 − 183 =</p>
      <p class="difference">−3</p>
    </article>
    <article v-click.fade-in="3" class="comparison-panel">
      <h2>Passes</h2>
      <p class="calculation">450 − 444 =</p>
      <p class="difference">6</p>
    </article>
  </section>
</main>

<style>
.soccer-similarity-intro { color: #282a2d; background: #f7f5f0; }
.soccer-similarity-intro .similarity-intro-slide { box-sizing: border-box; width: 100%; height: 100%; display: flex; flex-direction: column; align-items: center; padding: 0.9rem 2.5rem 0.9rem; }
.soccer-similarity-intro h1 { margin: 0; color: #282a2d; font-family: Georgia, 'Times New Roman', serif; font-size: clamp(2.15rem, 3.8vw, 2.9rem); font-weight: 500; letter-spacing: -0.035em; line-height: 1.1; text-align: center; }
.soccer-similarity-intro .comparison-data { width: min(100%, 850px); margin-top: clamp(1.8rem, 4.5vh, 2.7rem); }
.soccer-similarity-intro .data-note { margin: 0 0 0.45rem; color: #77736e; font: 500 clamp(0.82rem, 1.15vw, 0.95rem)/1.2 Inter, 'Aptos', Arial, sans-serif; letter-spacing: 0.015em; text-align: right; }
.soccer-similarity-intro table { width: 100%; border-collapse: collapse; table-layout: fixed; overflow: hidden; border: 1px solid #d8d3ca; border-top: 2px solid #c8102e; background: #fff; font-family: Inter, 'Aptos', Arial, sans-serif; }
.soccer-similarity-intro th,.soccer-similarity-intro td { padding: 1rem 1rem; border: 1px solid #e1ddd5; text-align: center; font-size: clamp(1.05rem, 1.5vw, 1.25rem); line-height: 1.2; }
.soccer-similarity-intro thead th { color: #34363a; background: #f1efea; font-weight: 600; }
.soccer-similarity-intro thead th:first-child,.soccer-similarity-intro tbody th { width: 31%; text-align: left; }
.soccer-similarity-intro tbody th { color: #34363a; background: #fbfaf7; font-weight: 600; }
.soccer-similarity-intro td { color: #34363a; font-variant-numeric: tabular-nums; }
.soccer-similarity-intro .variable-comparisons { width: min(100%, 1000px); margin-top: clamp(2rem, 5.5vh, 3.2rem); display: grid; grid-template-columns: repeat(3, minmax(0, 1fr)); gap: clamp(1rem, 2.2vw, 2rem); }
.soccer-similarity-intro .comparison-panel { min-width: 0; box-sizing: border-box; min-height: 12.5rem; padding: 1.1rem 0.8rem 1.25rem; border: 1px solid #e0dcd4; border-top: 2px solid #c8102e; background: rgba(255,255,255,0.72); text-align: center; }
.soccer-similarity-intro .comparison-panel h2 { margin: 0 0 0.8rem; color: #34363a; font-family: Georgia, 'Times New Roman', serif; font-size: clamp(1.2rem, 1.7vw, 1.45rem); font-weight: 500; line-height: 1.15; }
.soccer-similarity-intro .calculation { margin: 0; color: #5d5b57; font-family: Inter, 'Aptos', Arial, sans-serif; font-size: clamp(1.1rem, 1.65vw, 1.35rem); font-variant-numeric: tabular-nums; line-height: 1.25; }
.soccer-similarity-intro .difference { margin: 0.25rem 0 0; color: #a30f28; font-family: Georgia, 'Times New Roman', serif; font-size: clamp(1.8rem, 2.5vw, 2.2rem); font-weight: 600; font-variant-numeric: tabular-nums; line-height: 1; }
@media (max-width: 700px) {
  .soccer-similarity-intro .similarity-intro-slide { padding: 1rem 1.2rem 0.7rem; }
  .soccer-similarity-intro h1 { font-size: 1.8rem; }
  .soccer-similarity-intro .comparison-data { margin-top: 2.2rem; }
  .soccer-similarity-intro th,.soccer-similarity-intro td { padding: 0.72rem 0.35rem; font-size: 0.88rem; }
  .soccer-similarity-intro .variable-comparisons { margin-top: 2.2rem; gap: 0.5rem; }
  .soccer-similarity-intro .comparison-panel { min-height: 10.5rem; padding: 0.8rem 0.3rem; }
  .soccer-similarity-intro .comparison-panel h2 { font-size: 0.95rem; margin-bottom: 0.6rem; }
  .soccer-similarity-intro .calculation { font-size: 0.82rem; }
  .soccer-similarity-intro .difference { font-size: 1.55rem; }
}
</style>

---
class: soccer-distance
layout: default
---

<script setup>
import katex from 'katex'

const distanceMath = {
  differences: katex.renderToString('2,\\;-3,\\;6', { throwOnError: false }),
  squares: [
    katex.renderToString('2^2 = 4', { throwOnError: false }),
    katex.renderToString('(-3)^2 = 9', { throwOnError: false }),
    katex.renderToString('6^2 = 36', { throwOnError: false }),
  ],
  sum: katex.renderToString('4 + 9 + 36 = 49', { throwOnError: false }),
  root: katex.renderToString('\\sqrt{49}=\\textcolor{#a30f28}{\\large 7}', { throwOnError: false }),
}
</script>

<main class="distance-slide">
  <h1>From Differences to Distance</h1>
  <section class="distance-steps" aria-label="Combining the three differences into one distance">
    <article v-click.fade-in="1" class="distance-step">
      <span class="step-number">01</span>
      <h2>Differences</h2>
      <p class="step-math" v-html="distanceMath.differences"></p>
    </article>
    <div v-click.fade-in="2" class="step-arrow" aria-hidden="true">→</div>
    <article v-click.fade-in="2" class="distance-step">
      <span class="step-number">02</span>
      <h2>Square each</h2>
      <div class="step-math stacked-math"><span v-html="distanceMath.squares[0]"></span><span v-html="distanceMath.squares[1]"></span><span v-html="distanceMath.squares[2]"></span></div>
      <p class="positive-note">Each difference adds a positive amount</p>
    </article>
    <div v-click.fade-in="3" class="step-arrow" aria-hidden="true">→</div>
    <article v-click.fade-in="3" class="distance-step">
      <span class="step-number">03</span>
      <h2>Add</h2>
      <p class="step-math" v-html="distanceMath.sum"></p>
    </article>
    <div v-click.fade-in="4" class="step-arrow" aria-hidden="true">→</div>
    <article v-click.fade-in="4" class="distance-step final-step">
      <span class="step-number">04</span>
      <h2>Square root</h2>
      <p class="step-math root-equation" v-html="distanceMath.root"></p>
    </article>
  </section>
  <p v-click.fade-in="5" class="distance-takeaway">Take the square root to return to the original distance scale</p>
</main>

<style>
.soccer-distance { color: #282a2d; background: #f7f5f0; }
.soccer-distance .distance-slide { box-sizing: border-box; width: 100%; height: 100%; display: flex; flex-direction: column; align-items: center; padding: 0.85rem 2.2rem 0.7rem; }
.soccer-distance h1 { margin: 0; color: #282a2d; font-family: Georgia, 'Times New Roman', serif; font-size: clamp(2.1rem, 3.5vw, 2.7rem); font-weight: 500; letter-spacing: -0.035em; line-height: 1.1; text-align: center; }
.soccer-distance .distance-steps { width: min(100%, 1180px); flex: 1; min-height: 0; display: grid; grid-template-columns: minmax(0, 1.12fr) 1.8rem minmax(0, 1.45fr) 1.8rem minmax(0, 1.15fr) 1.8rem minmax(0, 1.12fr); align-items: center; gap: clamp(0.3rem, 0.8vw, 0.7rem); padding: 1.4rem 0 0.9rem; }
.soccer-distance .distance-step { box-sizing: border-box; min-width: 0; min-height: 14rem; padding: 1.15rem 0.8rem; border: 1px solid #e0dcd4; border-top: 2px solid #c8102e; background: rgba(255,255,255,0.72); text-align: center; display: flex; flex-direction: column; justify-content: center; align-items: center; }
.soccer-distance .step-number { color: #a30f28; font: 600 0.82rem/1 Inter, 'Aptos', Arial, sans-serif; letter-spacing: 0.08em; }
.soccer-distance .distance-step h2 { margin: 0.55rem 0 1.1rem; color: #34363a; font-family: Georgia, 'Times New Roman', serif; font-size: clamp(1.05rem, 1.45vw, 1.3rem); font-weight: 500; line-height: 1.15; }
.soccer-distance .step-math { margin: 0; color: #34363a; font: 500 clamp(1rem, 1.35vw, 1.15rem)/1.3 Inter, 'Aptos', Arial, sans-serif; font-variant-numeric: tabular-nums; text-align: center; white-space: nowrap; }
.soccer-distance :deep(.step-math .katex) { font-size: 1em; }
.soccer-distance .stacked-math { display: grid; justify-items: center; gap: 0.3rem; }
.soccer-distance .positive-note { margin: 0.8rem 0 0; color: #77736e; font: 400 clamp(0.68rem, 0.9vw, 0.78rem)/1.3 Inter, 'Aptos', Arial, sans-serif; }
.soccer-distance .step-arrow { color: #c8102e; font: 300 clamp(1.2rem, 2vw, 1.7rem)/1 Inter, 'Aptos', Arial, sans-serif; text-align: center; }
.soccer-distance .distance-takeaway { box-sizing: border-box; width: min(100%, 960px); min-height: 3.7rem; margin: 0 0 0.2rem; padding: 0.9rem 1rem; border-top: 1px solid #e0dcd4; color: #34363a; font: 600 clamp(1rem, 1.4vw, 1.2rem)/1.3 Inter, 'Aptos', Arial, sans-serif; text-align: center; }
@media (max-width: 700px) {
  .soccer-distance .distance-slide { padding: 0.8rem 0.65rem 0.55rem; }
  .soccer-distance h1 { font-size: 1.65rem; }
  .soccer-distance .distance-steps { grid-template-columns: 1fr; gap: 0.35rem; padding: 0.75rem 0 0.45rem; }
  .soccer-distance .distance-step { min-height: 0; padding: 0.45rem; }
  .soccer-distance .distance-step h2 { margin: 0.2rem 0 0.35rem; }
  .soccer-distance .step-arrow { transform: rotate(90deg); line-height: 0.8; }
  .soccer-distance .positive-note { margin-top: 0.35rem; }
  .soccer-distance .distance-takeaway { min-height: 0; padding: 0.55rem 0.35rem; font-size: 0.8rem; }
}
</style>

---
class: soccer-contribution
layout: default
---

<main class="contribution-slide">
  <h1>Does Every Difference Matter Equally?</h1>
  <section class="team-comparison" aria-label="Team A and Team B are seven units apart">
    <div class="team-card"><span class="team-dot"></span><span>Team A</span></div>
    <div class="distance-connector">
      <strong>7</strong>
      <svg viewBox="0 0 520 28" role="img" aria-label="Double-ended distance arrow">
        <defs><marker id="distance-arrow-start" markerWidth="8" markerHeight="8" refX="2" refY="4" orient="auto"><path d="M8 0 0 4 8 8" fill="none" stroke="#a7aeb5" stroke-width="1.4" /></marker><marker id="distance-arrow-end" markerWidth="8" markerHeight="8" refX="6" refY="4" orient="auto"><path d="M0 0 8 4 0 8" fill="none" stroke="#a7aeb5" stroke-width="1.4" /></marker></defs>
        <line x1="8" y1="14" x2="512" y2="14" stroke="#a7aeb5" stroke-width="1.8" marker-start="url(#distance-arrow-start)" marker-end="url(#distance-arrow-end)" />
      </svg>
      <span class="distance-label">Distance = 7</span>
    </div>
    <div class="team-card"><span class="team-dot"></span><span>Team B</span></div>
  </section>
  <section v-click.fade-in="1" class="contribution-chart" aria-label="Contributions to the squared distance">
    <h2>Contributions to the squared distance</h2>
    <div class="chart-row">
      <span class="stat-label">Goals</span>
      <div class="bar-track"><div class="bar-fill muted-bar" style="width: 8.9%"></div><span class="bar-value" style="left: calc(8.9% + 0.45rem)">4</span></div>
    </div>
    <div class="chart-row">
      <span class="stat-label">Shots</span>
      <div class="bar-track"><div class="bar-fill muted-bar" style="width: 20%"></div><span class="bar-value" style="left: calc(20% + 0.45rem)">9</span></div>
    </div>
    <div class="chart-row">
      <span class="stat-label">Passes</span>
      <div class="bar-track">
        <div class="bar-fill muted-bar" style="width: 80%"></div>
        <div v-click.fade-in="2" class="bar-fill passes-bar" style="width: 80%"></div>
        <span class="bar-value" style="left: calc(80% + 0.45rem)">36</span>
      </div>
    </div>
  </section>
  <p v-click.fade-in="3" class="contribution-question">Is passing really that much more important?</p>
</main>

<style>
.soccer-contribution { color: #282a2d; background: #f7f5f0; }
.soccer-contribution .contribution-slide { box-sizing: border-box; width: 100%; height: 100%; display: grid; grid-template-rows: auto 9.5rem minmax(0, 1fr) auto; align-items: center; justify-items: center; padding: 0.8rem 2.4rem 0.65rem; }
.soccer-contribution h1 { margin: 0; color: #282a2d; font-family: Georgia, 'Times New Roman', serif; font-size: clamp(2rem, 3.3vw, 2.65rem); font-weight: 500; letter-spacing: -0.035em; line-height: 1.1; text-align: center; }
.soccer-contribution .team-comparison { display: grid; grid-template-columns: minmax(8rem, 1fr) minmax(16rem, 2.6fr) minmax(8rem, 1fr); align-items: center; gap: clamp(1rem, 2vw, 1.8rem); width: min(100%, 790px); }
.soccer-contribution .team-card { display: flex; align-items: center; justify-content: center; gap: 0.55rem; padding: 0.8rem 1rem; border: 1px solid #e0dcd4; background: rgba(255,255,255,0.72); color: #34363a; font: 600 clamp(0.95rem, 1.3vw, 1.1rem)/1.2 Inter, 'Aptos', Arial, sans-serif; }
.soccer-contribution .team-dot { width: 0.72rem; height: 0.72rem; flex: 0 0 auto; border-radius: 50%; background: #497089; }
.soccer-contribution .distance-connector { display: flex; flex-direction: column; align-items: center; gap: 0.12rem; }
.soccer-contribution .distance-connector strong { color: #34363a; font: 600 clamp(1.7rem, 2.5vw, 2rem)/1 Georgia, 'Times New Roman', serif; }
.soccer-contribution .distance-connector svg { display: block; width: 100%; height: 1.15rem; overflow: visible; }
.soccer-contribution .distance-label { color: #5d5b57; font: 500 clamp(0.8rem, 1.05vw, 0.92rem)/1.2 Inter, 'Aptos', Arial, sans-serif; }
.soccer-contribution .contribution-chart { box-sizing: border-box; width: min(100%, 820px); align-self: center; padding: 0.75rem 1.15rem 0.9rem; border: 1px solid #e0dcd4; border-top: 2px solid #c8102e; background: rgba(255,255,255,0.58); }
.soccer-contribution .contribution-chart h2 { margin: 0 0 0.55rem; color: #5d5b57; font: 500 clamp(0.85rem, 1.1vw, 0.98rem)/1.2 Inter, 'Aptos', Arial, sans-serif; text-align: center; }
.soccer-contribution .chart-row { display: grid; grid-template-columns: 6rem minmax(0, 1fr); align-items: center; gap: 0.9rem; min-height: 2.45rem; }
.soccer-contribution .stat-label { color: #34363a; font: 500 clamp(0.95rem, 1.2vw, 1.05rem)/1.2 Inter, 'Aptos', Arial, sans-serif; }
.soccer-contribution .bar-track { position: relative; height: 1.35rem; }
.soccer-contribution .bar-fill { position: absolute; top: 0; left: 0; height: 100%; border-radius: 2px; transition: background-color 260ms ease, opacity 260ms ease; }
.soccer-contribution .muted-bar { background: #8099aa; }
.soccer-contribution .passes-bar { background: #c8102e; }
.soccer-contribution .bar-value { position: absolute; top: 50%; color: #34363a; font: 600 clamp(0.9rem, 1.15vw, 1rem)/1 Inter, 'Aptos', Arial, sans-serif; font-variant-numeric: tabular-nums; transform: translateY(-50%); }
.soccer-contribution .contribution-question { align-self: end; margin: 0.45rem 0 0.15rem; color: #34363a; font: 500 clamp(1.3rem, 2.05vw, 1.65rem)/1.2 Georgia, 'Times New Roman', serif; text-align: center; }
@media (max-width: 700px) {
  .soccer-contribution .contribution-slide { grid-template-rows: auto 7rem minmax(0, 1fr) auto; padding: 0.7rem 0.85rem 0.5rem; }
  .soccer-contribution h1 { font-size: 1.55rem; }
  .soccer-contribution .team-comparison { grid-template-columns: 5rem minmax(0, 1fr) 5rem; gap: 0.35rem; }
  .soccer-contribution .team-card { flex-direction: column; gap: 0.25rem; padding: 0.45rem 0.2rem; font-size: 0.68rem; }
  .soccer-contribution .team-dot { width: 0.55rem; height: 0.55rem; }
  .soccer-contribution .contribution-chart { padding: 0.5rem 0.55rem; }
  .soccer-contribution .chart-row { grid-template-columns: 3.7rem minmax(0, 1fr); gap: 0.35rem; min-height: 2rem; }
  .soccer-contribution .stat-label,.soccer-contribution .bar-value { font-size: 0.75rem; }
  .soccer-contribution .bar-track { height: 1.05rem; }
  .soccer-contribution .contribution-question { margin-top: 0.25rem; font-size: 1rem; }
}
</style>

---
class: soccer-standardization
layout: default
---

<main class="standardization-slide">
  <h1>Putting Statistics on Equal Footing</h1>
  <section class="standardization-flow" aria-label="Moving statistics from different raw scales to a common scale">
    <div class="scale-group original-group">
      <h2>Original scales</h2>
      <div class="raw-row"><span class="variable-label">Goals</span><span class="scale-word">Tens</span><span class="raw-track"><i style="width: 30%"></i></span></div>
      <div class="raw-row"><span class="variable-label">Shots</span><span class="scale-word">Hundreds</span><span class="raw-track"><i style="width: 62%"></i></span></div>
      <div class="raw-row"><span class="variable-label">Passes</span><span class="scale-word">Thousands</span><span class="raw-track"><i style="width: 100%"></i></span></div>
    </div>
    <div v-click.fade-in="1" class="process-arrow" aria-hidden="true">→</div>
    <div v-click.fade-in="1" class="standardization-box">Standardization</div>
    <div v-click.fade-in="1" class="process-arrow" aria-hidden="true">→</div>
    <div v-click.fade-in="2" class="scale-group common-group">
      <h2>Common scale</h2>
      <div class="common-row"><span class="variable-label">Goals</span><div class="numberline"><div class="tick-labels"><span>−3</span><span>−2</span><span>−1</span><span>0</span><span>1</span><span>2</span><span>3</span></div><i class="standardized-marker" style="left: 32.86%"></i></div></div>
      <div class="common-row"><span class="variable-label">Shots</span><div class="numberline"><div class="tick-labels"><span>−3</span><span>−2</span><span>−1</span><span>0</span><span>1</span><span>2</span><span>3</span></div><i class="standardized-marker" style="left: 52.86%"></i></div></div>
      <div class="common-row"><span class="variable-label">Passes</span><div class="numberline"><div class="tick-labels"><span>−3</span><span>−2</span><span>−1</span><span>0</span><span>1</span><span>2</span><span>3</span></div><i class="standardized-marker" style="left: 70%"></i></div></div>
    </div>
  </section>
  <p v-click.fade-in="3" class="standardization-takeaway">All statistics on the same scale!</p>
</main>

<style>
.soccer-standardization { color: #282a2d; background: #f7f5f0; }
.soccer-standardization .standardization-slide { box-sizing: border-box; width: 100%; height: 100%; display: grid; grid-template-rows: auto minmax(0, 1fr) auto; justify-items: center; align-items: center; padding: 0.9rem 2rem 0.65rem; }
.soccer-standardization h1 { margin: 0; color: #282a2d; font-family: Georgia, 'Times New Roman', serif; font-size: clamp(2rem, 3.3vw, 2.65rem); font-weight: 500; letter-spacing: -0.035em; line-height: 1.1; text-align: center; }
.soccer-standardization .standardization-flow { width: min(100%, 1160px); display: grid; grid-template-columns: minmax(0, 1.15fr) 1.4rem minmax(7.5rem, 0.7fr) 1.4rem minmax(0, 1.45fr); align-items: center; gap: clamp(0.45rem, 1vw, 0.85rem); }
.soccer-standardization .scale-group { min-width: 0; padding: 0; border: 0; background: transparent; }
.soccer-standardization .scale-group h2 { margin: 0 0 0.85rem; color: #5d5b57; font: 500 clamp(0.88rem, 1.15vw, 1rem)/1.2 Inter, 'Aptos', Arial, sans-serif; text-align: left; }
.soccer-standardization .raw-row,.soccer-standardization .common-row { display: grid; grid-template-columns: minmax(3.8rem, 0.75fr) minmax(0, 1.45fr) minmax(0, 1.35fr); align-items: center; gap: 0.45rem; min-height: 2.55rem; }
.soccer-standardization .variable-label { color: #34363a; font: 500 clamp(0.86rem, 1.12vw, 1rem)/1.15 Inter, 'Aptos', Arial, sans-serif; }
.soccer-standardization .scale-word { color: #77736e; font: 400 clamp(0.72rem, 0.95vw, 0.84rem)/1.15 Inter, 'Aptos', Arial, sans-serif; }
.soccer-standardization .raw-track { display: block; height: 0.62rem; background: #e7e9e9; }
.soccer-standardization .raw-track i { display: block; height: 100%; background: #8099aa; }
.soccer-standardization .process-arrow { color: #c8102e; font: 300 clamp(1.25rem, 2.1vw, 1.75rem)/1 Inter, 'Aptos', Arial, sans-serif; text-align: center; }
.soccer-standardization .standardization-box { box-sizing: border-box; display: flex; align-items: center; justify-content: center; justify-self: center; width: min(100%, 9rem); min-height: 8.5rem; padding: 0.8rem; border-top: 3px solid #c8102e; background: #34363a; color: #fbfaf7; font: 500 clamp(0.9rem, 1.15vw, 1.02rem)/1.25 Georgia, 'Times New Roman', serif; text-align: center; }
.soccer-standardization .common-row { grid-template-columns: minmax(3.4rem, 0.7fr) minmax(0, 2.3fr); gap: 0.45rem; min-height: 2.8rem; }
.soccer-standardization .numberline { position: relative; min-width: 0; padding-top: 0.22rem; }
.soccer-standardization .numberline::before { position: absolute; top: 0.38rem; left: 7.14%; right: 7.14%; border-top: 1px solid #9ca3aa; content: ''; }
.soccer-standardization .tick-labels { position: relative; display: grid; grid-template-columns: repeat(7, minmax(0, 1fr)); color: #4c4a46; font: 400 clamp(0.68rem, 0.9vw, 0.8rem)/1.2 Inter, 'Aptos', Arial, sans-serif; font-variant-numeric: tabular-nums; text-align: center; }
.soccer-standardization .tick-labels span { position: relative; padding-top: 1.5rem; }
.soccer-standardization .tick-labels span::before { position: absolute; top: 0; left: 50%; height: 0.5rem; border-left: 1px solid #9ca3aa; content: ''; }
.soccer-standardization .tick-labels span:nth-child(4)::before { height: 0.62rem; border-color: #c8102e; }
.soccer-standardization .standardized-marker { position: absolute; z-index: 2; top: 0; display: block; width: 4px; height: 22px; border-radius: 2px; background: #c8102e; transform: translateX(-50%); }
.soccer-standardization .standardization-takeaway { align-self: end; margin: 0 0 0.2rem; padding: 0.55rem 0.8rem 0.35rem; border-top: 1px solid #e0dcd4; color: #34363a; font: 500 clamp(1.15rem, 1.7vw, 1.42rem)/1.2 Georgia, 'Times New Roman', serif; text-align: center; }
@media (max-width: 700px) {
  .soccer-standardization .standardization-slide { padding: 0.7rem 0.8rem 0.45rem; }
  .soccer-standardization h1 { font-size: 1.55rem; }
  .soccer-standardization .standardization-flow { grid-template-columns: minmax(0, 1fr); gap: 0.12rem; padding: 0.35rem 0 0.15rem; }
  .soccer-standardization .scale-group { padding: 0; }
  .soccer-standardization .scale-group h2 { margin-bottom: 0.3rem; font-size: 0.72rem; text-align: left; }
  .soccer-standardization .raw-row { min-height: 1.55rem; }
  .soccer-standardization .common-row { min-height: 2.5rem; }
  .soccer-standardization .raw-row { grid-template-columns: 3.8rem 5.1rem minmax(0, 1fr); }
  .soccer-standardization .common-row { grid-template-columns: 3.8rem minmax(0, 1fr); }
  .soccer-standardization .variable-label { font-size: 0.72rem; }
  .soccer-standardization .scale-word,.soccer-standardization .tick-labels { font-size: 0.62rem; }
  .soccer-standardization .raw-track { height: 0.42rem; }
  .soccer-standardization .process-arrow { transform: rotate(90deg); font-size: 1rem; line-height: 0.9; }
  .soccer-standardization .standardization-box { width: min(100%, 8rem); min-height: 2.1rem; padding: 0.25rem; font-size: 0.76rem; }
  .soccer-standardization .numberline { padding-top: 0.15rem; }
  .soccer-standardization .numberline::before { top: 0.28rem; }
  .soccer-standardization .tick-labels span { padding-top: 1.35rem; }
  .soccer-standardization .tick-labels span::before { height: 0.4rem; }
  .soccer-standardization .standardization-takeaway { padding: 0.35rem 0.25rem 0.2rem; font-size: 0.95rem; }
}
</style>

---
class: soccer-correlation
layout: default
---

<main class="correlation-slide">
  <h1>But There’s Still One More Problem...</h1>
  <div class="correlation-plot-wrap">
    <svg class="correlation-plot" viewBox="0 0 800 440" role="img" aria-label="Scatterplot with Shots on the horizontal axis and Shots on Target on the vertical axis">
      <g class="plot-axes" fill="none" stroke="#77736e" stroke-width="2">
        <line x1="100" y1="350" x2="750" y2="350" />
        <line x1="100" y1="350" x2="100" y2="30" />
      </g>
      <g class="plot-ticks" fill="none" stroke="#a7a39c" stroke-width="1.5">
        <line x1="100" y1="350" x2="100" y2="358" /><line x1="208" y1="350" x2="208" y2="358" /><line x1="317" y1="350" x2="317" y2="358" /><line x1="425" y1="350" x2="425" y2="358" /><line x1="533" y1="350" x2="533" y2="358" /><line x1="642" y1="350" x2="642" y2="358" /><line x1="750" y1="350" x2="750" y2="358" />
        <line x1="92" y1="350" x2="100" y2="350" /><line x1="92" y1="297" x2="100" y2="297" /><line x1="92" y1="243" x2="100" y2="243" /><line x1="92" y1="190" x2="100" y2="190" /><line x1="92" y1="137" x2="100" y2="137" /><line x1="92" y1="83" x2="100" y2="83" /><line x1="92" y1="30" x2="100" y2="30" />
      </g>
      <g v-click.fade-in="1" class="scatter-points" fill="#66869b" fill-opacity="0.86" stroke="#496b81" stroke-width="1">
        <!-- Fixed-seed simulated observations (seed 13065); the trend line is the OLS fit. -->
        <circle cx="634" cy="73" r="5.5" /><circle cx="382" cy="190" r="5.5" /><circle cx="268" cy="218" r="5.5" /><circle cx="242" cy="248" r="5.5" /><circle cx="583" cy="183" r="5.5" />
        <circle cx="258" cy="322" r="5.5" /><circle cx="619" cy="102" r="5.5" /><circle cx="518" cy="193" r="5.5" /><circle cx="381" cy="251" r="5.5" /><circle cx="441" cy="139" r="5.5" />
        <circle cx="274" cy="205" r="5.5" /><circle cx="367" cy="242" r="5.5" /><circle cx="468" cy="195" r="5.5" /><circle cx="607" cy="156" r="5.5" /><circle cx="368" cy="234" r="5.5" />
        <circle cx="328" cy="212" r="5.5" /><circle cx="492" cy="207" r="5.5" /><circle cx="616" cy="86" r="5.5" /><circle cx="165" cy="317" r="5.5" /><circle cx="653" cy="153" r="5.5" />
        <circle cx="675" cy="154" r="5.5" /><circle cx="524" cy="132" r="5.5" /><circle cx="629" cy="124" r="5.5" /><circle cx="423" cy="141" r="5.5" /><circle cx="683" cy="94" r="5.5" />
        <circle cx="217" cy="313" r="5.5" /><circle cx="265" cy="237" r="5.5" /><circle cx="508" cy="152" r="5.5" /><circle cx="500" cy="303" r="5.5" /><circle cx="567" cy="69" r="5.5" />
        <circle cx="180" cy="224" r="5.5" /><circle cx="314" cy="265" r="5.5" /><circle cx="200" cy="327" r="5.5" /><circle cx="171" cy="297" r="5.5" /><circle cx="660" cy="86" r="5.5" />
        <circle cx="647" cy="101" r="5.5" /><circle cx="687" cy="83" r="5.5" /><circle cx="191" cy="200" r="5.5" /><circle cx="412" cy="191" r="5.5" /><circle cx="354" cy="221" r="5.5" />
        <circle cx="460" cy="161" r="5.5" /><circle cx="170" cy="296" r="5.5" /><circle cx="573" cy="115" r="5.5" /><circle cx="223" cy="306" r="5.5" /><circle cx="603" cy="136" r="5.5" />
        <circle cx="235" cy="284" r="5.5" /><circle cx="542" cy="74" r="5.5" /><circle cx="331" cy="178" r="5.5" /><circle cx="464" cy="248" r="5.5" /><circle cx="681" cy="68" r="5.5" />
        <circle cx="252" cy="261" r="5.5" /><circle cx="497" cy="172" r="5.5" /><circle cx="602" cy="113" r="5.5" /><circle cx="406" cy="245" r="5.5" /><circle cx="648" cy="180" r="5.5" />
        <circle cx="222" cy="289" r="5.5" /><circle cx="555" cy="194" r="5.5" /><circle cx="340" cy="255" r="5.5" /><circle cx="192" cy="279" r="5.5" /><circle cx="571" cy="120" r="5.5" />
        <circle cx="546" cy="141" r="5.5" /><circle cx="212" cy="254" r="5.5" /><circle cx="310" cy="240" r="5.5" /><circle cx="254" cy="251" r="5.5" /><circle cx="521" cy="219" r="5.5" />
      </g>
      <line v-click.fade-in="2" class="trend-line" x1="112" y1="312" x2="738" y2="82" />
      <g class="axis-labels" fill="#34363a" font-family="Inter, Aptos, Arial, sans-serif" font-size="21" font-weight="500">
        <text x="425" y="410" text-anchor="middle">Shots</text>
        <text x="28" y="190" text-anchor="middle" transform="rotate(-90 28 190)">Shots on Target</text>
      </g>
    </svg>
  </div>
  <p v-click.fade-in="3" class="correlation-takeaway">Soccer statistics are often correlated.</p>
</main>

<style>
.soccer-correlation { color: #282a2d; background: #f7f5f0; }
.soccer-correlation .correlation-slide { box-sizing: border-box; width: 100%; height: 100%; display: grid; grid-template-rows: auto minmax(0, 1fr) auto; justify-items: center; align-items: center; padding: 0.85rem 2rem 0.65rem; }
.soccer-correlation h1 { margin: 0; color: #282a2d; font-family: Georgia, 'Times New Roman', serif; font-size: clamp(2rem, 3.3vw, 2.65rem); font-weight: 500; letter-spacing: -0.035em; line-height: 1.1; text-align: center; }
.soccer-correlation .correlation-plot-wrap { box-sizing: border-box; width: min(100%, 980px); height: 100%; min-height: 0; display: grid; place-items: center; }
.soccer-correlation .correlation-plot { display: block; width: 100%; height: 100%; max-height: 100%; }
.soccer-correlation .axis-labels text { font-size: 21px !important; }
.soccer-correlation .trend-line { stroke: #c8102e; stroke-width: 3; stroke-dasharray: 11 10; stroke-linecap: round; opacity: 0.78; }
.soccer-correlation .correlation-takeaway { align-self: end; margin: 0 0 0.2rem; padding: 0.5rem 0.8rem 0.3rem; border-top: 1px solid #e0dcd4; color: #34363a; font: 500 clamp(1.2rem, 1.8vw, 1.5rem)/1.2 Georgia, 'Times New Roman', serif; text-align: center; }
@media (max-width: 700px) {
  .soccer-correlation .correlation-slide { padding: 0.7rem 0.8rem 0.45rem; }
  .soccer-correlation h1 { font-size: 1.55rem; }
  .soccer-correlation .correlation-plot-wrap { width: 100%; }
  .soccer-correlation .correlation-takeaway { padding: 0.35rem 0.25rem 0.2rem; font-size: 0.95rem; }
}
</style>
---
class: soccer-correlation-scale
layout: default
---

<main class="correlation-scale-slide">
  <h1>Correlation Isn't Always Obvious</h1>

  <section class="correlation-scale-section" aria-label="Correlation scale from negative one to positive one">
    <div class="correlation-scale-content">
      <h2 class="correlation-question">What is Correlation?</h2>
      <div class="coefficient-scale">
        <div class="coefficient-gradient" aria-hidden="true">
          <span style="left: 0%"></span><span style="left: 25%"></span><span style="left: 50%"></span><span style="left: 75%"></span><span style="left: 100%"></span>
        </div>
        <div class="coefficient-values"><span>−1</span><span>−0.5</span><span>0</span><span>+0.5</span><span>+1</span></div>
      </div>
      <div v-click.fade-in="1" class="correlation-meaning">
        <div class="meaning-labels"><span>Strong negative relationship</span><span>No clear linear relationship</span><span>Strong positive relationship</span></div>
      </div>
    </div>
  </section>

  <section v-click.fade-in="2" class="research-findings" aria-label="Relationships with Shots on Target">
    <h3>Surprising Relationships</h3>
    <h2>Relationships with Shots on Target</h2>
    <div class="finding-axis-row" aria-hidden="true">
      <span></span>
      <div class="finding-axis"><span>−1</span><span>0</span><span>+1</span></div>
    </div>
    <div v-click.fade-in="3" class="finding-row">
      <span class="finding-name">Clean Sheets</span>
      <div class="finding-track positive" style="--bar-width: 28%; --value-position: 78%">
        <span class="finding-bar"></span><span class="finding-value">+0.56</span>
      </div>
    </div>
    <div v-click.fade-in="4" class="finding-row">
      <span class="finding-name">Goals Allowed</span>
      <div class="finding-track negative" style="--bar-width: 30.5%; --value-position: 19.5%">
        <span class="finding-bar"></span><span class="finding-value">−0.61</span>
      </div>
    </div>
    <div v-click.fade-in="5" class="finding-row">
      <span class="finding-name">Goalkeeper Losses</span>
      <div class="finding-track negative" style="--bar-width: 35%; --value-position: 15%">
        <span class="finding-bar"></span><span class="finding-value">−0.70</span>
      </div>
    </div>
  </section>

  <p v-click.fade-in="6" class="correlation-conclusion">Even different aspects of soccer can be related.</p>
</main>

<style>
.soccer-correlation-scale { color: #282a2d; background: #f7f5f0; }
.soccer-correlation-scale .correlation-scale-slide { box-sizing: border-box; width: 100%; height: 100%; display: grid; grid-template-rows: auto auto minmax(0, 1fr) auto; gap: 0.35rem; padding: 0.65rem 2rem 0.45rem; }
.soccer-correlation-scale h1 { margin: 0; color: #282a2d; font-family: Georgia, 'Times New Roman', serif; font-size: clamp(2rem, 3.2vw, 2.55rem); font-weight: 500; letter-spacing: -0.035em; line-height: 1.1; text-align: center; }
.soccer-correlation-scale .correlation-scale-section { height: 12rem; min-height: 0; display: grid; place-items: center; transition: height 0.45s ease; }
.soccer-correlation-scale .correlation-scale-content { width: min(100%, 850px); }
.soccer-correlation-scale .coefficient-scale,.soccer-correlation-scale .correlation-meaning { transform-origin: center center; transition: transform 0.45s ease; }
.soccer-correlation-scale .correlation-question,.soccer-correlation-scale .research-findings h3 { color: #34363a; font: 600 clamp(1.05rem, 1.5vw, 1.2rem)/1.15 Georgia, 'Times New Roman', serif; text-align: center; }
.soccer-correlation-scale .correlation-question { margin: 0 0 0.9rem; }
.soccer-correlation-scale .coefficient-scale { width: 100%; max-width: 760px; margin: 0 auto; }
.soccer-correlation-scale .coefficient-gradient { position: relative; height: 0.8rem; margin: 0 0.35rem; border-radius: 999px; background: linear-gradient(90deg, #c8102e 0%, #d98d99 25%, #b9b7b2 50%, #8da6b4 75%, #66869b 100%); }
.soccer-correlation-scale .coefficient-gradient span { position: absolute; top: 50%; width: 2px; height: 1.35rem; background: #5b5b59; transform: translate(-50%, -50%); }
.soccer-correlation-scale .coefficient-gradient span:first-child,.soccer-correlation-scale .coefficient-gradient span:last-child { height: 1.55rem; }
.soccer-correlation-scale .coefficient-values { display: grid; grid-template-columns: repeat(5, 1fr); margin-top: 0.5rem; color: #34363a; font: 500 1rem/1 Inter, 'Aptos', Arial, sans-serif; font-variant-numeric: tabular-nums; text-align: center; }
.soccer-correlation-scale .coefficient-values span:first-child { text-align: left; }
.soccer-correlation-scale .coefficient-values span:last-child { text-align: right; }
.soccer-correlation-scale .correlation-meaning { margin: 1rem auto 0; text-align: center; }
.soccer-correlation-scale .meaning-labels { display: grid; grid-template-columns: 1fr 1fr 1fr; color: #4a4946; font: 500 0.82rem/1.2 Inter, 'Aptos', Arial, sans-serif; }
.soccer-correlation-scale .meaning-labels span:first-child { color: #a90d27; text-align: left; }
.soccer-correlation-scale .meaning-labels span:last-child { color: #526f81; text-align: right; }
.soccer-correlation-scale:has(.research-findings:not(.slidev-vclick-hidden)) .correlation-scale-section { height: 8.8rem; }
.soccer-correlation-scale:has(.research-findings:not(.slidev-vclick-hidden)) .coefficient-scale,.soccer-correlation-scale:has(.research-findings:not(.slidev-vclick-hidden)) .correlation-meaning { transform: scale(0.86); }
.soccer-correlation-scale .research-findings { width: min(100%, 960px); min-height: 0; justify-self: center; align-self: stretch; display: grid; grid-template-rows: auto auto auto repeat(3, minmax(2.45rem, 1fr)); gap: 0.18rem; padding: 0.1rem 0 0.15rem; border-top: 1px solid #e0dcd4; }
.soccer-correlation-scale .research-findings h3 { margin: 0.2rem 0 0; }
.soccer-correlation-scale .research-findings h2 { margin: 0.05rem 0 0.15rem; color: #34363a; font: 500 clamp(1rem, 1.35vw, 1.15rem)/1.15 Georgia, 'Times New Roman', serif; text-align: center; }
.soccer-correlation-scale .finding-axis-row,.soccer-correlation-scale .finding-row { display: grid; grid-template-columns: minmax(10rem, 0.9fr) minmax(0, 2.2fr); gap: 1rem; align-items: center; }
.soccer-correlation-scale .finding-axis { display: flex; justify-content: space-between; color: #77736e; font: 400 0.75rem/1 Inter, 'Aptos', Arial, sans-serif; font-variant-numeric: tabular-nums; }
.soccer-correlation-scale .finding-name { color: #34363a; font: 500 1rem/1.15 Inter, 'Aptos', Arial, sans-serif; }
.soccer-correlation-scale .finding-track { position: relative; height: 1.6rem; min-width: 0; }
.soccer-correlation-scale .finding-track::before { position: absolute; top: 50%; left: 0; right: 0; border-top: 1px solid #c9c6c0; content: ''; }
.soccer-correlation-scale .finding-track::after { position: absolute; top: 0.1rem; bottom: 0.1rem; left: 50%; border-left: 1px solid #8f8b85; content: ''; }
.soccer-correlation-scale .finding-bar { position: absolute; top: 50%; height: 0.72rem; border-radius: 999px; transform: translateY(-50%); }
.soccer-correlation-scale .finding-track.positive .finding-bar { left: 50%; width: var(--bar-width); background: #66869b; }
.soccer-correlation-scale .finding-track.negative .finding-bar { right: 50%; width: var(--bar-width); background: #c8102e; }
.soccer-correlation-scale .finding-value { position: absolute; top: calc(50% - 0.5rem); color: #34363a; font: 600 0.9rem/1 Inter, 'Aptos', Arial, sans-serif; font-variant-numeric: tabular-nums; transform: translateY(-90%); }
.soccer-correlation-scale .finding-track.positive .finding-value { left: calc(var(--value-position) + 0.7rem); }
.soccer-correlation-scale .finding-track.negative .finding-value { left: calc(var(--value-position) - 0.7rem); transform: translate(-100%, -90%); }
.soccer-correlation-scale .correlation-conclusion { justify-self: center; align-self: end; margin: 0 0 0.15rem; padding-top: 0.45rem; border-top: 1px solid #e0dcd4; color: #34363a; font: 500 clamp(1.15rem, 1.7vw, 1.4rem)/1.2 Georgia, 'Times New Roman', serif; text-align: center; }
@media (max-width: 700px) {
  .soccer-correlation-scale .correlation-scale-slide { gap: 0.18rem; padding: 0.55rem 0.9rem 0.35rem; }
  .soccer-correlation-scale h1 { font-size: 1.55rem; }
  .soccer-correlation-scale .correlation-scale-section { height: 10.5rem; }
  .soccer-correlation-scale:has(.research-findings:not(.slidev-vclick-hidden)) .correlation-scale-section { height: 7.7rem; }
  .soccer-correlation-scale .coefficient-gradient { height: 0.62rem; }
  .soccer-correlation-scale .coefficient-values { font-size: 0.75rem; }
  .soccer-correlation-scale .correlation-question { margin-bottom: 0.65rem; }
  .soccer-correlation-scale .correlation-meaning { margin-top: 0.75rem; }
  .soccer-correlation-scale .meaning-labels { font-size: 0.56rem; }
  .soccer-correlation-scale .research-findings { grid-template-rows: auto auto auto repeat(3, minmax(2.05rem, 1fr)); gap: 0.1rem; }
  .soccer-correlation-scale .research-findings h2 { font-size: 0.95rem; }
  .soccer-correlation-scale .finding-axis-row,.soccer-correlation-scale .finding-row { grid-template-columns: minmax(6.3rem, 0.85fr) minmax(0, 2.2fr); gap: 0.4rem; }
  .soccer-correlation-scale .finding-axis { font-size: 0.6rem; }
  .soccer-correlation-scale .finding-name { font-size: 0.68rem; }
  .soccer-correlation-scale .finding-track { height: 1.35rem; }
  .soccer-correlation-scale .finding-bar { height: 0.55rem; }
  .soccer-correlation-scale .finding-value { top: calc(50% - 0.35rem); font-size: 0.62rem; }
  .soccer-correlation-scale .correlation-conclusion { padding-top: 0.32rem; font-size: 0.88rem; }
}
</style>

---
class: soccer-correlation-motivation
layout: default
---

<main class="correlation-motivation-slide">
  <h1>Why Does Correlation Matter?</h1>
  <div class="plot-stack" role="img" aria-label="Conceptual scatterplot of Shots and Shots on Target, with Team A, Team B, and Team C revealed in sequence.">
    <img class="plot-layer plot-base" src="/slide15/scatter-base-v4.svg" alt="" />
    <img v-click.fade-in="1" class="plot-layer plot-team-b" src="/slide15/team-b-v3.svg" alt="" />
    <img v-click.fade-in="2" class="plot-layer plot-team-c" src="/slide15/team-c-v3.svg" alt="" />
  </div>
  <p v-click.fade-in="3" class="distance-statement">Team B and Team C are the same Euclidean distance from Team A.</p>
  <p v-click.fade-in="4" class="similarity-question">Does equal distance really mean equal similarity?</p>
</main>

<style>
.soccer-correlation-motivation { color: #282a2d; background: #f7f5f0; }
.soccer-correlation-motivation .correlation-motivation-slide { box-sizing: border-box; width: 100%; height: 100%; display: grid; grid-template-rows: auto minmax(0, 1fr) auto auto; gap: 0.15rem; padding: 0.5rem 1.6rem 0.4rem; }
.soccer-correlation-motivation h1 { margin: 0; color: #282a2d; font-family: Georgia, 'Times New Roman', serif; font-size: clamp(1.9rem, 3.1vw, 2.45rem); font-weight: 500; letter-spacing: -0.035em; line-height: 1.1; text-align: center; }
.soccer-correlation-motivation .plot-stack { position: relative; justify-self: center; width: min(100%, 1120px); height: 100%; min-height: 0; }
.soccer-correlation-motivation .plot-layer { position: absolute; inset: 0; display: block; width: 100%; height: 100%; object-fit: contain; }
.soccer-correlation-motivation .distance-statement { margin: 0.2rem 0 0; color: #5a5752; font: 500 clamp(1rem, 1.35vw, 1.2rem)/1.25 Inter, 'Aptos', Arial, sans-serif; text-align: center; }
.soccer-correlation-motivation .similarity-question { margin: 0.2rem 0 0; padding: 0.55rem 0 0.25rem; border-top: 1px solid #e0dcd4; color: #34363a; font: 500 clamp(1.3rem, 2vw, 1.6rem)/1.2 Georgia, 'Times New Roman', serif; text-align: center; }
@media (max-width: 700px) {
  .soccer-correlation-motivation .correlation-motivation-slide { padding: 0.45rem 0.7rem 0.3rem; }
  .soccer-correlation-motivation h1 { font-size: 1.55rem; }
  .soccer-correlation-motivation .distance-statement { font-size: 0.78rem; }
  .soccer-correlation-motivation .similarity-question { font-size: 0.98rem; }
}
</style>

---
class: soccer-whitening
layout: default
---

<main class="whitening-slide">
  <h1>Whitening the Data</h1>
  <div class="whitening-figure" role="img" aria-label="The same 65 illustrative observations before and after whitening. The slide reveals the two correlation patterns and three corresponding example observations in sequence.">
    <img class="plot-layer" src="/slide16/before.svg?v=2" alt="" />
    <img v-click.fade-in="1" class="plot-layer" src="/slide16/original-correlation.svg?v=2" alt="" />
    <img v-click.fade-in="[2, 6]" class="plot-layer" src="/slide16/before-ellipse.svg?v=1" alt="" />
    <img v-click.fade-in="3" class="plot-layer" src="/slide16/after.svg?v=4" alt="" />
    <img v-click.fade-in="4" class="plot-layer" src="/slide16/transformed-correlation.svg?v=2" alt="" />
    <img v-click.fade-in="[5, 6]" class="plot-layer" src="/slide16/after-circle.svg?v=1" alt="" />
    <img v-click.fade-in="7" class="plot-layer" src="/slide16/example-original-21.svg?v=2" alt="" />
    <img v-click.fade-in="8" class="plot-layer" src="/slide16/example-original-36.svg?v=2" alt="" />
    <img v-click.fade-in="9" class="plot-layer" src="/slide16/example-original-40.svg?v=2" alt="" />
    <img v-click.fade-in="10" class="plot-layer" src="/slide16/example-whitened-21.svg?v=2" alt="" />
    <img v-click.fade-in="11" class="plot-layer" src="/slide16/example-whitened-36.svg?v=2" alt="" />
    <img v-click.fade-in="12" class="plot-layer" src="/slide16/example-whitened-40.svg?v=2" alt="" />
  </div>
  <p v-click.fade-in="13" class="whitening-takeaway">Adjusting the coordinates to account for correlation.</p>
</main>

<style>
.soccer-whitening { color: #282a2d; background: #f7f5f0; }
.soccer-whitening .whitening-slide { box-sizing: border-box; width: 100%; height: 100%; display: grid; grid-template-rows: auto minmax(0, 1fr) auto; justify-items: center; align-items: center; gap: 0.2rem; padding: 0.45rem 1.35rem 0.35rem; }
.soccer-whitening h1 { margin: 0; color: #282a2d; font-family: Georgia, 'Times New Roman', serif; font-size: clamp(1.9rem, 3.1vw, 2.45rem); font-weight: 500; letter-spacing: -0.035em; line-height: 1.1; text-align: center; }
.soccer-whitening .whitening-figure { position: relative; justify-self: center; width: min(100%, 1380px); height: 100%; min-height: 0; }
.soccer-whitening .plot-layer { position: absolute; inset: 0; display: block; width: 100%; height: 100%; object-fit: contain; }
.soccer-whitening .whitening-takeaway { align-self: end; justify-self: center; margin: 0 0 0.12rem; padding-top: 0.4rem; border-top: 1px solid #e0dcd4; color: #34363a; font: 500 clamp(1.15rem, 1.7vw, 1.4rem)/1.2 Georgia, 'Times New Roman', serif; text-align: center; }
@media (max-width: 700px) {
  .soccer-whitening .whitening-slide { padding: 0.45rem 0.65rem 0.3rem; gap: 0.12rem; }
  .soccer-whitening h1 { font-size: 1.55rem; }
  .soccer-whitening .whitening-takeaway { font-size: 0.88rem; }
}
</style>

---
class: soccer-similarity-whitening
layout: default
---

<main class="similarity-whitening-slide">
  <h1>Does Whitening Change Similarity?</h1>
  <div class="similarity-whitening-figure" role="img" aria-label="Before and after whitening comparison of Team A, Team B, and Team C. Team B and Team C are equally distant from Team A before whitening, while the transformed distances differ.">
    <img class="comparison-layer" src="/slide17/before.svg?v=1" alt="" />
    <img v-click.fade-in="1" class="comparison-layer" src="/slide17/after-background.svg?v=1" alt="" />
    <img v-click.fade-in="2" class="comparison-layer" src="/slide17/after-team-a.svg?v=2" alt="" />
    <img v-click.fade-in="3" class="comparison-layer" src="/slide17/after-team-b.svg?v=2" alt="" />
    <img v-click.fade-in="4" class="comparison-layer" src="/slide17/after-team-c.svg?v=2" alt="" />
  </div>
  <p v-click.fade-in="5" class="similarity-whitening-takeaway">Accounting for correlation changes how we measure similarity.</p>
</main>

<style>
.soccer-similarity-whitening { color: #282a2d; background: #f7f5f0; }
.similarity-whitening-slide { box-sizing: border-box; width: 100%; height: 100%; display: grid; grid-template-rows: auto minmax(0, 1fr) auto; justify-items: center; align-items: center; gap: 0.15rem; padding: 0.45rem 1rem 0.35rem; }
.similarity-whitening-slide h1 { margin: 0; color: #282a2d; font-family: Georgia, "Times New Roman", serif; font-size: clamp(1.9rem, 3.1vw, 2.45rem); font-weight: 500; letter-spacing: -0.035em; line-height: 1.1; text-align: center; }
.similarity-whitening-figure { position: relative; justify-self: center; width: min(100%, 1440px); height: 100%; min-height: 0; }
.similarity-whitening-figure .comparison-layer { position: absolute; inset: 0; display: block; width: 100%; height: 100%; object-fit: contain; }
.similarity-whitening-takeaway { justify-self: center; margin: 0 0 0.1rem; padding-top: 0.45rem; border-top: 1px solid #e0dcd4; color: #34363a; font: 700 clamp(1.2rem, 1.8vw, 1.45rem)/1.2 Georgia, "Times New Roman", serif; text-align: center; text-decoration-line: underline; text-decoration-color: #c8102e; text-decoration-thickness: 2.5px; text-underline-offset: 8px; }
@media (max-width: 700px) {
  .similarity-whitening-slide { padding: 0.45rem 0.6rem 0.3rem; gap: 0.1rem; }
  .similarity-whitening-slide h1 { font-size: 1.55rem; }
  .similarity-whitening-takeaway { font-size: 0.88rem; }
}
</style>

---
class: soccer-scale-up
layout: default
---

<main class="scale-up-slide">
  <h1>From 2 Variables to 40 Variables</h1>
  <div class="scale-up-figure" role="img" aria-label="A correlated two-variable scatterplot leads to a symbolic dataset matrix with 40 initial variables.">
    <img class="scale-up-layer" src="/slide18/example.svg?v=1" alt="" />
    <img v-click.fade-in="1" class="scale-up-layer" src="/slide18/transition.svg?v=1" alt="" />
    <img v-click.fade-in="2" class="scale-up-layer" src="/slide18/dataset-matrix.svg?v=1" alt="" />
  </div>
  <div v-click.fade-in="3" class="scale-up-context" aria-label="Dataset size: 500 team-seasons across 25 seasons">
    <span><strong>500</strong> Team-Seasons</span>
    <i aria-hidden="true"></i>
    <span><strong>25</strong> Seasons</span>
  </div>
  <p v-click.fade-in="4" class="scale-up-takeaway">The same idea, applied to many statistics at once.</p>
</main>

<style>
.soccer-scale-up { color: #282a2d; background: #f7f5f0; }
.scale-up-slide { box-sizing: border-box; width: 100%; height: 100%; display: grid; grid-template-rows: auto minmax(0,1fr) auto; justify-items: center; align-items: center; gap: 0.12rem; padding: 0.45rem 1rem 0.35rem; }
.scale-up-slide h1 { margin: 0; color: #282a2d; font-family: Georgia, 'Times New Roman', serif; font-size: clamp(1.9rem,3.1vw,2.45rem); font-weight: 500; letter-spacing: -0.035em; line-height: 1.1; text-align: center; }
.scale-up-figure { position: relative; justify-self: center; width: min(100%,1440px); height: 100%; min-height: 0; }
.scale-up-layer { position: absolute; inset: 0; display: block; width: 100%; height: 100%; object-fit: contain; }
.scale-up-context { display: flex; align-items: center; justify-content: center; gap: 2rem; color: #5a5752; font: 600 clamp(1rem,1.4vw,1.15rem)/1.2 Inter, Aptos, Arial, sans-serif; }
.scale-up-context strong { color: #c8102e; font: 700 1.5em/1 Georgia, 'Times New Roman', serif; margin-right: 0.22rem; }
.scale-up-context i { width: 1px; height: 1.5rem; background: #d9d4cc; }
.scale-up-takeaway { justify-self: center; margin: 0 0 0.1rem; padding-top: 0.4rem; border-top: 1px solid #e0dcd4; color: #34363a; font: 500 clamp(1.1rem,1.6vw,1.35rem)/1.2 Georgia, 'Times New Roman', serif; text-align: center; }
@media (max-width:700px) { .scale-up-slide { padding: .4rem .55rem .25rem; gap:.08rem; } .scale-up-slide h1 { font-size:1.55rem; } .scale-up-context { gap:1rem; } .scale-up-takeaway { font-size:.9rem; } }
</style>

---
class: soccer-variable-reduction
layout: default
---

<main class="variable-reduction-slide">
  <h1>From 40 Variables back to 14</h1>
  <div class="variable-reduction-figure" role="img" aria-label="An initial 40-variable dataset has six illustrative dependency cells highlighted before reduction to 14 retained variables.">
    <img class="reduction-layer" src="/slide19/initial-matrix.svg?v=1" alt="" />
    <img v-click.fade-in="1" class="reduction-layer" src="/slide19/problem-dependencies.svg?v=1" alt="" />
    <img v-click.fade-in="2" class="reduction-layer" src="/slide19/usable-matrix.svg?v=1" alt="" />
  </div>
  <p v-click.fade-in="3" class="reduction-takeaway">Some statistics repeated too much information already captured by others.</p>
</main>

<style>
.soccer-variable-reduction { color: #282a2d; background: #f7f5f0; }
.variable-reduction-slide { box-sizing: border-box; width: 100%; height: 100%; display: grid; grid-template-rows: auto minmax(0,1fr) auto; justify-items: center; align-items: center; gap: 0.12rem; padding: 0.45rem 1rem 0.35rem; }
.variable-reduction-slide h1 { margin: 0; color: #282a2d; font-family: Georgia, 'Times New Roman', serif; font-size: clamp(1.9rem,3.1vw,2.45rem); font-weight: 500; letter-spacing: -0.035em; line-height: 1.1; text-align: center; }
.variable-reduction-figure { position: relative; justify-self: center; width: min(100%,1440px); height: 100%; min-height: 0; }
.reduction-layer { position: absolute; inset: 0; display: block; width: 100%; height: 100%; object-fit: contain; }
.reduction-takeaway { justify-self: center; margin: 0 0 0.1rem; padding-top: 0.42rem; border-top: 1px solid #e0dcd4; color: #34363a; font: 500 clamp(1.2rem,1.8vw,1.5rem)/1.2 Georgia, 'Times New Roman', serif; text-align: center; white-space: nowrap; }
.reduction-takeaway span { color: #c8102e; }
@media (max-width:700px) { .variable-reduction-slide { padding:.4rem .55rem .25rem; gap:.08rem; } .variable-reduction-slide h1 { font-size:1.55rem; } .reduction-takeaway { font-size:.9rem; white-space:normal; } }
</style>

---
class: soccer-score-pipeline
layout: default
---

<main class="score-pipeline-slide">
  <h1>Building the Soccer Similarity Score</h1>
  <div class="score-pipeline-figure" role="img" aria-label="Fourteen retained variables pass through a whitening transform, followed by Euclidean distance in whitened space, which is Mahalanobis distance.">
    <svg class="pipeline-layer" xmlns="http://www.w3.org/2000/svg" width="1500" height="500" viewBox="0 0 1500 500" aria-hidden="true">
      <rect x="145" y="142" width="30" height="30" rx="2" fill="#c9d9e2" stroke="#f7f5f0" stroke-width="1.5"/>
      <rect x="181" y="142" width="30" height="30" rx="2" fill="#d9e4e9" stroke="#f7f5f0" stroke-width="1.5"/>
      <rect x="217" y="142" width="30" height="30" rx="2" fill="#d9e4e9" stroke="#f7f5f0" stroke-width="1.5"/>
      <rect x="253" y="142" width="30" height="30" rx="2" fill="#c9d9e2" stroke="#f7f5f0" stroke-width="1.5"/>
      <rect x="289" y="142" width="30" height="30" rx="2" fill="#d9e4e9" stroke="#f7f5f0" stroke-width="1.5"/>
      <rect x="325" y="142" width="30" height="30" rx="2" fill="#d9e4e9" stroke="#f7f5f0" stroke-width="1.5"/>
      <rect x="361" y="142" width="30" height="30" rx="2" fill="#c9d9e2" stroke="#f7f5f0" stroke-width="1.5"/>
      <rect x="145" y="178" width="30" height="30" rx="2" fill="#d9e4e9" stroke="#f7f5f0" stroke-width="1.5"/>
      <rect x="181" y="178" width="30" height="30" rx="2" fill="#d9e4e9" stroke="#f7f5f0" stroke-width="1.5"/>
      <rect x="217" y="178" width="30" height="30" rx="2" fill="#c9d9e2" stroke="#f7f5f0" stroke-width="1.5"/>
      <rect x="253" y="178" width="30" height="30" rx="2" fill="#d9e4e9" stroke="#f7f5f0" stroke-width="1.5"/>
      <rect x="289" y="178" width="30" height="30" rx="2" fill="#d9e4e9" stroke="#f7f5f0" stroke-width="1.5"/>
      <rect x="325" y="178" width="30" height="30" rx="2" fill="#c9d9e2" stroke="#f7f5f0" stroke-width="1.5"/>
      <rect x="361" y="178" width="30" height="30" rx="2" fill="#d9e4e9" stroke="#f7f5f0" stroke-width="1.5"/>
      <text x="250" y="265" text-anchor="middle" font-family="Georgia, 'Times New Roman', serif" font-size="25" style="font-size:25px" font-weight="700" fill="#34363a">14 Retained Variables</text>
    </svg>
    <svg v-click.fade-in="1" class="pipeline-layer" xmlns="http://www.w3.org/2000/svg" width="1500" height="500" viewBox="0 0 1500 500" aria-hidden="true">
      <line x1="410" y1="204" x2="570" y2="204" stroke="#c8102e" stroke-width="4.5" stroke-linecap="round"/><path d="M570 189L596 204L570 219Z" fill="#c8102e"/>
      <g transform="translate(14 0)">
      <line x1="690" y1="255" x2="810" y2="255" stroke="#aaa69f" stroke-width="1.5"/><line x1="750" y1="145" x2="750" y2="270" stroke="#aaa69f" stroke-width="1.5"/>
      <g transform="translate(-21 0)">
      <ellipse cx="720" cy="205" rx="38" ry="17" transform="rotate(-34 720 205)" fill="#d8e4e9" stroke="#758d9d" stroke-width="2.5"/>
      <circle cx="710" cy="215" r="4" fill="#66869b"/><circle cx="725" cy="202" r="4" fill="#66869b"/><circle cx="737" cy="191" r="4" fill="#66869b"/>
      <g transform="translate(116.9 30.75) scale(0.85)"><path d="M761 205H783" stroke="#c8102e" stroke-width="2.5"/><path d="M783 198L794 205L783 212Z" fill="#c8102e"/></g>
      <circle cx="825" cy="205" r="31" fill="#f0f3f4" stroke="#758d9d" stroke-width="2.5"/>
      <circle cx="810" cy="191" r="4" fill="#66869b"/><circle cx="829" cy="188" r="4" fill="#66869b"/><circle cx="839" cy="202" r="4" fill="#66869b"/><circle cx="815" cy="212" r="4" fill="#66869b"/><circle cx="831" cy="220" r="4" fill="#66869b"/><circle cx="823" cy="204" r="4" fill="#66869b"/>
      </g>
      <text x="750" y="319" text-anchor="middle" font-family="Georgia, 'Times New Roman', serif" font-size="25" style="font-size:25px" font-weight="700" fill="#34363a">Whitening Transform</text>
      </g>
    </svg>
    <svg v-click.fade-in="2" class="pipeline-layer" xmlns="http://www.w3.org/2000/svg" width="1500" height="500" viewBox="0 0 1500 500" aria-hidden="true">
      <line x1="932" y1="204" x2="1092" y2="204" stroke="#c8102e" stroke-width="4.5" stroke-linecap="round"/><path d="M1092 189L1118 204L1092 219Z" fill="#c8102e"/>
      <line x1="1160" y1="260" x2="1360" y2="260" stroke="#aaa69f" stroke-width="1.8"/><line x1="1160" y1="260" x2="1160" y2="142" stroke="#aaa69f" stroke-width="1.8"/>
      <line x1="1192" y1="226" x2="1326" y2="165" stroke="#758d9d" stroke-width="3" stroke-dasharray="6 5"/>
      <circle cx="1192" cy="226" r="8" fill="#34363a" stroke="#f7f5f0" stroke-width="2"/><circle cx="1326" cy="165" r="8" fill="#c8102e" stroke="#f7f5f0" stroke-width="2"/>
      <text x="1260" y="307" text-anchor="middle" font-family="Georgia, 'Times New Roman', serif" font-size="23" style="font-size:23px" font-weight="700" fill="#34363a">Euclidean Distance</text>
      <text x="1260" y="337" text-anchor="middle" font-family="Georgia, 'Times New Roman', serif" font-size="22" style="font-size:22px" font-weight="600" fill="#34363a">in Whitened Space</text>
    </svg>
  </div>
  <div v-click.fade-in="3" class="pipeline-conclusion">
    <svg class="pipeline-down-arrow" viewBox="0 0 28 172" aria-hidden="true"><path d="M14 1V157M7 149L14 165L21 149" fill="none" stroke="#c8102e" stroke-width="3" stroke-linecap="round" stroke-linejoin="round"/></svg>
    <h2>Mahalanobis Distance</h2>
  </div>
  <p v-click.fade-in="4" class="pipeline-score">Our Soccer Similarity Score</p>
  <p v-click.fade-in="5" class="pipeline-equivalence"><span>Euclidean distance after whitening</span><b>=</b><span>Mahalanobis distance</span></p>
</main>

<style>
.soccer-score-pipeline { color: #282a2d; background: #f7f5f0; }
.score-pipeline-slide { box-sizing: border-box; width: 100%; height: 100%; display: grid; grid-template-rows: auto minmax(0,1fr) auto auto auto; justify-items: center; align-items: center; gap: 0.08rem; padding: 0.4rem 1rem 0.3rem; }
.score-pipeline-slide h1 { margin: 0; color: #282a2d; font-family: Georgia, 'Times New Roman', serif; font-size: clamp(1.9rem,3.1vw,2.45rem); font-weight: 500; letter-spacing: -0.035em; line-height: 1.1; text-align: center; }
.score-pipeline-figure { position: relative; justify-self: center; width: min(100%,1440px); height: 100%; min-height: 0; }
.pipeline-layer { position: absolute; inset: 0; display: block; width: 100%; height: 100%; object-fit: contain; }
.pipeline-conclusion { position: relative; display: flex; flex-direction: column; align-items: center; justify-content: center; gap: 0.1rem; margin-top: 0.02rem; }
.pipeline-down-arrow { position: absolute; left: calc(50% + 14px); bottom: calc(100% + 0.08rem); display: block; width: 1.6rem; height: 7rem; transform: translateX(-50%); overflow: visible; }
.pipeline-conclusion h2 { margin: 0; color: #c8102e; font: 700 clamp(1.45rem,2.05vw,1.7rem)/1.08 Georgia, 'Times New Roman', serif; text-align: center; }
.pipeline-equivalence { display: flex; align-items: center; justify-content: center; gap: 0.8rem; margin: 0; color: #34363a; font: 600 clamp(1.05rem,1.55vw,1.3rem)/1.15 Georgia, 'Times New Roman', serif; text-align: center; white-space: nowrap; }
.pipeline-equivalence b { color: #c8102e; font: 700 1.3em/1 Inter, Aptos, Arial, sans-serif; }
.pipeline-score { margin: 0; color: #34363a; font: 600 clamp(1.15rem,1.7vw,1.4rem)/1.1 Georgia, 'Times New Roman', serif; text-align: center; }
@media (max-width:700px) { .score-pipeline-slide { padding:.38rem .55rem .24rem; gap:.06rem; } .score-pipeline-slide h1 { font-size:1.52rem; } .pipeline-equivalence { font-size:.84rem; gap:.35rem; white-space:normal; } .pipeline-score { font-size:.98rem; } }
</style>
---
class: soccer-interpretation
layout: default
---

<main class="interpretation-slide">
  <h1>What Are We Actually Comparing?</h1>
  <section class="variable-groups" aria-label="Four groups of retained variables">
    <article v-click.fade-in="1" class="variable-card">
      <header><h2>Goalkeeping</h2><strong>6</strong></header>
      <ul class="goalkeeping-variables"><li>Goalkeeper Clean Sheet %</li><li>Goalkeeper Save %</li><li>Goalkeeper Saves</li><li class="goalkeeper-shots-faced">Goalkeeper Shots On Target Faced</li><li>Goalkeeper Ties</li><li>Goalkeepers Used</li></ul>
    </article>
    <article v-click.fade-in="2" class="variable-card">
      <header><h2>Squad &amp; Substitutions</h2><strong>4</strong></header>
      <ul><li>Total Players Used</li><li>Average Age</li><li>Total Substitutions Throughout Season</li><li>Minutes Per Substitution</li></ul>
    </article>
    <article v-click.fade-in="3" class="variable-card">
      <header><h2>Discipline</h2><strong>2</strong></header>
      <ul><li>Yellow Cards</li><li>Fouls</li></ul>
    </article>
    <article v-click.fade-in="4" class="variable-card">
      <header><h2>Attacking</h2><strong>2</strong></header>
      <ul><li>Penalties Attempted</li><li>Shots on Target Per Game</li></ul>
    </article>
  </section>
  <section class="research-questions" aria-label="How the research question changed">
    <p v-click.fade-in="5" class="original-question"><strong>Our Original Question:</strong><span>"Which teams have the most similar playing styles?"</span></p>
    <div v-click.fade-in="6" class="final-question">
      <svg viewBox="0 0 28 20" aria-hidden="true"><path d="M14 1v12M8 9l6 6 6-6" fill="none" stroke="#c8102e" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"/></svg>
      <p><strong>Our Final Question:</strong><span>"Which team-seasons have the most similar <em>statistical profiles</em>?"</span></p>
    </div>
  </section>
</main>

<style>
.soccer-interpretation { color: #282a2d; background: #f7f5f0; }
.interpretation-slide { box-sizing: border-box; width: 100%; height: 100%; display: grid; grid-template-rows: auto minmax(0,1fr) auto; justify-items: center; align-items: center; gap: 0.4rem; padding: 0.42rem 1.15rem 0.72rem; }
.interpretation-slide h1 { margin: 0; color: #282a2d; font: 500 clamp(1.9rem,3.1vw,2.45rem)/1.1 Georgia, 'Times New Roman', serif; letter-spacing: -0.035em; text-align: center; }
.variable-groups { width: min(100%, 1140px); height: 95%; align-self: start; min-height: 0; display: grid; grid-template-columns: repeat(2,minmax(0,1fr)); grid-template-rows: minmax(0,1.45fr) minmax(0,1fr); gap: 0.6rem 0.9rem; }
.variable-card { min-width: 0; box-sizing: border-box; padding: 0.7rem 1rem; border: 1px solid #dedbd4; border-top: 2px solid #c8102e; border-radius: 0.35rem; background: rgba(255,255,255,0.72); }
.variable-card header { display: flex; justify-content: space-between; align-items: baseline; gap: 0.5rem; margin-bottom: 0.3rem; }
.variable-card h2 { margin: 0; color: #34363a; font: 600 clamp(1.02rem,1.45vw,1.2rem)/1.12 Georgia, 'Times New Roman', serif; }
.variable-card header strong { flex: 0 0 auto; color: #c8102e; font: 700 clamp(1.15rem,1.6vw,1.35rem)/1 Georgia, 'Times New Roman', serif; }
.variable-card ul { display: grid; gap: 0.11rem; margin: 0; padding: 0; list-style: none; color: #45474a; font: 500 clamp(0.76rem,0.94vw,0.84rem)/1.16 Inter, Aptos, Arial, sans-serif; }
.variable-card ul.goalkeeping-variables { font-size: clamp(0.72rem,0.9vw,0.78rem); line-height: 1.16; }
.goalkeeping-variables { grid-template-columns: minmax(0,0.95fr) minmax(0,1.05fr); grid-template-rows: repeat(3,min-content); grid-auto-flow: column; column-gap: 1.05rem; align-content: start; font: 500 clamp(0.72rem,0.9vw,0.78rem)/1.16 Inter, Aptos, Arial, sans-serif; }
.goalkeeping-variables .goalkeeper-shots-faced { font-size: clamp(0.70rem,0.86vw,0.76rem); white-space: nowrap; }
.research-questions { width: min(100%, 1140px); display: grid; justify-items: center; gap: 0.34rem; margin: 0; padding-top: 0.45rem; border-top: 1px solid #dedbd4; text-align: center; }
.original-question { margin: 0; color: #55575b; font: 500 clamp(0.9rem,1.2vw,1.02rem)/1.2 Georgia, 'Times New Roman', serif; }
.original-question strong,.final-question strong { display: block; margin: 0 0 0.08rem; color: #34363a; font-weight: 700; }
.final-question { display: flex; flex-direction: column; align-items: center; justify-content: center; gap: 0.08rem; width: 100%; }
.final-question svg { width: 0.95rem; height: 0.62rem; }
.final-question p { max-width: 1120px; margin: 0; color: #34363a; font: 600 clamp(1.02rem,1.4vw,1.16rem)/1.18 Georgia, 'Times New Roman', serif; text-align: center; }
.final-question em { color: #c8102e; font-style: normal; font-weight: 700; }
@media (max-width:700px) {
  .interpretation-slide { padding: 0.35rem 0.5rem 0.28rem; gap: 0.22rem; }
  .interpretation-slide h1 { font-size: 1.45rem; }
  .variable-groups { gap: 0.35rem; }
  .variable-card { padding: 0.42rem 0.48rem; }
  .variable-card h2 { font-size: 0.8rem; }
  .variable-card header strong { font-size: 0.95rem; }
  .variable-card ul { gap: 0.1rem; font-size: 0.60rem; line-height: 1.12; }
  .variable-card ul.goalkeeping-variables { font-size: 0.58rem; line-height: 1.08; }
  .original-question { font-size: 0.73rem; }
  .final-question p { font-size: 0.82rem; }
}
</style>

---
class: soccer-first-result
layout: default
---

<main class="first-result-slide">
  <h1>Reading the Score: A First Result</h1>

  <div class="result-columns">
    <section class="interpret-panel" aria-label="Two ways to read the score">
      <h2>Two Ways to Read the Score</h2>
      <article v-click.fade-in="1" class="mode-block raw-mode">
        <div class="mode-heading"><h3>Raw Distance</h3><strong>Lower = More Similar</strong></div>
        <div class="score-rule raw-rule"><span>More similar</span><i aria-hidden="true"></i><span>Less similar</span></div>
        <p class="mode-description">0 = identical statistical profiles</p>
      </article>
      <article v-click.fade-in="2" class="mode-block percentile-mode">
        <div class="mode-heading"><h3>Percentile Mode</h3><strong>Higher = More Similar</strong></div>
        <div class="percentile-scale">
          <div class="score-rule"><span>Less similar</span><i aria-hidden="true"></i><span>More similar</span></div>
          <div class="percentile-endpoints"><span>0th</span><span>100th</span></div>
        </div>
        <p class="mode-description">90th percentile = more similar than most pairings</p>
      </article>
    </section>
    <section class="app-column" aria-label="Shiny app results for Arsenal 2024/25">
      <h2 v-click.fade-in="3">Example from the App</h2>
      <div v-click.fade-in="3" class="app-result-panel">
        <div class="reference-team">
          <span>Reference team-season</span>
          <strong>Arsenal <i>2024/25</i></strong>
        </div>
        <div v-click.fade-in="4" class="results-table-wrap">
          <div class="results-heading"><strong>Most similar team-seasons</strong><span>Raw Distance</span></div>
          <ol class="similarity-results">
            <li class="closest"><span><b>1</b> Everton <i>2024/25</i></span><strong>2.9360</strong></li>
            <li><span><b>2</b> Brighton <i>2019/20</i></span><strong>2.9461</strong></li>
            <li><span><b>3</b> Newcastle United <i>2022/23</i></span><strong>3.0389</strong></li>
            <li><span><b>4</b> Liverpool <i>2007/08</i></span><strong>3.4448</strong></li>
            <li><span><b>5</b> Sheffield United <i>2019/20</i></span><strong>3.4881</strong></li>
          </ol>
        </div>
      </div>
    </section>
  </div>

  <footer v-click.fade-in="5" class="result-takeaway">
    <p class="result-main-takeaway">Two ways to express the same statistical similarity.</p>
    <p class="result-caveat">An abstract statistical measure, not a direct measure of playing style.</p>
  </footer>
</main>

<style>
.soccer-first-result { color: #282a2d; background: #f7f5f0; }
.first-result-slide { box-sizing: border-box; width: 100%; height: 100%; display: grid; grid-template-rows: auto minmax(0,1fr) auto; align-items: stretch; gap: .55rem; padding: .48rem 1.25rem .62rem; }
.first-result-slide h1 { margin: 0; color: #282a2d; font: 500 clamp(1.9rem,3.1vw,2.45rem)/1.1 Georgia,'Times New Roman',serif; letter-spacing: -.035em; text-align: center; }
.result-columns { width: min(100%,1180px); height: 100%; max-height: 29rem; min-height: 0; justify-self: center; align-self: stretch; display: grid; grid-template-columns: minmax(300px,.86fr) minmax(0,1.5fr); gap: .9rem; align-items: stretch; }
.interpret-panel,.app-column { box-sizing: border-box; min-width: 0; min-height: 0; display: grid; grid-template-rows: auto minmax(0,1fr); gap: .58rem; }
.interpret-panel { grid-template-rows: auto minmax(0,1fr) minmax(0,1fr); }
.interpret-panel > h2,.app-column > h2 { margin: 0; color: #34363a; font: 600 clamp(1.02rem,1.45vw,1.18rem)/1.14 Georgia,'Times New Roman',serif; }
.mode-block { box-sizing: border-box; min-height: 0; display: flex; flex-direction: column; justify-content: center; padding: .72rem .82rem; border: 1px solid #dedbd4; border-top: 2px solid #c8102e; border-radius: .35rem; background: rgba(255,255,255,.72); }
.percentile-mode { }
.mode-heading { display: flex; align-items: baseline; justify-content: space-between; gap: .4rem; }
.mode-heading h3 { margin: 0; color: #34363a; font: 700 clamp(.88rem,1.1vw,.98rem)/1.15 Georgia,'Times New Roman',serif; }
.mode-heading strong { color: #c8102e; font: 700 clamp(.75rem,.95vw,.84rem)/1.15 Inter,Aptos,Arial,sans-serif; text-align: right; }
.mode-description { margin: .34rem 0 0; color: #515356; font: 500 clamp(.73rem,.9vw,.82rem)/1.24 Inter,Aptos,Arial,sans-serif; }
.score-rule { display: grid; grid-template-columns: auto minmax(2rem,1fr) auto; align-items: center; gap: .38rem; margin-top: .48rem; color: #66686b; font: 600 clamp(.62rem,.76vw,.7rem)/1 Inter,Aptos,Arial,sans-serif; }
.score-rule i { position: relative; height: 2px; background: linear-gradient(90deg,#c8102e,#c9c5be); }
.score-rule i::after { position: absolute; top: 50%; right: 0; width: .32rem; height: .32rem; border-top: 1px solid #c8102e; border-right: 1px solid #c8102e; content: ''; transform: translateY(-50%) rotate(45deg); }
.percentile-scale { margin-top: .1rem; }
.percentile-scale .score-rule { margin-top: .42rem; background: linear-gradient(90deg,#c9c5be,#c8102e); background-clip: text; }
.percentile-scale .score-rule i { background: linear-gradient(90deg,#c9c5be,#c8102e); }
.percentile-scale .score-rule i::after { border-color: #c8102e; }
.percentile-endpoints { display: flex; justify-content: space-between; margin: .12rem .1rem 0; color: #8a8986; font: 500 clamp(.58rem,.68vw,.64rem)/1 Inter,Aptos,Arial,sans-serif; }
.zero-profile { display: flex; align-items: center; gap: .45rem; padding: .18rem .32rem; border-radius: .24rem; background: #f4eeee; }
.zero-mark { display: grid; width: 1.6rem; height: 1.6rem; flex: 0 0 auto; place-items: center; border: 1px solid #c8102e; border-radius: 50%; color: #c8102e; font: 700 .9rem Georgia,'Times New Roman',serif; }
.zero-profile b,.zero-profile small { display: block; }
.zero-profile b { color: #34363a; font: 600 clamp(.7rem,.84vw,.76rem)/1.15 Inter,Aptos,Arial,sans-serif; }
.zero-profile small { margin-top: .08rem; color: #77797b; font: 500 clamp(.62rem,.74vw,.68rem)/1.1 Inter,Aptos,Arial,sans-serif; }
.direction-cue { display: flex; align-items: center; gap: .38rem; margin: .27rem .08rem 0; color: #77797b; font: 600 .62rem/1 Inter,Aptos,Arial,sans-serif; }
.direction-cue i { height: 1px; flex: 1; background: linear-gradient(90deg,#c8102e,#c9c5be); }
.percentile-example { display: flex; flex-direction: column; gap: .1rem; padding: .24rem .38rem; border-left: 2px solid #c8102e; background: #f7f1ed; }
.percentile-example b { color: #c8102e; font: 700 clamp(.76rem,.95vw,.84rem)/1.15 Georgia,'Times New Roman',serif; }
.percentile-example span { color: #45474a; font: 600 clamp(.7rem,.85vw,.76rem)/1.18 Inter,Aptos,Arial,sans-serif; }
.example-note { display: block; margin-top: .22rem; color: #77797b; font: 500 clamp(.58rem,.7vw,.64rem)/1.15 Inter,Aptos,Arial,sans-serif; }
.app-result-panel { box-sizing: border-box; min-width: 0; min-height: 0; display: flex; flex-direction: column; padding: .82rem .95rem .66rem; border: 1px solid #dedbd4; border-top: 2px solid #c8102e; border-radius: .35rem; background: rgba(255,255,255,.72); }
.reference-team { display: flex; align-items: center; justify-content: space-between; gap: .7rem; padding: .5rem .65rem; border: 1px solid #e4e0d9; border-radius: .28rem; background: #f8f7f3; }
.reference-team span { color: #696b6d; font: 500 clamp(.72rem,.9vw,.82rem)/1.2 Inter,Aptos,Arial,sans-serif; }
.reference-team strong { color: #34363a; font: 700 clamp(.94rem,1.2vw,1.06rem)/1.2 Georgia,'Times New Roman',serif; }
.reference-team i,.similarity-results i { color: #77797b; font: normal 500 .9em Inter,Aptos,Arial,sans-serif; }
.results-table-wrap { margin-top: .42rem; }
.results-heading { display: flex; justify-content: space-between; gap: .5rem; margin: 0 .56rem .12rem; color: #66686b; font: 600 clamp(.67rem,.85vw,.76rem)/1.15 Inter,Aptos,Arial,sans-serif; text-transform: uppercase; letter-spacing: .045em; }
.similarity-results { display: grid; gap: .1rem; margin: 0; padding: 0; list-style: none; }
.similarity-results li { display: flex; align-items: center; justify-content: space-between; gap: .55rem; min-height: 2.12rem; padding: .3rem .58rem; border-bottom: 1px solid #ece9e3; color: #34363a; font: 500 clamp(.8rem,1.03vw,.92rem)/1.18 Inter,Aptos,Arial,sans-serif; }
.similarity-results li:last-child { border-bottom: 0; }
.similarity-results li.closest { border-radius: .24rem; background: #f7f1ed; }
.similarity-results li span { min-width: 0; }
.similarity-results li b { display: inline-grid; width: 1.28rem; height: 1.28rem; place-items: center; margin-right: .42rem; border-radius: 50%; color: #66686b; background: #ebe9e4; font: 600 .73rem Inter,Aptos,Arial,sans-serif; }
.similarity-results li.closest b { color: white; background: #c8102e; }
.similarity-results li strong { flex: 0 0 auto; color: #34363a; font: 700 clamp(.85rem,1.04vw,.94rem)/1 Georgia,'Times New Roman',serif; font-variant-numeric: tabular-nums; }
.similarity-results li.closest strong { color: #c8102e; }
.result-takeaway { width: min(100%,1180px); justify-self: center; display: grid; justify-items: center; gap: .18rem; padding-top: .42rem; border-top: 1px solid #dedbd4; text-align: center; }
.result-main-takeaway { margin: 0; color: #34363a; font: 600 clamp(1.08rem,1.65vw,1.38rem)/1.15 Georgia,'Times New Roman',serif; }
.result-caveat { margin: 0; color: #696b6d; font: 500 clamp(.72rem,.95vw,.84rem)/1.2 Inter,Aptos,Arial,sans-serif; }
@media (max-width:700px) {
  .first-result-slide { padding:.38rem .5rem .35rem; gap:.32rem; }
  .first-result-slide h1 { font-size:1.42rem; }
  .result-columns { grid-template-columns:minmax(0,.88fr) minmax(0,1.12fr); gap:.35rem; }
  .interpret-panel,.app-column { gap:.32rem; }
  .mode-block,.app-result-panel { padding:.42rem; }
  .interpret-panel > h2,.app-column > h2 { font-size:.74rem; }
  .mode-block { padding:.28rem; }
  .mode-heading { align-items:flex-start; flex-direction:column; gap:.1rem; }
  .mode-heading h3 { font-size:.7rem; }
  .mode-heading strong,.mode-description { font-size:.57rem; }
  .zero-profile b { font-size:.54rem; }
  .zero-profile small,.example-note { font-size:.48rem; }
  .percentile-example b,.percentile-example span { font-size:.54rem; }
  .reference-team { align-items:flex-start; flex-direction:column; gap:.12rem; padding:.32rem; }
  .reference-team span { font-size:.55rem; }
  .reference-team strong { font-size:.7rem; }
  .results-heading { margin:.26rem .2rem .08rem; font-size:.49rem; }
  .similarity-results li { min-height:1.55rem; padding:.18rem .2rem; font-size:.57rem; }
  .similarity-results li b { width:.9rem; height:.9rem; margin-right:.15rem; font-size:.52rem; }
  .similarity-results li strong { font-size:.62rem; }
  .result-main-takeaway { font-size:.9rem; }
  .result-caveat { font-size:.59rem; }
}
</style>

---
class: soccer-app-intro
layout: default
---

<main class="app-intro-slide">
  <h1>Explore the Soccer Similarity Score</h1>
  <div class="app-image-slot">
    <div v-click.fade-in="1" class="app-screenshot-frame">
      <img src="/shiny_app_demo_cropped.png" alt="PL Team Similarity Shiny app showing the mode selectors, four app tabs, Arsenal 2024/25 selected, and the Find Similar Teams controls" />
    </div>
  </div>
  <p v-click.fade-in="2" class="live-transition">Let's See It <em>Live</em></p>
</main>

<style>
.soccer-app-intro { color: #282a2d; background: #f7f5f0; }
.app-intro-slide { box-sizing: border-box; width: 100%; height: 100%; display: grid; grid-template-rows: auto minmax(0,1fr) auto; justify-items: center; align-items: center; gap: .62rem; padding: .62rem 1.25rem .78rem; }
.app-intro-slide h1 { margin: 0; color: #282a2d; font: 500 clamp(1.9rem,3.1vw,2.45rem)/1.1 Georgia,'Times New Roman',serif; letter-spacing: -.035em; text-align: center; }
.app-image-slot { box-sizing: border-box; width: 100%; min-height: 0; display: flex; justify-content: center; align-items: center; }
.app-screenshot-frame { box-sizing: border-box; width: min(94%,1540px); overflow: hidden; border: 1px solid #d9d5cd; border-radius: .34rem; background: #0d1117; box-shadow: 0 .45rem 1.2rem rgba(40,42,45,.11); }
.app-screenshot-frame img { display: block; width: 100%; height: auto; }
.live-transition { margin: 0; color: #34363a; font: 600 clamp(1.45rem,2.15vw,1.8rem)/1.15 Georgia,'Times New Roman',serif; text-align: center; }
.live-transition em { color: #c8102e; font-style: normal; }
@media (max-width:700px) {
  .app-intro-slide { padding:.42rem .55rem .48rem; gap:.38rem; }
  .app-intro-slide h1 { font-size:1.45rem; }
  .app-screenshot-frame { width:100%; }
  .live-transition { font-size:1.08rem; }
}
</style>

---
layout: default
class: live-demo-slide
---

<main class="live-demo-slide-content">
  <h1>Live Demonstration</h1>
  <iframe
    class="live-demo-iframe"
    src="https://01a19f24-88f6-03bf-2753-2acd4f51e0f7.share.connect.posit.cloud/"
    title="PL Team Similarity live Shiny application"
    scrolling="yes"
    loading="eager"
    referrerpolicy="strict-origin-when-cross-origin"
  ></iframe>
  <a
    class="live-demo-fallback"
    href="https://01a19f24-88f6-03bf-2753-2acd4f51e0f7.share.connect.posit.cloud/"
    target="_blank"
    rel="noopener noreferrer"
  >Open App in Browser</a>
</main>

<style>
.live-demo-slide { position: relative; box-sizing: border-box; width: 100%; height: 100%; overflow: hidden; color: #282a2d; background: #f7f5f0; }
.live-demo-slide-content { position: absolute; inset: 0; box-sizing: border-box; display: grid; grid-template-rows: auto minmax(0,1fr) auto; gap: .36rem; padding: .4rem .55rem .32rem; }
.live-demo-slide-content h1 { margin: 0; color: #282a2d; font: 500 clamp(1.55rem,2.45vw,2.05rem)/1.06 Georgia,'Times New Roman',serif; letter-spacing: -.03em; text-align: center; }
.live-demo-iframe { display: block; box-sizing: border-box; width: 100%; height: 100%; min-width: 0; min-height: 0; border: 1px solid #d9d5cd; border-radius: .32rem; background: #0d1117; }
.live-demo-fallback { justify-self: center; color: #77716c; font: 500 clamp(.64rem,.82vw,.76rem)/1.1 Inter,Aptos,Arial,sans-serif; text-decoration: underline; text-decoration-color: #c8102e; text-underline-offset: 2px; }
.live-demo-fallback:hover { color: #c8102e; }
@media (max-width:700px) {
  .live-demo-slide-content { gap:.24rem; padding:.25rem .3rem .22rem; }
  .live-demo-slide-content h1 { font-size:1.28rem; }
}
</style>

---
layout: default
class: soccer-deliverables
---

<main class="deliverables-slide">
  <h1>What Did This Project Produce?</h1>
  <section class="deliverables-grid" aria-label="Four project deliverables">
    <article v-click.fade-in="1" class="deliverable-card">
      <svg class="deliverable-icon dataset-icon" viewBox="0 0 100 76" role="img" aria-label="A small data table">
        <rect x="8" y="7" width="84" height="62" rx="4" fill="#fff" stroke="#9aa9b2" stroke-width="2" />
        <path d="M8 24h84M8 39h84M8 54h84M36 7v62M64 7v62" stroke="#b9c4ca" stroke-width="1.5" />
        <rect x="10" y="9" width="24" height="13" rx="1" fill="#c8102e" opacity=".82" />
        <rect x="38" y="26" width="24" height="11" rx="1" fill="#dce5e9" />
        <rect x="66" y="41" width="24" height="11" rx="1" fill="#dce5e9" />
        <rect x="10" y="56" width="24" height="11" rx="1" fill="#dce5e9" />
      </svg>
      <div class="deliverable-copy">
        <h2>Dataset</h2>
        <p>25 seasons, 500 team-seasons</p>
      </div>
    </article>
    <article v-click.fade-in="2" class="deliverable-card">
      <svg class="deliverable-icon similarity-icon" viewBox="0 0 100 76" role="img" aria-label="Two observations connected by a measured distance">
        <path d="M19 43H81" stroke="#85898a" stroke-width="2" />
        <path d="M24 38l-6 5 6 5M76 38l6 5-6 5" fill="none" stroke="#c8102e" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round" />
        <circle cx="18" cy="43" r="8" fill="#34363a" stroke="#f7f5f0" stroke-width="2" />
        <circle cx="82" cy="43" r="8" fill="#66869b" stroke="#f7f5f0" stroke-width="2" />
        <path d="M34 24h32" stroke="#c8102e" stroke-width="2.5" stroke-linecap="round" />
        <circle cx="50" cy="24" r="3" fill="#c8102e" />
      </svg>
      <div class="deliverable-copy">
        <h2>Similarity Score</h2>
        <p>A method for comparing statistical profiles</p>
      </div>
    </article>
    <article v-click.fade-in="3" class="deliverable-card">
      <svg class="deliverable-icon app-icon" viewBox="0 0 100 76" role="img" aria-label="A simple interactive application window">
        <rect x="9" y="9" width="82" height="58" rx="5" fill="#fff" stroke="#7f8d95" stroke-width="2" />
        <path d="M10 22h80" stroke="#c8102e" stroke-width="3" />
        <circle cx="18" cy="16" r="2" fill="#c8102e" />
        <circle cx="25" cy="16" r="2" fill="#b9c4ca" />
        <circle cx="32" cy="16" r="2" fill="#b9c4ca" />
        <rect x="18" y="31" width="25" height="26" rx="2" fill="#e8edf0" />
        <path d="M23 37h15M23 43h11M23 49h14" stroke="#8195a0" stroke-width="2" stroke-linecap="round" />
        <rect x="50" y="31" width="32" height="10" rx="2" fill="#dce5e9" />
        <rect x="50" y="47" width="22" height="10" rx="2" fill="#c8102e" opacity=".78" />
      </svg>
      <div class="deliverable-copy">
        <h2>Interactive App</h2>
        <p>A tool for exploring team similarities</p>
      </div>
    </article>
    <article v-click.fade-in="4" class="deliverable-card">
      <svg class="deliverable-icon paper-icon" viewBox="0 0 100 76" role="img" aria-label="A completed research paper">
        <path d="M28 7h32l16 16v46H28z" fill="#fff" stroke="#7f8d95" stroke-width="2" stroke-linejoin="round" />
        <path d="M60 7v17h16" fill="#f1efea" stroke="#7f8d95" stroke-width="2" stroke-linejoin="round" />
        <path d="M38 34h27M38 42h27M38 50h20M38 58h24" stroke="#9aa9b2" stroke-width="2" stroke-linecap="round" />
        <path d="M38 27h17" stroke="#c8102e" stroke-width="3" stroke-linecap="round" />
      </svg>
      <div class="deliverable-copy">
        <h2>Research Paper</h2>
        <p>A complete explanation of the project and its findings</p>
      </div>
    </article>
  </section>
</main>

<style>
.soccer-deliverables { color: #282a2d; background: #f7f5f0; }
.deliverables-slide { box-sizing: border-box; width: 100%; height: 100%; display: grid; grid-template-rows: auto minmax(0,1fr); align-items: stretch; gap: .62rem; padding: .58rem 1.35rem .62rem; }
.deliverables-slide > h1 { margin: 0; color: #282a2d; font: 500 clamp(1.9rem,3.1vw,2.45rem)/1.1 Georgia,'Times New Roman',serif; letter-spacing: -.035em; text-align: center; }
.deliverables-grid { box-sizing: border-box; width: min(100%,1160px); height: 100%; min-height: 0; justify-self: center; display: grid; grid-template-columns: repeat(2,minmax(0,1fr)); grid-template-rows: repeat(2,minmax(0,1fr)); gap: .92rem 1.08rem; }
.deliverable-card { box-sizing: border-box; min-width: 0; min-height: 0; display: flex; align-items: center; gap: 1.1rem; padding: 1.05rem 1.2rem; border: 1px solid #dedbd4; border-top: 2px solid #c8102e; border-radius: .36rem; background: rgba(255,255,255,.72); }
.deliverable-icon { display: block; width: clamp(4.8rem,8vw,6.25rem); height: auto; flex: 0 0 auto; overflow: visible; }
.deliverable-copy { min-width: 0; }
.deliverable-copy h2 { margin: 0 0 .34rem; color: #34363a; font: 600 clamp(1.1rem,1.55vw,1.28rem)/1.12 Georgia,'Times New Roman',serif; }
.deliverable-copy p { margin: 0; color: #55575b; font: 500 clamp(.82rem,1.08vw,.94rem)/1.3 Inter,Aptos,Arial,sans-serif; }
@media (max-width:700px) {
  .deliverables-slide { gap:.38rem; padding:.38rem .55rem .4rem; }
  .deliverables-slide > h1 { font-size:1.42rem; }
  .deliverables-grid { gap:.38rem; }
  .deliverable-card { flex-direction:column; justify-content:center; gap:.32rem; padding:.42rem; text-align:center; }
  .deliverable-icon { width:2.8rem; }
  .deliverable-copy h2 { margin-bottom:.12rem; font-size:.78rem; }
  .deliverable-copy p { font-size:.58rem; }
}
</style>

---
layout: default
class: limitations-improvements
---

<main class="limitations-slide">
  <h1>Limitations &amp; Future Improvements</h1>
  <div class="limitations-column-headings" aria-hidden="true">
    <h2>Current Limitations</h2>
    <span></span>
    <h2>Future Improvements</h2>
  </div>
  <section class="limitations-rows" aria-label="Current limitations and possible improvements">
    <article v-click.fade-in="1" class="limitation-row">
      <div class="limitation-side">
        <h3>Limited Available Statistics</h3>
      </div>
      <div class="limitation-arrow" aria-hidden="true">
        <svg viewBox="0 0 54 28"><path d="M3 14h43m-9-9 9 9-9 9" fill="none" stroke="#c8102e" stroke-width="3" stroke-linecap="round" stroke-linejoin="round" /></svg>
      </div>
      <div class="improvement-side">
        <h3>Collect More Detailed Soccer Data</h3>
        <p>Pressing, possession, and passing patterns</p>
      </div>
    </article>
    <article v-click.fade-in="2" class="limitation-row">
      <div class="limitation-side">
        <h3>Uneven Representation</h3>
      </div>
      <div class="limitation-arrow" aria-hidden="true">
        <svg viewBox="0 0 54 28"><path d="M3 14h43m-9-9 9 9-9 9" fill="none" stroke="#c8102e" stroke-width="3" stroke-linecap="round" stroke-linejoin="round" /></svg>
      </div>
      <div class="improvement-side">
        <h3>Choose a More Balanced Set of Statistics</h3>
        <p>Capture more aspects of team performance</p>
      </div>
    </article>
    <article v-click.fade-in="3" class="limitation-row">
      <div class="limitation-side">
        <h3>Premier League Only</h3>
      </div>
      <div class="limitation-arrow" aria-hidden="true">
        <svg viewBox="0 0 54 28"><path d="M3 14h43m-9-9 9 9-9 9" fill="none" stroke="#c8102e" stroke-width="3" stroke-linecap="round" stroke-linejoin="round" /></svg>
      </div>
      <div class="improvement-side">
        <h3>Explore Additional Leagues</h3>
        <p>Compare teams across more competitions</p>
      </div>
    </article>
  </section>
  <footer v-click.fade-in="4" class="limitations-takeaway">
    <p>Better data could bring us closer to measuring <em>playing style</em>.</p>
  </footer>
</main>

<style>
.limitations-improvements { color: #282a2d; background: #f7f5f0; }
.limitations-slide { box-sizing: border-box; width: 100%; height: 100%; display: grid; grid-template-rows: auto auto minmax(0,1fr) auto; gap: .52rem; padding: .58rem 1.35rem .62rem; }
.limitations-slide > h1 { margin: 0; color: #282a2d; font: 500 clamp(1.9rem,3.1vw,2.45rem)/1.1 Georgia,'Times New Roman',serif; letter-spacing: -.035em; text-align: center; }
.limitations-column-headings { width: min(100%,1160px); justify-self: center; display: grid; grid-template-columns: minmax(0,1fr) 3.4rem minmax(0,1.2fr); align-items: end; padding: 0 .95rem; }
.limitations-column-headings h2 { margin: 0; color: #55575b; font: 600 clamp(.88rem,1.18vw,1.02rem)/1.1 Georgia,'Times New Roman',serif; }
.limitations-column-headings h2:last-child { text-align: left; }
.limitations-rows { width: min(100%,1160px); height: 100%; min-height: 0; justify-self: center; display: grid; grid-template-rows: repeat(3,minmax(0,1fr)); gap: .56rem; }
.limitation-row { box-sizing: border-box; min-width: 0; min-height: 0; display: grid; grid-template-columns: minmax(0,1fr) 3.4rem minmax(0,1.2fr); align-items: center; padding: .65rem .95rem; border: 1px solid #dedbd4; border-left: 2px solid #c8102e; border-radius: .35rem; background: rgba(255,255,255,.7); }
.limitation-side,.improvement-side { min-width: 0; }
.limitation-row h3 { margin: 0; color: #34363a; font: 600 clamp(1rem,1.48vw,1.22rem)/1.2 Georgia,'Times New Roman',serif; }
.improvement-side h3 { color: #34363a; }
.improvement-side p { margin: .28rem 0 0; color: #66686b; font: 500 clamp(.78rem,1.02vw,.9rem)/1.25 Inter,Aptos,Arial,sans-serif; }
.limitation-arrow { display: grid; place-items: center; transform: translateX(-1rem); }
.limitation-arrow svg { display: block; width: 2.8rem; height: 1.55rem; overflow: visible; }
.limitations-takeaway { width: min(100%,1160px); justify-self: center; padding-top: .45rem; border-top: 1px solid #dedbd4; text-align: center; }
.limitations-takeaway p { margin: 0; color: #34363a; font: 600 clamp(1.1rem,1.65vw,1.34rem)/1.15 Georgia,'Times New Roman',serif; }
.limitations-takeaway em { color: #c8102e; font-style: normal; }
@media (max-width:700px) {
  .limitations-slide { gap:.35rem; padding:.36rem .55rem .4rem; }
  .limitations-slide > h1 { font-size:1.42rem; }
  .limitations-column-headings { grid-template-columns:minmax(0,1fr) 1.65rem minmax(0,1fr); padding:0 .35rem; }
  .limitations-column-headings h2 { font-size:.65rem; }
  .limitations-rows { gap:.32rem; }
  .limitation-row { grid-template-columns:minmax(0,1fr) 1.65rem minmax(0,1fr); padding:.38rem .35rem; }
  .limitation-row h3 { font-size:.7rem; }
  .improvement-side p { margin-top:.14rem; font-size:.57rem; }
  .limitation-arrow { transform: translateX(-.25rem); }
  .limitation-arrow svg { width:1.45rem; height:1rem; }
  .limitations-takeaway { padding-top:.25rem; }
  .limitations-takeaway p { font-size:.82rem; }
}
</style>

---
layout: default
class: presentation-finale
---

<main class="finale-slide">
  <h1 class="finale-heading">Back to the Beginning</h1>
  <section class="finale-message" aria-label="Closing message">
    <div class="finale-question-wrap">
      <p class="finale-question">If Arsenal are so boring, who else is?</p>
    </div>
    <div v-click.fade-in="1" class="finale-conclusion">
      <div class="finale-divider" aria-hidden="true"></div>
      <p><span class="finale-line">One question about Arsenal became a new way to compare</span>
        <span class="finale-line"><span class="finale-red">25 seasons</span> of Premier League teams.</span></p>
    </div>
    <p v-click.fade-in="2" class="finale-deliverables">Similarity Score <span aria-hidden="true">•</span> Research Paper <span aria-hidden="true">•</span> Shiny App</p>
  </section>
</main>

<style>
.presentation-finale { color:#282a2d; background:#f7f5f0; }
.finale-slide { box-sizing:border-box; width:100%; height:100%; display:flex; flex-direction:column; align-items:center; padding:2.2rem 5rem 1.8rem; }
.finale-heading { margin:0; color:#55575b; font:500 clamp(1.12rem,1.8vw,1.42rem)/1.2 Georgia,'Times New Roman',serif; text-align:center; }
.finale-message { flex:1; min-height:0; width:100%; display:flex; flex-direction:column; align-items:center; justify-content:center; padding-top:.5rem; text-align:center; }
.finale-question-wrap { position:relative; width:min(100%,1000px); margin:0 auto 2.5rem; padding:.5rem 0; }
.finale-question-wrap::before,.finale-question-wrap::after { position:absolute; z-index:0; color:rgba(200,16,46,.20); font:500 clamp(7rem,13vw,10.5rem)/.7 Georgia,'Times New Roman',serif; pointer-events:none; }
.finale-question-wrap::before { content:'“'; left:13%; top:50%; transform:translateY(-50%); }
.finale-question-wrap::after { content:'”'; right:13%; top:50%; transform:translateY(-50%); }
.finale-question { position:relative; z-index:1; margin:0; padding:0 clamp(3rem,8vw,6rem); color:#282a2d; font:500 clamp(2.2rem,4.25vw,3.45rem)/1.16 Georgia,'Times New Roman',serif; letter-spacing:-.025em; }
.finale-conclusion { width:min(100%,1000px); }
.finale-divider { width:min(100%,390px); height:2px; margin:0 auto 1.35rem; background:#c8102e; }
.finale-conclusion p { margin:0; color:#34363a; font:500 clamp(1.48rem,2.5vw,2.06rem)/1.3 Georgia,'Times New Roman',serif; }
.finale-line { display:block; }
.finale-red { color:#c8102e; }
.finale-deliverables { margin:1.55rem 0 0; color:#55575b; font:500 clamp(.85rem,1.15vw,1rem)/1.25 Inter,Aptos,Arial,sans-serif; letter-spacing:.025em; text-align:center; }
@media (max-width:700px) {
  .finale-slide { padding:1.2rem 1rem 1.1rem; }
  .finale-heading { font-size:1rem; }
  .finale-question-wrap { margin-bottom:1.7rem; }
  .finale-question-wrap::before,.finale-question-wrap::after { font-size:5.5rem; }
  .finale-question { padding:0 2.2rem; font-size:2rem; }
  .finale-divider { margin-bottom:1rem; }
  .finale-conclusion p { font-size:1.22rem; }
  .finale-deliverables { margin-top:1rem; font-size:.78rem; }
}
</style>

---
layout: default
class: final-qa
---

<main class="final-qa-slide">
  <h1>Thank you</h1>
  <section class="final-qa-center" aria-label="Questions and project title">
    <h2>Questions?</h2>
    <div class="final-qa-divider" aria-hidden="true"></div>
    <p class="final-qa-project">Soccer Similarity Score</p>
  </section>
</main>

<style>
.final-qa { color:#282a2d; background:#f7f5f0; }
.final-qa-slide { box-sizing:border-box; width:100%; height:100%; display:flex; flex-direction:column; align-items:center; padding:2.35rem 4rem 2rem; }
.final-qa-slide > h1 { margin:0; color:#55575b; font:500 clamp(1.15rem,1.8vw,1.45rem)/1.2 Georgia,'Times New Roman',serif; text-align:center; }
.final-qa-center { flex:1; min-height:0; width:100%; display:flex; flex-direction:column; justify-content:center; align-items:center; text-align:center; padding-bottom:1.2rem; }
.final-qa-center h2 { margin:0; color:#282a2d; font:500 clamp(3.4rem,7vw,5.6rem)/1.08 Georgia,'Times New Roman',serif; letter-spacing:-.035em; }
.final-qa-divider { width:min(22vw,230px); height:2px; margin:1.7rem auto 1.25rem; background:#c8102e; }
.final-qa-project { margin:0; color:#34363a; font:500 clamp(1.45rem,2.35vw,1.95rem)/1.25 Georgia,'Times New Roman',serif; }
@media (max-width:700px) {
  .final-qa-slide { padding:1.2rem 1rem 1.1rem; }
  .final-qa-center h2 { font-size:3rem; }
  .final-qa-project { font-size:1.3rem; }
}
</style>

---
src: ./pages/rigor-faq.md
---
