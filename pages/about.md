---
layout: page
menu: false
date: '2025-09-10 01:53:59'
title: About
description: Some description.
permalink: /about/
---

<style>
/* Scoped dark overhaul — only loads on /about/, so page-wrapper selectors
   here never touch the home page or posts. Matches jekflix theme red #ff0a16. */
.content,
.content .post,
.content .post-content.fullwidth {
  background-color: #141414;
  color: #f2f2f2;
}
.content .post-content.fullwidth {
  max-width: 860px;
  margin: 0 auto;
}
/* Theme sets .post-content p/li to #333 (for light pages) — override for dark. */
.content .post-content p,
.content .post-content li { color: #e6e6e6; }
.content .post-content .about-lead p { color: #d9d9d9; }
.content .post-content a {
  color: #ff0a16;
  transition: color .2s ease;
}
.content .post-content a:hover { color: #ff4d57; }

.content .post-content h1 {
  color: #ffffff;
  border-bottom: 2px solid #ff0a16;
  padding-bottom: .25em;
  margin-top: 1.6em;
}

/* Intro / bio */
.about-intro {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  gap: 28px;
  margin: 8px 0 4px;
}
.about-intro img {
  width: 180px;
  height: 250px;
  object-fit: cover;
  border-radius: 14px;
  box-shadow: 0 0 0 3px rgba(255, 10, 22, .55), 0 10px 30px rgba(0, 0, 0, .6);
  flex: 1 0 auto;
  margin-left: 30px;
}
.about-lead { flex: 1 1 320px; }
.about-lead .role-tag {
  display: inline-block;
  font-size: 13px;
  letter-spacing: .14em;
  text-transform: uppercase;
  color: #ff0a16;
  font-weight: 700;
  margin-bottom: 6px;
}
.about-lead h2 {
  color: #ffffff;
  font-size: 30px;
  margin: 0 0 10px;
}

/* Section micro-heading (reuses role-tag look as a standalone label) */
.section-label {
  display: block;
  font-size: 13px;
  letter-spacing: .14em;
  text-transform: uppercase;
  color: #ff0a16;
  font-weight: 700;
  margin: 22px 0 2px;
}

/* Skills strip */
.skills-strip {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  margin: 18px 0 8px;
}
/* Core stack: filled accent-bordered pills (visually dominant) */
.skills-strip .skill {
  background-color: #1c1c1c;
  border: 1px solid #ff0a16;
  color: #f2f2f2;
  font-size: 13px;
  font-weight: 600;
  padding: 6px 13px;
  border-radius: 999px;
}

/* Experience timeline */
.xp-timeline {
  position: relative;
  margin: 10px 0 30px;
  padding-left: 30px;
}
.xp-timeline::before {
  content: "";
  position: absolute;
  left: 7px;
  top: 6px;
  bottom: 6px;
  width: 3px;
  border-radius: 3px;
  background: linear-gradient(180deg, #ff0a16 0%, #700005 100%);
}
.xp-card {
  position: relative;
  background-color: #1c1c1c;
  border: 1px solid #2a2a2a;
  border-radius: 12px;
  padding: 20px 22px;
  margin-bottom: 22px;
  box-shadow: 0 6px 22px rgba(0, 0, 0, .5), 0 0 0 1px rgba(255, 10, 22, .05);
  transition: transform .2s ease, box-shadow .2s ease, border-color .2s ease;
}
.xp-card:hover {
  transform: translateY(-2px);
  border-color: rgba(255, 10, 22, .5);
  box-shadow: 0 10px 30px rgba(0, 0, 0, .6), 0 0 18px rgba(255, 10, 22, .12);
}
.xp-card::before {
  content: "";
  position: absolute;
  left: -30px;
  top: 24px;
  width: 13px;
  height: 13px;
  border-radius: 50%;
  background-color: #ff0a16;
  box-shadow: 0 0 0 4px #141414, 0 0 10px rgba(255, 10, 22, .8);
}
.xp-head {
  display: flex;
  flex-wrap: wrap;
  align-items: baseline;
  justify-content: space-between;
  gap: 4px 14px;
}
.xp-head .company {
  color: #ffffff;
  font-size: 20px;
  font-weight: 700;
}
.xp-head .company .sub {
  color: #a6a6a6;
  font-weight: 400;
  font-size: 15px;
}
.xp-head .dates {
  color: #a6a6a6;
  font-size: 14px;
  font-variant-numeric: tabular-nums;
  white-space: nowrap;
}
.xp-card .logo {
  display: block;
  width: 110px;
  height: auto;
  margin: 4px 0 14px auto;
}

/* "Now" badge for currently-active roles */
.now-badge {
  display: inline-block;
  vertical-align: middle;
  margin-left: 8px;
  font-size: 11px;
  font-weight: 700;
  letter-spacing: .08em;
  text-transform: uppercase;
  color: #ff4d57;
  background-color: rgba(255, 10, 22, .12);
  border: 1px solid rgba(255, 10, 22, .5);
  border-radius: 999px;
  padding: 2px 9px;
}
.now-badge::before {
  content: "";
  display: inline-block;
  width: 7px;
  height: 7px;
  margin-right: 6px;
  border-radius: 50%;
  background-color: #ff0a16;
  box-shadow: 0 0 6px rgba(255, 10, 22, .9);
  vertical-align: middle;
  animation: now-pulse 1.8s ease-in-out infinite;
}
@keyframes now-pulse {
  0%, 100% { opacity: 1; transform: scale(1); }
  50% { opacity: .45; transform: scale(.7); }
}

.xp-bullets {
  list-style: none;
  margin: 14px 0 0;
  padding: 0;
}
.xp-bullets li {
  position: relative;
  padding-left: 22px;
  margin-bottom: 9px;
  color: #d9d9d9;
  line-height: 1.55;
}
.xp-bullets li::before {
  content: "\25B8";
  position: absolute;
  left: 0;
  color: #ff0a16;
  font-size: 14px;
  top: 1px;
}

/* Role progression sub-entries (DWA) */
.xp-roles {
  list-style: none;
  margin: 14px 0 0;
  padding: 0;
  border-top: 1px solid #2a2a2a;
}
.xp-roles li {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  gap: 4px 12px;
  padding: 11px 0;
  border-bottom: 1px solid #242424;
}
.xp-roles .role-name {
  color: #f2f2f2;
  font-weight: 600;
}
.xp-roles .role-dates {
  color: #a6a6a6;
  font-size: 14px;
  font-variant-numeric: tabular-nums;
}

/* Tech tag chips */
.tech-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 8px;
  margin-top: 16px;
}
/* Per-role tech: muted outline pills (same shape as skills, lower emphasis) */
.tech-tags .tag {
  font-size: 12px;
  font-weight: 600;
  letter-spacing: .02em;
  color: #cccccc;
  background-color: transparent;
  border: 1px solid #3a3a3a;
  border-radius: 999px;
  padding: 4px 11px;
}

@media (max-width: 600px) {
  .about-intro img { width: 140px; height: 140px; }
  .xp-head .dates { white-space: normal; }
}

@media (prefers-reduced-motion: reduce) {
  .xp-card,
  .content .post-content a { transition: none; }
  .xp-card:hover { transform: none; }
  .now-badge::before { animation: none; }
}
</style>

<div class="about-intro" markdown="0">
  <img src="images/me.jpg" alt="Dave Louie Roxas">
  <div class="about-lead">
    <h2>Hi, I'm Dave Roxas</h2>
    <p>Senior game engineer with 8+ years building and shipping gameplay systems, tools, and audio pipelines in <strong>Unity/C#</strong>. Progressed from QA through to senior engineering at a single studio, with a track record of designing scalable, multi-platform systems and partnering across design, audio, and content teams.</p>
  </div>
</div>

Recently expanded into web and iGaming development, shipping WebGL and browser-based games using TypeScript, Svelte, and Pixi.js. Strong in systems design, prototyping, and developer tooling, with deep experience in version control, performance optimization, and modern engineering practices.

I'm also a **strong team player** who thrives in **collaborative environments**. Great games are made by great teams, and I always strive to bring out the best in the people I work with.

<span class="section-label" markdown="0">Core Stack</span>

<div class="skills-strip" markdown="0">
  <span class="skill">C#</span>
  <span class="skill">Unity</span>
  <span class="skill">Luau</span>
  <span class="skill">TypeScript</span>
  <span class="skill">Roblox / Rojo</span>
  <span class="skill">Svelte</span>
  <span class="skill">Pixi.js</span>
  <span class="skill">Phaser</span>
  <span class="skill">Zenject</span>
  <span class="skill">UniTask</span>
  <span class="skill">FMOD</span>
  <span class="skill">Tools & Engine Dev</span>
</div>

# Experiences

<div class="xp-timeline" markdown="0">

  <div class="xp-card">
    <div class="xp-head">
      <span class="company">Independent Game Developer — Personal R&amp;D <span class="sub">(iGaming Technologies)</span></span>
      <span class="dates">Jan 2026 – Present <span class="now-badge">Now</span></span>
    </div>
    <ul class="xp-bullets">
      <li>Conducted independent research and rapid prototyping of web-based and WebGL game architectures using Unity, Svelte, Pixi.js, and Phaser, evaluating performance, scalability, maintainability, and deployment strategies across stacks.</li>
      <li>Explored advanced Unity patterns including finite state machine (FSM) architectures, dependency injection with Zenject, asynchronous programming with UniTask, and modular framework design for reusable gameplay systems.</li>
      <li>Researched and implemented asset delivery solutions for WebGL deployments, including Unity Addressables, remote content streaming, asset bundle optimization, and theme-based content management workflows.</li>
      <li>Experimented with slot, reel-based, and grid-based game mechanics using the Stake SDK — configurable math models, cascading win systems, symbol event pipelines, reel behavior simulations, and player feedback systems.</li>
      <li>Investigated frontend architecture patterns using Svelte and TypeScript, focusing on reactive state management, event-driven design, animation systems, audio orchestration, and scalable UI frameworks.</li>
      <li>Evaluated approaches for deterministic financial calculations, implementing micro-unit and integer-based currency models to eliminate floating-point precision issues.</li>
      <li>Built proof-of-concept tools and experimental frameworks for game configuration, deployment automation, content pipelines, runtime extensibility, and rapid feature iteration.</li>
      <li>Researched integration patterns and technical requirements for RGS-connected gaming platforms, including game lifecycle management, platform interoperability, and deployment workflows.</li>
    </ul>
    <div class="tech-tags">
      <span class="tag">Unity LTS (C#)</span>
      <span class="tag">Zenject</span>
      <span class="tag">UniTask</span>
      <span class="tag">Svelte</span>
      <span class="tag">TypeScript</span>
      <span class="tag">Pixi.js 8</span>
      <span class="tag">Phaser 3</span>
      <span class="tag">Vite</span>
      <span class="tag">Pnpm</span>
      <span class="tag">FMOD</span>
    </div>
  </div>

  <div class="xp-card">
    <div class="xp-head">
      <span class="company">Ranida Games</span>
      <span class="dates">Oct 2025 – Jun 2026</span>
    </div>
    <ul class="xp-bullets">
      <li>Designed and shipped multiple Roblox games across distinct genres — a co-op zombie shooter with roguelike progression, a team-based sniper FPS, and a beach idle/tycoon with treasure hunting and crafting.</li>
      <li>Architected full client-server multiplayer systems using Roblox's RemoteEvent model, enforcing server authority while keeping clients responsive.</li>
      <li>Built a modular inventory, crafting, and quest progression system with DataStore persistence and versioned schema migration.</li>
      <li>Developed a procedural terrain chunk system and a wave-based NPC survival mode with configurable per-type behavior.</li>
      <li>Created reusable UI systems — inventory, reward announcements, cosmetics, and a generic window package.</li>
    </ul>
    <div class="tech-tags">
      <span class="tag">Roblox Studio</span>
      <span class="tag">Luau</span>
      <span class="tag">Rojo</span>
    </div>
  </div>

  <div class="xp-card">
    <div class="xp-head">
      <span class="company">Dusk Wave Arts <span class="sub">(DWA)</span></span>
      <span class="dates">Aug 2017 – Oct 2025 · 8 yrs 2 mos</span>
    </div>
    <img class="logo" src="images/dwa.png" alt="Dusk Wave Arts">
    <ul class="xp-roles">
      <li><span class="role-name">Senior Game Engineer</span><span class="role-dates">Mar 2024 – Oct 2025 · 1 yr 7 mos</span></li>
      <li><span class="role-name">Game Engineer</span><span class="role-dates">Nov 2022 – Mar 2024 · 1 yr 5 mos</span></li>
      <li><span class="role-name">Quality Assurance</span><span class="role-dates">Sep 2017 – Nov 2022 · 5 yrs 3 mos</span></li>
      <li><span class="role-name">Junior Game Developer</span><span class="role-dates">Aug 2017 – Nov 2022 · 5 yrs 4 mos</span></li>
    </ul>
  </div>

</div>
