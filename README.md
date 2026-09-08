# Interval Timer ⏱️

[![GitHub Pages](https://img.shields.io/badge/Live%20Demo-GitHub%20Pages-3b82f6?style=for-the-badge&logo=github)](https://ketan-k.github.io/interval-timer/)
[![PWA Ready](https://img.shields.io/badge/PWA-Installable%20%26%20Offline-9333ea?style=for-the-badge&logo=pwa)](https://web.dev/progressive-web-apps/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge)](LICENSE)
[![Design: Material 3](https://img.shields.io/badge/Design-Material%203-blue.svg?style=for-the-badge&logo=google)](https://m3.material.io/)
[![Zero Dependencies](https://img.shields.io/badge/Dependencies-Zero-success.svg?style=for-the-badge)](https://developer.mozilla.org/)

> A sleek, distraction-free interval timer and counter crafted in **Google Material Design 3 (Material You / Google Clock)** aesthetic. Features customizable round & rest intervals, audio chimes, offline PWA support, screen wake lock, and zero external runtime dependencies.

🔗 **Live Application:** [https://ketan-k.github.io/interval-timer/](https://ketan-k.github.io/interval-timer/)

---

## ✨ Features

- 📱 **Progressive Web App (PWA) & Offline-First:**
  - **Installable:** Install as a standalone native-like app on macOS, Windows, Linux, Android, and iOS directly from the browser.
  - **100% Offline Capability:** Powered by a lightweight Service Worker (`sw.js`) that caches application shell and fonts for instant loading anywhere.
  - **Screen Wake Lock API:** Prevents your phone or laptop display from sleeping or dimming while an interval is actively running.
- 🎨 **Google Material Design 3 Aesthetic:**
  - Authentic Google Dark mode container (`#20242e`) with radiant Google Blue (`#3b82f6`) accents.
  - Light / Dark theme toggle with persistent preferences.
  - Google Sans & Roboto typography with tabular numerals (`tabular-nums`) to prevent digit shifting.
- ⭕ **Hero Circular Dial:**
  - High-visibility 310px SVG countdown dial with smooth progress stroke and 4 cardinal reference dots.
  - Millisecond precision readout (`00:30.00`).
- ⚡ **Precision 60fps Timing Engine:**
  - Eliminates browser `setInterval` background drift by utilizing `requestAnimationFrame` and high-resolution timestamp deltas.
- 🔁 **Work & Rest Intervals:**
  - Configurable **Round Duration** (5s – 180s) and **Rest Interval** (0s – 60s).
  - Ambient color shifts: Google Blue during active rounds, soothing Google Amber during rest intervals, and Emerald Green on workout completion.
- 🛑 **Flexible Interval Flow Toggles:**
  - **Stop after round:** Automatically pauses when a round finishes, allowing you to manually start rest or take a break.
  - **Stop after rest:** Automatically pauses after rest recovery finishes before starting the next round.
  - Leave both off for seamless continuous auto-advance.
- 🔔 **Synthesized Web Audio Chimes:**
  - Zero external `.mp3` or asset downloads; synthesizes crisp Google Clock style chimes natively via the Web Audio API.
  - Distinct auditory cues for countdown warnings, rest transitions, and completion fanfare.
- 📑 **Dynamic Tab Title & Favicon Countdown:**
  - Live timer countdown in the browser tab title (`(00:24) Round 1/4 • Google Timer`) and dynamically colored SVG favicon.
- 🚀 **Quick Preset Chips:**
  - Add `+15s`, `+30s`, or `+1m` to the current interval on the fly without interrupting countdown flow.
- 🖥️ **Fullscreen Mode (<kbd>F</kbd>):**
  - Expands smoothly into a distraction-free display for workout monitors, presentations, or study desks.
- 💾 **LocalStorage Persistence:**
  - Automatically saves your preferred round counts, durations, rest intervals, toggles, sound, and theme settings.

---

## ⌨️ Keyboard Shortcuts

| Key | Action |
| :--- | :--- |
| <kbd>Space</kbd> | Start / Pause / Resume timer |
| <kbd>R</kbd> | Reset timer to initial state |
| <kbd>F</kbd> | Toggle Fullscreen mode |
| <kbd>M</kbd> | Mute / Unmute audio chimes |

---

## 📲 Installing as a PWA

### On Desktop (Chrome, Edge, Brave, Safari 17+)
1. Visit [https://ketan-k.github.io/interval-timer/](https://ketan-k.github.io/interval-timer/)
2. Click the **Install** icon in the browser address bar or the header install button.
3. The timer opens in its own clean window without browser tabs or URLs, dockable like a native app.

### On Mobile (iOS & Android)
- **Android (Chrome):** Tap the install prompt or menu (⋮) → **"Install App"**.
- **iOS (Safari):** Tap the Share icon (□↑) → **"Add to Home Screen"**.

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
- **Structure:** Semantic HTML5
- **Styling:** Vanilla CSS3 with Material Design 3 Custom Properties
- **Logic:** Vanilla JavaScript (ES6+)
- **Audio:** Web Audio API (`AudioContext` oscillator synthesis)
- **Typography:** Google Fonts (`Google Sans`, `Roboto Mono`)

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

Crafted with care by [Ketan Katore](https://github.com/Ketan-K).
