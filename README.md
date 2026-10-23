# 🎡 Wheel of Impossible Destiny

> **"A highly questionable decision device. No skill required. No appeals accepted. Your fate is about to get weird."**  
> *Fate Engine Vol. 01*

---

## 📖 Overview

**Wheel of Impossible Destiny** is a cyberpunk, dark-arcade-styled interactive web application that leaves life's critical decisions to the whims of the cosmos. Built with pure HTML5 Canvas, modern CSS, and the native Web Audio API, the app pairs procedural visual effects, tactile synth sound design, and sharp typography with 12 absurd, cosmic prophecies.

---

## ✨ Features

### 🎯 1. Interactive Canvas Destiny Wheel
- **Crisp High-DPI Rendering**: Dynamic canvas scaling according to `window.devicePixelRatio` for razor-sharp sector rendering on Retina and 4K displays.
- **Physical Rotation Physics**: Custom quartic ease-out curve (`1 - (1 - t)^4.4`) simulating realistic momentum, friction, and deceleration across 6–8 full revolutions.
- **Exact Landing Precision**: Mathematically aligns the target slice center directly beneath the neon pointer upon deceleration.

### 🔮 2. The 12 Cosmic Fates
Every spin resolves into one of twelve predetermined prophecies:

| # | Tag | Fate Prophecy | Accent Color |
|---|---|---|---|
| `01` | **PUDDLE MAYOR** | *You are now the mayor of a very small puddle.* | `#d5ff3f` (Acid Green) |
| `02` | **GOOSE ENEMY** | *A goose has added you to its enemies list.* | `#ff6682` (Hot Pink) |
| `03` | **MULTIVERSE HAIR** | *You have excellent hair in every alternate universe.* | `#a88cff` (Violet) |
| `04` | **SOCK PROPHECY** | *Your left sock knows the entire truth.* | `#65dfea` (Cyan) |
| `05` | **POCKET SYMPHONY** | *A tiny orchestra will follow you for a day.* | `#ff9a5e` (Orange) |
| `06` | **LUNAR DEBT** | *You owe the moon one sincere compliment.* | `#d5ff3f` (Acid Green) |
| `07` | **CHAIR APPROVAL** | *The next chair you meet is mildly impressed.* | `#ff6682` (Hot Pink) |
| `08` | **FRIENDLY CRYPTID** | *You become a cryptid, but a very approachable one.* | `#a88cff` (Violet) |
| `09` | **AURA PLUS** | *Your aura has been upgraded to premium.* | `#65dfea` (Cyan) |
| `10` | **MAIN CHARACTER WIND** | *A dramatic breeze will arrive on cue.* | `#ff9a5e` (Orange) |
| `11` | **PIGEON FAME** | *You are legally interesting to three pigeons.* | `#d5ff3f` (Acid Green) |
| `12` | **SNACK PROPHECY** | *The universe owes you a snack. Collect soon.* | `#ff6682` (Hot Pink) |

### 🔊 3. Procedural Synthesizer Audio (Web Audio API)
No external sound files or bulky assets required:
- **Click Sound**: Quick triangle-wave frequency drop (`510Hz → 310Hz`) when the spin button is initiated.
- **Ticking Wheel Clicks**: Speed-sensitive square wave pulses (`300Hz–470Hz`) dynamically triggered as slices cross the pointer.
- **Victory Chime**: 3-stage arpeggiated melodic synth triumph (`440Hz → 660Hz → 990Hz → 1320Hz`) upon fate reveal.
- **Mute / Unmute Toggle**: Full user control with accessible ARIA toggle state.

### 💥 4. Visual Effects & Neo-Arcade Aesthetics
- **Particle Confetti Cannon**: Physics-driven explosion of ~92 particles on destination reveal, simulating velocity, gravity, air resistance, rotation, and fading alpha.
- **Haptic Screen Shake**: Dynamic viewport shudder effect (`@keyframes shake`) when fate locks in.
- **Cyberpunk Dark Mode**: High-contrast dark palette (`#101015`), subtle fractal noise overlay, neon acid highlights (`#d5ff3f`), and rotating celestial dash ring.
- **Fate Telemetry & Luck Meter**:
  - **Spins Logged Counter**: Tracks cumulative spin sessions.
  - **Luck Meter**: 5-state streak indicator (`PROMISINGLY ODD` → `MILDLY CURSED` → `COSMICALLY RANDOM` → `ABSOLUTELY FATED` → `CHAOS CONFIRMED`).
  - **Recent Fates History**: Stores and displays the last 3 assigned fate chips.

### ♿ 5. Accessibility & Responsiveness
- **Accessible ARIA Attributes**: Screen-reader friendly with `aria-live="polite"` result panels, descriptive labels, and button states.
- **`prefers-reduced-motion` Support**: Detects user motion preferences to disable screen shake, eliminate tick jitter, and shorten the spin duration from ~6s down to 950ms.
- **Fully Responsive**: Adapts seamlessly from large desktop monitors down to 320px mobile screens.

---

## 🛠️ Tech Stack & Architecture

- **Markup & Styling**: Semantic HTML5, CSS custom properties (variables), Flexbox, CSS Grid, and Google Fonts (`Space Grotesk` & `DM Mono`).
- **Rendering Engine**: HTML5 2D Canvas (`<canvas id="wheel">` and `<canvas id="particles">`).
- **Audio Engine**: Native Browser `AudioContext` with programmatic oscillators and gain envelopes.
- **Zero External Dependencies**: Pure, standalone vanilla JavaScript — runs directly in any modern browser without build steps or bundlers.

---

## 🚀 Getting Started

### Option 1: Open Directly in Browser
Since the application in `artifacts/impossible-destiny/index.html` is completely self-contained, you can open it directly:

```bash
# On macOS
open artifacts/impossible-destiny/index.html

# On Linux
xdg-open artifacts/impossible-destiny/index.html

# On Windows
start artifacts/impossible-destiny/index.html
```

### Option 2: Serve Locally via HTTP Server

```bash
# Using Python 3
python3 -m http.server 8000 --directory artifacts/impossible-destiny

# Or using npx serve
npx serve artifacts/impossible-destiny
```

Then visit [http://localhost:8000](http://localhost:8000) in your browser.

---

## 📁 Repository Structure

```
Wheel-of-Impossible-Destiny/
├── artifacts/
│   ├── impossible-destiny/
│   │   ├── index.html        # Complete standalone Fate Engine application
│   │   ├── package.json      # Vite React app package configuration
│   │   └── src/              # React workspace app components & styles
│   ├── api-server/           # Backend API server workspace
│   └── mockup-sandbox/       # Design mockup sandbox
├── lib/                      # Shared workspace libraries (api-spec, db, etc.)
├── package.json              # Root workspace manifest
├── pnpm-workspace.yaml       # pnpm workspace configuration
└── README.md                 # Project documentation
```

---

## 📜 Credits & License

- **Concept & Implementation**: Created by **Student 150096725032**
- **License**: MIT
