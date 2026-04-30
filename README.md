# OMR Game — With Form

Sovendus OMR Festival touchscreen kiosk game. This version includes a contact form (name, company, email) on the entry screen.

Live demo: enable GitHub Pages on this repo (Settings → Pages → Deploy from branch `main`, root). The redirect at the project root forwards to `src/index.html`.

## Run locally

### As a website (browser)

```bash
npm start
```

Then open http://localhost:3000

The form fields can be left empty — on the web there is no input save, so users can continue without filling them in.

### As an Electron kiosk app

The original Electron entry points (`main.js`, `preload.js`, `launch.js`) are kept for the on-site kiosk build, where input is written to `game input.xlsx` via the `xlsx` package. To run the kiosk version:

```bash
npm install
npx electron .
```

## Project structure

- `src/` — the game (HTML/CSS/JS), runs in any browser
- `assets/` — images, fonts, icons
- `landing-page/` — separate landing page
- `main.js`, `preload.js`, `launch.js` — Electron kiosk wrappers
- `serve.js` — tiny static file server for local browser testing
