# GMAT Quant Trainer

A single-file web app for practicing GMAT quant questions on a tablet (built for a
Galaxy tablet + S-Pen). Runs fully offline once loaded.

## Files
- **`gmat_practice.html`** — the entire app (HTML + CSS + JS, no build step, no server).
- **`index.html`** — redirects to the app so the site root opens it.
- **`questions_db.txt`** — source-of-truth question bank (JSON array). The questions are
  also embedded inside `gmat_practice.html` so it works when opened as a local file.

## Features
- Randomized practice sessions with a set question count.
- Filters: all / only-wrong / only-needed-hints / both, plus self-rated difficulty
  (low / medium / high / unrated) and "skip ones I already got correct."
- Per-question difficulty rating buttons.
- S-Pen drawing over the whole pane (pen draws, finger navigates/scrolls); eraser,
  undo, clear, colors.
- "Claude" tutor panel: instant offline Hint + Full-steps for every question, plus an
  optional live chat (paste an Anthropic API key in Settings).
- Progress + session history saved in the browser (localStorage).

## Run it on the tablet (GitHub Pages)
Once this repo is pushed and Pages is enabled (Settings → Pages → deploy from
`main` / root), open on the tablet:

```
https://<your-username>.github.io/<repo-name>/
```

Add it to the tablet home screen. Every push updates the live site.

## Live Claude chat (optional)
The offline Hint / Full-steps buttons need no setup. To also chat live, open
⚙ Settings in the app and paste an Anthropic API key — it is stored only in your
browser and calls the Anthropic API directly from the tablet.
