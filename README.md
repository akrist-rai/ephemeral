<div align="center">

```
███████╗██████╗ ██╗  ██╗███████╗███╗   ███╗███████╗██████╗  █████╗ ██╗
██╔════╝██╔══██╗██║  ██║██╔════╝████╗ ████║██╔════╝██╔══██╗██╔══██╗██║
█████╗  ██████╔╝███████║█████╗  ██╔████╔██║█████╗  ██████╔╝███████║██║
██╔══╝  ██╔═══╝ ██╔══██║██╔══╝  ██║╚██╔╝██║██╔══╝  ██╔══██╗██╔══██║██║
███████╗██║     ██║  ██║███████╗██║ ╚═╝ ██║███████╗██║  ██║██║  ██║███████╗
╚══════╝╚═╝     ╚═╝  ╚═╝╚══════╝╚═╝     ╚═╝╚══════╝╚═╝  ╚═╝╚═╝  ╚═╝╚══════╝
```

**A manga/anime-inspired CTF learning platform for CS concepts.**  
*Learn by exploring. Prove it in the arena. Score like Balatro.*

![License](https://img.shields.io/badge/license-MIT-red?style=flat-square)
![Status](https://img.shields.io/badge/status-early_prototype-lime?style=flat-square&color=00ff41)
![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen?style=flat-square)
![Vibe Coded](https://img.shields.io/badge/frontend-vibe_coded-orange?style=flat-square)

</div>

---

## The Problem

CS students grind LeetCode and DSA — important, but it creates tunnel vision. **Most never explore the rest of computer science**: systems programming, security, networks, probability, ML internals, compilers. Not because they don't want to. Because nobody made it feel worth exploring.

Ephemeral is the fix.

---

## How It Works

Every topic on Ephemeral follows the same three-act structure:

### Act 1 — The Question
Every episode starts with a *child's question*. Something embarrassingly simple on the surface:

> *"Mommy, what is a file descriptor?"*
> *"Mommy, why does Dijkstra fail on negative weights?"*
> *"Mommy, what made the Transformer the last one standing?"*

You don't know the answer. That's the point. **Go find out.**

### Act 2 — The Resources
A short, **ordered** reading list (papers, articles, videos). Not a pile of links — a curriculum. ~30–60 minutes per episode. Enough to actually understand the concept, not just recognise the name.

### Act 3 — The CTF Arena (Balatro-style)
Here's where it gets different.

Instead of a standard CTF submission page, you play a **roguelike card game** — mechanically inspired by [Balatro](https://www.playbalatro.com/):

- You're dealt a **hand of concept cards**. Each card has **chips** (base score) and a **mult** (multiplier).
- Score = `chips × mult`. Hit the blind's target to advance.
- **Jokers** modify your run: *"First wrong answer each blind is free"*, *"Playing exactly 1 card: +60 chips"*, *"Carry +0.5 mult into the next challenge"*.
- **Boss Blind** disables hints. The monster is watching.
- Challenges are real: reverse-engineer a model config, name the inductive bias in a code block, derive an architecture output. Not multiple choice.

The learning is real. The scoring is a game.

---

## Thematic Structure

Each CS domain is wrapped in a **manga/anime series** — not just cosplay, but a narrative lens that gives episodes stakes and flavour:

| Series | Domain | Inspiration |
|--------|--------|-------------|
| **The Eclipse** | Algorithms | Berserk |
| **Grand Line** | Cybersecurity | One Piece |
| **Johan's Labyrinth** | Machine Learning | Monster |
| **The Knot** | Networks | Dark |
| **Book of Prophecy** | Data Structures | 20th Century Boys |
| **One Punch Grind** | Competitive Programming | One Punch Man |
| **Instrumentality** | Mathematics | Evangelion |
| **El Psy Congroo** | Probability | Steins;Gate |

---

## Current State

> ⚠️ **Early prototype.** Single HTML file, vibe-coded frontend, no backend yet. The bones are real.

**What works right now:**
- Full home screen with series manifest
- Series page with arc/season navigation
- Episode detail page (Brief → Resources → CTF Arena)
- One complete episode: *"Ruhenheim — Why Transformers Dominate Vision"* (ML series, S2E3)
- Working Balatro card game with: score engine, joker tray, shop, 3 blinds (Entry → Core → Boss), hint system, XP and result screen

**What's needed:**
- React/SvelteKit migration (it's one giant HTML file right now)
- Backend: auth, progress tracking, user XP/run state
- Content: more episodes across all 8 domains
- Mobile polish

---

## Tech Stack (Planned)

| Layer | Stack |
|-------|-------|
| Frontend | Vite + React or SvelteKit |
| Backend | Bun + Koa (or Hono) |
| DB | Supabase + Drizzle ORM |
| Auth | JWT / Supabase Auth |
| Deployment | TBD |

---

## Contributing

**This is an open call. Ephemeral needs people.**

You don't have to be a developer to contribute. Here's what's most useful right now:

### 📝 Content Authors
Write an episode for a domain you know. Format:
1. One "Mommy, what is X?" question
2. An ordered reading list (3–6 resources, with notes on what to focus on)
3. 3–5 CTF challenges with: setup text, code artifact/config, flag (exact answer), hint, explanation

Open an issue with `[CONTENT]` in the title and the domain/concept you want to cover.

### ⚛️ Frontend Developers
The prototype needs to become a real app. React, SvelteKit, whatever you're fluent in — I can handle backend. Take a look at `ephemeral.html` to understand the component structure and design system (CSS variables, class naming, etc.).

### 🎮 Game Design
The Balatro mechanic is rough. Is it fun? Does it get in the way of learning? What would make the card/joker economy more meaningful? Open an issue with `[GAME]`.

### 🔍 Domain Experts
If you know systems internals, compiler design, formal probability, cryptography, or anything deep — come help design the arc structure. The curriculum side matters as much as the code.

---

## Running It

For now, just open `ephemeral.html` in a browser. No build step, no server.

```bash
git clone https://github.com/akrist-rai/ephemeral
cd ephemeral
open ephemeral.html   # or just drag into browser
```

---

## Why "Ephemeral"?

The platform shouldn't matter. The learning should outlast it. You'll forget the card game mechanics. You won't forget what a file descriptor is after you've had to prove it under a timer.

Also: this might go nowhere. But the idea is worth building.

---

## License

MIT — take it, fork it, build on it.

---

<div align="center">
<sub>Built by <a href="https://github.com/akrist-rai">akrist-rai</a> · Currently seeking contributors · Open issues welcome</sub>
</div>
