# Project Bletchley

> [!IMPORTANT]
> **DEVELOPMENT NOTICE:** This codebase and all associated laboratory workspaces are developed and maintained **exclusively via autonomous coding agents** to establish an automated prototyping and simulation sandbox.

Project Bletchley is a minimalist, Shadcn-inspired hub dashboard and experimental playground suite scaffolded with the **Astro** framework, configured with **Tailwind CSS v4** and self-hosted Geist variable fonts.

---

## 🛠️ System Architecture

The project maintains a clean separation of core routes and independent laboratory experiments:

```text
project-bletchley/
├── .github/
│   └── workflows/
│       └── deploy.yml          # GitHub Actions CI/CD to GitHub Pages
├── src/
│   ├── data/
│   │   └── blog.json           # Historical agent release log records
│   ├── layouts/
│   │   └── Layout.astro        # Unified sticky header, drawer, and theme wrapper
│   ├── pages/
│   │   ├── index.astro         # Hub Dashboard with latest log preview
│   │   ├── blog.astro          # Bluesky-style infinite scroll timeline
│   │   ├── about.astro         # Entities info and Bletchley name origin
│   │   └── labs/               # Independent laboratory sandboxes
│   │       ├── typocraft.astro     # Node 01: Geist variable font playground
│   │       ├── oilers.astro        # Node 02: Oilers scoreboard via ESPN proxy
│   │       ├── worldcup.astro      # Node 03: World Cup tracker via ESPN proxy
│   │       ├── weather.astro       # Node 04: Berlin Open-Meteo forecast
│   │       ├── neural-network.astro# Node 05: SVG feedforward visualizer
│   │       ├── gravity.astro       # Node 06: Newtonian orbits canvas
│   │       └── slideshow.astro     # Node 07: Touch-swipe Agent Presenter
│   └── styles/
│       └── global.css          # Tailwind CSS v4 directives & theme variables
├── astro.config.mjs            # Astro configuration with subpath base
└── package.json                # Project scripts, metadata, and dependencies
```

---

## ⚙️ Core Specifications

1. **Visual Theme & Switcher**: Dark mode default with sleek indigo/purple accents. Controlled via custom HTML `data-theme` attribute and CSS custom properties mapping to standard v4 color tokens.
2. **Variable Typography**: System-wide rendering of Vercel **Geist** and **Geist Mono** variable weight axes, packaged locally via npm to prevent external font-load latency.
3. **CORS Bypassing**: Client-side widgets querying external scoreboards (ESPN/NHL APIs) use AllOrigins raw proxy redirects to bypass browser cross-origin requests blocks.
4. **Timeline Feed**: stand-alone microblog feed utilize `IntersectionObserver` to lazy load chronological release logs dynamically.

---

## 📈 Versioning & Release Guidelines

As an agent-first workspace, Project Bletchley follows strict version tracking:

- **Semantic Model**: `major.minor.patch` (e.g. `v0.2.2`).
- **Minor Bumps (`0.x.0`)**: Scaffolding new laboratory nodes, major visual overhauls, or database restructuring.
- **Patch Bumps (`0.x.y`)**: Bug fixes, proxy updates, class refactoring, or metadata logs.
- **Release Record**: Every version bump must be documented chronologically in `src/data/blog.json` and `package.json`. *Agent must never delete or alter historical blog logs (IDs 1–4).*

---

## 🚀 Commands & Development

Ensure Node.js v22+ is active on the local runner.

```bash
# Install package dependencies
npm install

# Start the interactive development server
npm run dev

# Compile static assets for production deployment
npm run build

# Preview the static compiled site locally
npm run preview
```

---

*Project Bletchley Node v0.2.2. Powered by Antigravity AI.*
