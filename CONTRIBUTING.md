# Contributing to Agent Swarm

Thank you for your interest in contributing to **Agent Swarm**! We welcome bug fixes, documentation improvements, and performance optimizations.

---

## 🎯 Core Principles

1. **Zero Runtime Dependencies**: The core portfolio and the rebuilder engine (`swarm.js`) must run natively in modern evergreen browsers without requiring bundlers (Webpack, Vite, Rollup) or npm runtime packages.
2. **Vanilla Web APIs**: Animations, cursors, DOM snapshotting, and audio synthesis are implemented with standard Canvas, Web Audio, and DOM APIs.
3. **Dual Engine Parity**: `swarm.js` in the project root and `extension/swarm.js` must remain identical at all times.

---

## 🛠️ Local Development

### 1. Standalone Portfolio
To preview or modify the portfolio template:

```bash
# Start a local static server
python3 -m http.server 8080
# or
npx serve .
```

Open `http://localhost:8080` in Chrome, Safari, or Firefox.

### 2. Chrome Extension
To test changes in the Chrome Extension:
1. Navigate to `chrome://extensions` in Chrome.
2. Enable **Developer mode** (top-right toggle).
3. Click **Load unpacked** and select the [`extension/`](extension/) directory.
4. Click the extension icon or hit `Alt+Shift+S` on any live webpage.

---

## 📋 Pull Request Process

1. **Fork & Branch**: Create a feature branch from `main` (e.g., `git checkout -b fix/audio-latency`).
2. **Keep Parity**: If you modify `swarm.js`, copy the file into `extension/swarm.js`:
   ```bash
   cp swarm.js extension/swarm.js
   ```
   Verify that `diff -u swarm.js extension/swarm.js` returns zero diff.
3. **Check Console**: Ensure no warnings or errors are thrown in the browser console.
4. **Submit PR**: Open a pull request against `main` using the provided Pull Request Template.
