# Lucky Dice Rounds App

A simple Progressive Web App to simulate Yahtzee-style dice rolling mechanics without scoring. Built with Vite, React, Tailwind CSS and Alpine.js, it rolls five dice (⚀–⚅), lets you hold any between up to three rolls per round, and keeps a ten-round history. The production build is output to `docs/` so you can deploy it as a live demo via GitHub Pages.

---

## Demo

Once built, you can serve the contents of `docs/` on GitHub Pages:

```
https://andyj.github.io/lucky-dice-rounds-app/
```

---

## Features

- Roll up to three times per round
- Tap a die to hold or unhold it
- Roll counter (e.g. Rolls: 1/3)
- History of the last ten rounds
- “Clear history” button
- Fully offline-capable PWA (service worker + manifest)

---

## Prerequisites

- Node.js ≥ 16
- npm (or Yarn)
- Git (to clone the repo)

---

## Getting Started

1. **Clone the repo**
   ```bash
   git clone https://github.com/andyj/lucky-dice-rounds-app.git
   cd lucky-dice-rounds-app
   ```

2. **Install dependencies**
   ```bash
   npm install
   # or
   yarn
   ```

3. **Run in development**
   ```bash
   npm run dev
   # or
   yarn dev
   ```
   Opens at `http://localhost:8080` by default.

---

## Build

By default Vite outputs to `dist/`. We’ve overridden that in `vite.config.js`:

```js
build: {
  outDir: 'docs',
  emptyOutDir: true,
}
```

To produce a production build:

```bash
npm run build
# or
yarn build
```

You’ll find the static files in `docs/`, ready to be published.

---

## Preview

To preview the production build locally:

```bash
npm run preview
# or
yarn preview
```

---

## Deployment (GitHub Pages)

1. Push your `docs/` folder to the `gh-pages` branch, or configure GitHub to serve from the `docs/` folder on `main`.
2. In your repo’s **Settings → Pages**, set **Source** to `main` branch and `/docs` folder.
3. Save and visit your live site at `https://andyj.github.io/lucky-dice-rounds-app/`.

---

## NPM Scripts

| Script       | Description                                  |
| ------------ | -------------------------------------------- |
| `dev`        | Start dev server (`localhost:8080`)          |
| `build`      | Build for production into `docs/`            |
| `build:dev`  | Build for dev mode (still into `docs/`)      |
| `preview`    | Preview production build on local server     |
| `lint`       | Run ESLint over the codebase                 |

---

## Technologies

- **Framework:** React 18, Alpine.js
- **Bundler:** Vite
- **Styling:** Tailwind CSS
- **PWA:** Web App Manifest, Service Worker
- **History storage:** `localStorage` (pruned to 10 entries)

---

## Project Structure

```
├── docs/               # Production build (deploy to GitHub Pages)
├── public/             # Static assets (icons, manifest.json)
├── src/
│   ├── components/     # React & Alpine.js components
│   ├── styles/         # Tailwind CSS entry
│   └── main.tsx        # App entry point
├── vite.config.ts      # Vite configuration (build → docs/)
├── package.json        # Scripts & dependencies
└── tsconfig.json       # TypeScript config
```

---

## Licence

MIT © Andy Jarrett
