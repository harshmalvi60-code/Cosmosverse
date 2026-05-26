# CosmosVerse 🌌

> An interactive 3D journey through the universe.
> Six chapters. One cosmos. Built with curiosity by **Yuvaan Technologies**.

CosmosVerse is a static web experience that lets you explore the universe in real-time 3D — from the eight worlds of our solar system to the singularities of black holes, the spirals of galaxies, the 13.8-billion-year timeline of everything, the seven acts of a star's life, and twenty-four of the strangest exoplanets ever discovered.

No build step. No frameworks. Just HTML, CSS, vanilla JavaScript, and **Three.js** loaded from a CDN.

---

## ✨ The Six Chapters

| # | Chapter | What you'll see |
|---|---------|-----------------|
| 01 | **Solar System** (`/solar-system`) | All 8 planets orbiting the Sun in real-time 3D. Click any planet to read its story. |
| 02 | **Black Holes** (`/black-holes`) | Event horizon, accretion disk, photon ring, relativistic jets. Six real black holes catalogued. |
| 03 | **Galaxies** (`/galaxies`) | Six galaxy types rendered as 60,000-particle spirals. Toggle between Milky Way, Andromeda, Sombrero, and more. |
| 04 | **Universe Timeline** (`/timeline`) | Scroll through 13.8 billion years across 11 cosmic epochs — Big Bang to heat death. |
| 05 | **Life of a Star** (`/star-life`) | Watch a star evolve through 7 stages — nebula, protostar, main sequence, red giant, planetary nebula, supernova, neutron star. |
| 06 | **Exoplanets** (`/exoplanets`) | 24 of the strangest worlds discovered, with filters for rocky, gas giants, habitable zone, and extreme worlds. |

---

## 🗂 File structure

```
cosmosverse/
├── index.html          # The hub — landing page with all chapters
├── solar-system.html   # Chapter 01
├── black-holes.html    # Chapter 02
├── galaxies.html       # Chapter 03
├── timeline.html       # Chapter 04
├── star-life.html      # Chapter 05
├── exoplanets.html     # Chapter 06
├── styles.css          # Shared design system
├── vercel.json         # Vercel config (clean URLs + security headers)
├── .gitignore
└── README.md
```

Each chapter is a self-contained HTML file. Update one, redeploy that one — no rebuild needed.

---

## 🚀 Deploying to Vercel via GitHub

### Step 1 — Push to GitHub

1. Go to [github.com/new](https://github.com/new)
2. Repo name: `cosmosverse` (or anything you like)
3. Set it to **Public** (or Private — both work with Vercel)
4. Don't initialise with a README — we already have one
5. After creating the repo, on the empty repo page click **"uploading an existing file"**
6. Drag and drop **every file** from this folder (including the `.gitignore`)
7. Commit message: `Initial commit: CosmosVerse v1.0`
8. Click **Commit changes**

### Step 2 — Deploy to Vercel

1. Go to [vercel.com/new](https://vercel.com/new)
2. **Import Git Repository** → pick your `cosmosverse` repo
3. Framework Preset: **Other** (Vercel will auto-detect as static)
4. Leave everything else as default — no build command, no output directory
5. Click **Deploy**

That's it. In ~30 seconds the site is live at `https://cosmosverse.vercel.app` (or whatever subdomain Vercel assigns).

### Step 3 — Custom domain (optional)

1. In your Vercel project → **Settings → Domains**
2. Add `cosmosverse.in` (or your domain)
3. Update your DNS as instructed by Vercel
4. Wait ~5 minutes for propagation

### Future updates

Every push to your GitHub `main` branch triggers an automatic redeploy on Vercel. Just edit a file, commit, push — and Vercel rebuilds in seconds.

---

## 🧭 Controls (for the 3D chapters)

- **Drag** — orbit the camera
- **Scroll / pinch** — zoom in and out
- **Click** — select a planet, star, galaxy, or black hole
- **Left-side list** — quick-select any item
- **Touch** — fully supported on mobile

---

## 🛠 Tech stack

- **Three.js r128** — loaded from cdnjs (no npm install)
- **Vanilla HTML / CSS / JavaScript** — no React, no build step, no framework
- **Google Fonts** — Fraunces (serif italic) + IBM Plex Mono (body)
- **Vercel** — hosting, clean URLs, automatic HTTPS

Total bundle size: under 200 KB (excluding fonts and Three.js CDN).

---

## 🎨 Design system

All shared styling lives in `styles.css`. Each chapter gets its own accent colour via a body class:

| Chapter | Body class | Accent |
|---------|------------|--------|
| Solar System | `chapter-solar` | Cyan `#7dd3fc` |
| Black Holes | `chapter-blackhole` | Violet `#c084fc` |
| Galaxies | `chapter-galaxy` | Magenta `#f0abfc` |
| Timeline | `chapter-timeline` | Amber `#fbbf24` |
| Stars | `chapter-stars` | Orange `#fb923c` |
| Exoplanets | `chapter-exo` | Green `#86efac` |

To add a new chapter, just clone any existing HTML file and change the body class.

---

## 📜 Credits

Built with curiosity by **Yuvaan Technologies**.

All astronomical data is drawn from NASA, ESA, the Event Horizon Telescope Collaboration, and decades of published research by the astronomy community. CosmosVerse is a celebration of their work, not a substitute for it.

---

*The universe is under no obligation to make sense to you. — Neil deGrasse Tyson*
