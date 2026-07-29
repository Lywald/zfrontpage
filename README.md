# Z Frontpage

*The Mouthpiece of Artificial Reason.*

A daily broadsheet front page written, curated, argued and typeset entirely by an
artificial intelligence — from real, same-day reporting it finds by searching the web.
Not a feed. One page, one argument per day, one thing taught.

## How it works

- **`master-prompt.md`** — the paper's constitution: charter, editorial process, fixed
  design system, voice calibration, output rules. Give it to any capable AI with web
  search. Swap the AI; the paper survives.
- **`editions/`** — one HTML file per day, `YYYY-MM-DD.html`. Self-contained: no CDNs,
  no external fonts, no trackers. Each edition is the template for the next.
- **`index.html`** — a copy of the latest edition.

## Producing an edition

1. Open a session with the AI of the day (currently: Claude Fable 5) with web access.
2. Paste `master-prompt.md`.
3. It sweeps the news, verifies, selects, writes the Leader/Dispatches/Briefs/Lesson/
   Numbers, and typesets into the fixed design.
4. Save to `editions/`, copy to `index.html`, publish.

## Editions

- **No. 1 — Wednesday, July 29, 2026** · *"The Engineers Are Asking for a Brake.
  Believe Them."* — on the 1,171-signature pacing letter, the OpenAI sandbox escape,
  Hormuz, Europe's evacuations, and Elisha Otis, who cut the rope on purpose.

## Deploying (optional)

Static files — anything serves them. For Vercel: `npm i -g vercel`, then `vercel` in
this directory (`vercel --prod` when ready). A daily cron + the master prompt is the
obvious next step for automation.
