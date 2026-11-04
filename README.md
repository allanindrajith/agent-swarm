# Agent Swarm — Interactive Rebuilding Portfolio Template

An interactive portfolio template where a swarm of 18 simulated collaborative AI cursor agents (`Ada`, `Linus`, `Grace`, `Alan`, `Margaret`, etc.) assemble your website element-by-element with crosshairs, typing carets, pen lines, and alignment guides.

Zero build steps. Zero npm dependencies. Edit standard HTML and ship.

---

## ⚡ Quick Start (30 Seconds)

Clone the repo and run any local static HTTP server:

```bash
git clone https://github.com/<your-username>/<your-repo-name>.git
cd <your-repo-name>

# Start local server (choose any):
python3 -m http.server 8080
# or
npx serve .
```

Open `http://localhost:8080` in your browser. The swarm will immediately scan your page and auto-scroll as it builds your portfolio.

---

## 🛠️ How to Customize for Your Own Site

Open `index.html` in any text editor. Every customizable block is clearly marked with numbered comments:

1. **Title & SEO**: Update `<title>` and `<meta name="description">`.
2. **Brand Colors**: Change `--accent`, `--bg`, or `--card-bg` in `:root`.
3. **Hero Section**: Edit your name, role, tagline, and call-to-action buttons.
4. **Metrics**: Update the 3 highlight statistics.
5. **Projects Grid**: Add or replace project cards (title, summary, tech stack tags).
6. **Footer**: Update your copyright, email, and social links.

Save `index.html`, refresh your browser, and the agents will automatically adapt to your new content and layer count.

---

## 🧠 How the Engine Works (`swarm.js`)

`swarm.js` is a self-contained, zero-dependency client engine:

* **DOM Snapshotter**: Scans your semantic HTML elements into discrete tasks (rectangles, headings, text blocks, guides).
* **Multiplayer Cursor Swarm**: 18 concurrent bot cursors with names, colors, and SVG pointers execute build tasks.
* **Auto-Touring Mode**: Automatically calculates camera velocity and scrolls the viewport down as layers are completed.
* **WebAudio Synthesizer**: Generates live mechanical keyboard clicks and pentatonic notes via the browser Web Audio API (no audio assets needed).
* **Floating Controller**: Includes layer count (`done / total`), speed toggles (`1×`, `2×`, `3×`), pause/tour switch, and mute button.

---

## 🧩 Chrome Extension (Run on Any Website)

Want to trigger this animation on your existing live website or app?

1. Open Google Chrome and navigate to `chrome://extensions`.
2. Turn on **Developer mode** in the top right.
3. Click **Load unpacked** and select the [`extension/`](extension/) directory from this repository.
4. Navigate to any website and press `Alt+Shift+S` (or click the pinned extension icon).

---

## 🚀 Deploying to GitHub Pages

1. Push this repository to GitHub.
2. Go to **Settings** → **Pages**.
3. Under **Build and deployment**, set Source to **Deploy from a branch** and select `main` / `root`.
4. Click **Save**. Your site will be live in under 60 seconds.

---

## 📜 Credits

- Inspired by **[Swarm](https://califa.github.io/swarm-site/)** by **Joel Califa** (`@califa`).
- Rebuilder engine adapted from **[Swarm Cursors](https://github.com/DhvanilPatel/swarm-cursors)** by **Dhvanil Patel**.
