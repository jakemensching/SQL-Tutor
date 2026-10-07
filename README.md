# SQL Sprint ⚡

A personal SQL learning app built around a twice-a-week study schedule. It takes you from basic `SELECT` queries to window functions and query optimization in 28 sessions over 14 weeks.

## Features

- **Curriculum:** 28 sessions across 8 modules (Foundations, Filtering, Aggregates, Joins, Subqueries and CTEs, Transforming data, Window functions, Real-world SQL). Each session has a checklist, and every session after the first opens with a warm-up.
- **Micro-review:** 3-question spaced repetition sets (about 2 minutes). Correct answers come back after 1, 3, 7, 14, then 30 days. Misses come back the next day.
- **Query lab:** real SQLite running in the browser (via [sql.js](https://github.com/sql-js/sql.js)) with a 7-table practice database and 20 auto-graded challenges.
- **Progress tracker:** per-module mastery, review accuracy, challenges solved, and an 8-week consistency chart.

## Tech

- Single file: `index.html` (HTML, CSS, vanilla JavaScript, no build step)
- SQL engine: sql.js 1.12.0 (asm.js build), loaded from cdnjs when the Query lab opens
- Fonts: Bricolage Grotesque and JetBrains Mono from Google Fonts
- Storage: `localStorage` in the browser

## Run locally

Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
```

Then visit http://localhost:8000.

## Deploy with GitHub Pages

1. Push this repo to GitHub.
2. Go to **Settings > Pages**.
3. Under **Source**, pick **Deploy from a branch**, then `main` and `/ (root)`.
4. Your site will be live at `https://<your-username>.github.io/<repo-name>/`.

## Notes on data

Progress is saved in your browser's `localStorage`, so it stays on the device and browser you use. Clearing site data resets it. The Claude-hosted version of this app syncs progress to a Claude account instead; that sync code checks for `window.claude` and is skipped automatically everywhere else.

## Roadmap ideas

- Cross-device sync with a real backend (Supabase or similar)
- AI hints that explain why a query is wrong
- More challenges per module
- Import your own CSV datasets into the Query lab
