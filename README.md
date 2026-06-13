# Tiny Lives — a cozy little life simulator

A complete, playable life-simulation game (think *The Sims*, shrunk down) that runs entirely in your browser from **one single HTML file**. No installation, no internet, no dependencies — just double-click `life-sim.html` and play.

> **Made by Claude Fable 5 — in 1 prompt, in about 1 hour.**
> The entire game (≈1,860 lines of HTML, CSS and JavaScript) was generated,
> tested in a real browser, debugged and delivered from a single request.

---

## ▶ How to play

1. Double-click **`life-sim.html`** (any modern browser: Chrome, Edge, Firefox).
2. **New Game → pick a lot** on the neighborhood map.
3. Move into a **furnished house** (Cozy Cottage / Family Home / Modern Loft) or
   start from an **empty plot** and build it yourself.
4. **Create your household** — as many Sims as you like.
5. Click a Sim to select them, click objects or other Sims to give commands, and
   keep everyone's needs in the green.

**Controls:** click a Sim to select • click furniture → choose an action •
click another Sim → Talk / Joke / Argue • `Space` pause • `1` / `3` speed •
`B` build mode • `Esc` close menus.

---

## What's in it

- **Main menu, neighborhood map and lot selection** with animated transitions.
- **Sim Creator:** name, gender, 6 skin tones, 5 hairstyles, 8 hair colors,
  10 outfit colors, and 3 personality traits from a list of 10.
- **Live mode:** top-down 2D house, 5 needs (Hunger, Energy, Hygiene, Fun,
  Social), mood, a day/night cycle that actually darkens the lot, and
  interactable objects (bed, fridge, shower, toilet, sink, TV, bookshelf, sofa…).
- **Personality that matters:** traits change need-decay rates *and* autonomous
  behavior — a Foodie eats more often, a Bookworm gravitates to the bookshelf,
  a Grumpy Sim argues and stays moodier.
- **Social system:** Talk / Joke / Argue between Sims, with a relationship meter.
- **Build & Buy mode:** paint walls, drag out rooms on a grid, place and delete
  furniture from categorized panels, with a working in-game economy (§).
- **100% Canvas 2D art** — every Sim, wall and appliance is drawn in code. No
  image files, no sprite sheets, no external assets.

---

## ✅ Why it's great

- **Truly zero-install / zero-dependency.** One file, no build step, no server,
  no CDN, no internet. It works offline and you can email it to someone.
- **Surprisingly complete.** Menu → map → creator → live mode → build mode is a
  full gameplay loop, not a tech demo stub.
- **Traits aren't cosmetic.** They visibly drive both stat decay and what Sims
  choose to do on their own.
- **Self-contained and portable.** Runs the same on any machine with a browser;
  nothing to keep up to date.
- **Procedural art.** Because everything is drawn with Canvas primitives, the
  whole game is just text — easy to read, copy, and tweak.
- **Built and verified fast.** Generated, syntax-checked, and play-tested in an
  actual browser inside a single session.

## ⚠️ Cons & limitations

Be fair about what a "one file, one prompt" game is and isn't:

- **No save/load.** State lives in memory — refreshing the page restarts the
  game. There's no persistence.
- **Everything's in one file.** ~1,860 lines of HTML/CSS/JS together is great for
  portability but harder to maintain or extend than a modular codebase.
- **Simple AI.** Autonomous behavior is utility-based and can look repetitive;
  Sims occasionally path awkwardly or bunch up (no Sim-to-Sim collision).
- **Rough balancing.** Need-decay rates and the economy were set by feel, not
  tuned through real playtesting. Money only goes *down* — there are no jobs or
  income yet.
- **No audio.** No music or sound effects.
- **No life progression.** No aging, careers, skills growth or life stages — it's
  a needs-and-build sandbox, not a full life-story sim.
- **Geometric / emoji art.** Charming and consistent, but not detailed sprite art.
- **Desktop-mouse oriented.** The canvas scales, but it isn't designed for touch.
- **Not micro-optimized.** It redraws the whole canvas each frame and recomputes
  pathfinding on demand — fine at this scale, not built for huge lots or crowds.
- **Generated in one pass.** It was tested, but edge cases that weren't exercised
  during that testing may still surface. Treat it as a polished proof-of-concept,
  not a shipped product.

---

## 🛠 Tech

Plain **HTML + CSS + JavaScript**, rendered on a single **`<canvas>`** with the
2D context. No frameworks, no libraries, no external files. BFS grid
pathfinding, a fixed-timestep-ish game loop driven by `requestAnimationFrame`,
and a small utility-AI for Sim autonomy.

*Built by Claude Fable 5 · single prompt · ~1 hour.*
