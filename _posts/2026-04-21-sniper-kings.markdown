---
layout: post
title:  "Sniper Kings"
subtitle: "Sniper Kings is a pure skill-based sniper experience built for players who want real, focused combat."
description: Sniper Kings is a pure skill-based sniper experience built for players who want real, focused combat.
image: /games/2026/04/21/SK1.webp
date:   2026-04-21 15:08:22 +0800
categories: games
category: games
tags:
- Shooter
- Deathmatch
author: "Ranida Games"
paginate: false
role: "Lua Scripter"
---

{% include post-game-styles.html %}

<div class="post-cta-bar">
  <a href="https://www.roblox.com/games/108480515793043/Sniper-Kings" class="cta-btn cta-primary">Play on Roblox</a>
</div>

<div class="post-meta-card">
  <div class="meta-col">
    <h3 class="meta-label">Role</h3>
    <p>{{ page.role }}</p>
  </div>
  <div class="meta-col">
    <h3 class="meta-label">Tools &amp; Tech</h3>
    <ul class="tool-list">
      <li>Roblox Studio</li>
      <li>Luau</li>
      <li>Rojo</li>
    </ul>
  </div>
</div>

<span class="section-label">My Contribution</span>

Built the "Troll" event system (Nuke, Big Head, Wave trolls) with chat/popup announcements and contributed to the gacha spin-the-wheel feature.

### Feature Implementation

- **Troll system** — `TrollService` with **Nuke Troll** (launch SFX, temporary sphere-part explosion VFX, tuned explosion radius), **Big Head Troll**, and **Wave Troll** (wave distance/collision tuning so trolled players stay reachable).
- **TrollAnnouncementHandler** — chat + popup announcements for troll events.
- **Spin-the-wheel** — booster service client; integration/sync work around the spin wheel feature.

### Notable fixes & involvements
- RoundUI client typo fixes, removed a rogue `MarketplaceService:GetProductInfo` call, Selene config, repeated Studio↔Rojo place syncs.

<hr class="section-divider">

<span class="section-label">About the Game</span>

Sniper Kings is a pure skill-based sniper experience built for players who want real, focused combat.

Inspired by classic sniper-only battles, two teams face off head-on — no cheap flanks, no surprise attacks. Just positioning, precision, and raw aim.

Lock in your target and take the shot. No roaming around. No getting picked off by hidden campers. Here, you face your enemy head-on.

![Image](/games/2026/04/21/SK2.webp)

Every move matters. Every shot counts. In here, the sniper is king.

- Headshots are heavily rewarded
- Master positioning and long-range duels
- Collect sniper rifles of different rarities
- Customize your playstyle with unique scopes
- Fast-paced, action-packed team battles
