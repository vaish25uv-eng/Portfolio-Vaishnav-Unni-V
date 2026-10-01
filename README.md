# Portfolio Studio — GitHub Pages version

This is a single self-contained `index.html` — no build step, no npm install,
no Python. Your browser compiles and runs it on the fly.

## How it works

- React, ReactDOM and the icon library load from a public CDN (esm.sh) via an
  **import map** in the `<head>`.
- **Babel Standalone** (also from a CDN) compiles the JSX in the browser at
  page-load time — this is what lets a `.jsx`-style file run with zero
  build tooling.
- Saved edits use the browser's own `localStorage`, scoped to whatever
  domain the page is hosted on (GitHub Pages, in this case). This replaces
  Claude's artifact-only storage API, which only works inside claude.ai.

## Deploy it on GitHub Pages (free, ~2 minutes)

1. Go to [github.com/new](https://github.com/new) and create a new repository
   (public, no need to add a README/.gitignore).
2. On the repo's main page, click **Add file → Upload files**.
3. Drag in `index.html` from this download, then **Commit changes**.
4. Go to **Settings → Pages** (left sidebar).
5. Under **Build and deployment → Source**, choose **Deploy from a branch**.
6. Branch: `main`, folder: `/ (root)` → **Save**.
7. GitHub will give you a live URL after a minute or two, usually:
   `https://<your-username>.github.io/<repo-name>/`

That's it — the portfolio, Studio editor (gear icon, default passcode
`studio2026`), autosave, export/import and theme editor all work exactly as
they did in the Claude preview, now running on your own GitHub Pages URL.

## Notes

- **Change the Studio passcode** once it's live — anyone with your URL who
  guesses/finds the default passcode could open the editor (there's no
  server, so this is a light deterrent, not real security).
- Saved edits live only in the browser/device you edited from (localStorage
  isn't synced across devices). Use **Studio → Data → Export** to download a
  JSON backup you can re-import elsewhere, or to hand off to a future
  backend.
- If you'd rather have an actual pre-built JavaScript bundle (no in-browser
  compile step, marginally faster first load), that needs a real Node/npm
  build — say the word and I can walk you through setting that up too.
