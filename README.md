# Interval Timer ⏱️

[![GitHub Pages](https://img.shields.io/badge/Live%20Demo-GitHub%20Pages-3b82f6?style=for-the-badge&logo=github)](https://ketan-k.github.io/interval-timer/)
[![PWA Ready](https://img.shields.io/badge/PWA-Installable%20%26%20Offline-9333ea?style=for-the-badge&logo=pwa)](https://web.dev/progressive-web-apps/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge)](LICENSE)
[![Zero Dependencies](https://img.shields.io/badge/Dependencies-Zero-success.svg?style=for-the-badge)](https://developer.mozilla.org/)

> A sleek, distraction-free interval timer with round counter and rest intervals. Minimalist, offline-ready, background-throttling immune, and built with zero external dependencies.

🔗 **Live Application:** [https://ketan-k.github.io/interval-timer/](https://ketan-k.github.io/interval-timer/)

---

## ✨ Features & Architecture

- ⭕ **Hero Circular Dial:**
  - High-visibility 310px SVG countdown dial with smooth progress stroke and cardinal reference markers.
  - Millisecond precision readout (`00:30.00`) and live round subtext.
- ⚡ **Dual-Engine Timing Architecture (Zero Drift & Background Throttling Immune):**
  - **Foreground:** Driven by `requestAnimationFrame` and high-resolution timestamp deltas for fluid 60fps UI updates.
  - **Background (Web Worker Heartbeat):** Bypasses browser tab throttling when minimized or backgrounded by utilizing an inline dedicated Web Worker thread to ensure audio chimes, round transitions, and tab title updates continue firing exactly on time.
- 🔁 **Work & Rest Intervals:**
  - Configurable **Round Duration** (5s – 180s) and **Rest Interval** (0s – 60s).
  - Ambient color shifts: Electric Blue during active rounds, soothing Amber during rest intervals, and Emerald Green on workout completion.
- 🛑 **Flexible Interval Flow Toggles:**
  - **Stop after round:** Automatically pauses when a round finishes, allowing you to manually start rest or take a break.
  - **Stop after rest:** Automatically pauses after rest recovery finishes before starting the next round.
  - Leave both off for seamless continuous auto-advance.
- 📱 **Progressive Web App (PWA) & Offline-First:**
  - **Installable:** Install as a standalone desktop or mobile app directly from the browser.
  - **100% Offline:** Powered by a lightweight Service Worker (`sw.js`) that caches all assets.
  - **Screen Wake Lock API:** Prevents your phone or laptop display from sleeping while an interval is running.
- 🔔 **Synthesized Web Audio Chimes:**
  - Synthesizes crisp chimes natively via the Web Audio API without external audio files.
  - Proactive gesture-unlocking pipeline guarantees immediate audio firing across iOS Safari, macOS, and Android.
- 📑 **Dynamic Tab Title & Favicon Countdown:**
  - Live timer countdown in the browser tab title (`(00:24) Round 1/4 • Timer`) and dynamically colored SVG favicon.
- 🚀 **Preset Quick Adds:**
  - Add `+15s`, `+30s`, or `+1m` on the fly without interrupting countdown flow.
- 🖥️ **Fullscreen Mode (<kbd>F</kbd>):**
  - Expands into a distraction-free view for workout monitors, presentations, or study desks.
- 💾 **Defensive LocalStorage Persistence:**
  - Robust schema validation protects persisted preferences (rounds, duration, rest, theme, audio) against data corruption.

---

## ⌨️ Keyboard Shortcuts

| Key | Action |
| :--- | :--- |
| <kbd>Space</kbd> | Start / Pause / Resume timer |
| <kbd>R</kbd> | Reset timer to initial state |
| <kbd>F</kbd> | Toggle Fullscreen mode |
| <kbd>M</kbd> | Mute / Unmute audio chimes |

---

## 📲 Installing as an App

### On Desktop (Chrome, Edge, Brave, Safari 17+)
1. Visit [https://ketan-k.github.io/interval-timer/](https://ketan-k.github.io/interval-timer/)
2. Click the **Install** button in the top bar (or the install icon in the URL bar).
3. The timer opens in its own window, dockable like a native app.

### On Mobile (iOS & Android)
- **Android (Chrome):** Tap menu (⋮) → **"Install App"** or tap the install icon.
- **iOS (Safari):** Tap Share (□↑) → **"Add to Home Screen"**.

---

## 🚀 Running Locally

Because this project is built with vanilla web technologies, there are **no dependencies to install** and **no build steps required**.

1. Clone the repository:
   ```bash
   git clone https://github.com/Ketan-K/interval-timer.git
   cd interval-timer
   ```

2. Open `index.html` directly in any modern web browser:
   ```bash
   # On macOS
   open index.html

   # On Linux
   xdg-open index.html

   # On Windows
   start index.html
   ```

Or serve via any static file server:
```bash
npx serve .
# or
python3 -m http.server 8080
```

---

## 🛠️ Tech Stack

- **PWA:** Web App Manifest (`manifest.webmanifest`), Service Worker (`sw.js`), Screen Wake Lock API
- **Worker:** Inline Web Worker thread (Blob URL) for background throttling bypass
- **Structure:** Semantic HTML5
- **Styling:** Modern Vanilla CSS3 with Custom Properties
- **Logic:** Vanilla JavaScript (ES6+)
- **Audio:** Web Audio API (`AudioContext` oscillator synthesis)

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

Crafted with care by [Ketan Katore](https://github.com/Ketan-K).
