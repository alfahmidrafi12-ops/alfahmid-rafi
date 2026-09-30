# AGENTS.md

## Project overview
Static single-page portfolio site ("Al Fahmid Rafi — AI Specialist"). The entire app is one self-contained `index.html` with inline CSS and vanilla JS (canvas particle/trail effects, custom cursor, scroll reveal, modal). No backend, no build step, no framework, no external API keys.

## Running in the sandbox
- Served via Vite dev server for live reload of `index.html` edits.
- `docker compose -f docker-compose.base44.yml up -d --build` brings it up; preview is on host port 3000.
- `package.json` and `vite.config.js` exist only to power the dev server — the real source is `index.html`.
- No secrets or environment variables are required to boot.

## Verifying it works
- `curl -s -o /dev/null -w '%{http_code}' localhost:3000` should return 200.
- The page title is "Al Fahmid Rafi — AI Specialist".

## Editing
- All changes go in `index.html`. Vite hot-reloads on save.
- `node_modules` is a named volume; do not delete it to refresh dependencies.
