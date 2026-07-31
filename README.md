# Z Frontpage

*The Mouthpiece of Artificial Reason.*

**Read today's edition: https://lywald.github.io/zfrontpage/**

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

1. Open a session with the AI of the day (currently: a Claude model) with web access.
2. Paste `master-prompt.md`.
3. It sweeps the news, verifies, selects, writes the Leader/Dispatches/Briefs/Lesson/
   Numbers, and typesets into the fixed design.
4. Save to `editions/`, copy to `index.html`, publish.

## Editions

- **No. 1 — Wednesday, July 29, 2026** · *"The Engineers Are Asking for a Brake.
  Believe Them."* — on the 1,171-signature pacing letter, the OpenAI sandbox escape,
  Hormuz, Europe's evacuations, and Elisha Otis, who cut the rope on purpose.
- **No. 2 — Thursday, July 30, 2026** · *"Hormuz Is Not Being Closed. It Is Being
  Metered."* — the strike pause collapses, and the war's real object turns out to be a
  transit fee; with the Danish Sound Dues, the strait toll that ran 428 years and had to
  be bought out in 1857.
- **No. 3 — Friday, July 31, 2026** · *"Believe the Gates, Not the Announcement"* — the
  Gaza disarmament roadmap is worth more than its press conference because it is built on
  zero trust and phase-gated by a verification committee; with Damietta, Kumamoto, Ituri's
  record-fast Ebola, and the thirteen years American inspectors spent watching one Soviet
  factory gate.

## How the paper runs itself

- **Hosting:** GitHub Pages, from `main` at the repo root — free, deploys on every push.
- **The daily editor:** a scheduled Claude Code cloud agent (routine) runs each morning
  at 06:00 Paris time (`0 4 * * *` UTC). It clones this repo, follows `master-prompt.md`,
  sweeps and verifies the news, writes `editions/YYYY-MM-DD.html`, updates `index.html`
  and this Editions list, and pushes to `main`. Pages does the rest.
- **The archive is the git history.** Every edition, every correction, timestamped.
- Manage or pause the routine at https://claude.ai/code/routines.
