# CLAUDE.md

This repo is Jitse-Jan's GitHub profile README (renders on https://github.com/jitsejan).

## Source of truth for content

- Career/skills content should be derived from the latest CV at
  `/Users/jitsejan/code/personal/resume-latex-jitsejan/` (filename includes the CV date,
  e.g. `CV JJM Van Waterschoot 2026-09.pdf`). Always use the most recent dated file.
- **Never mention company or client names** on this public profile. Generalize
  achievements (e.g. "led a data function from 7 to 22 engineers" instead of naming
  the employer). Skills, tools, and quantified outcomes are fine to include.

## Known fragile external images

The stats/badge images in README.md depend on free third-party services that have
broken repeatedly:

- `github-readme-stats-*.vercel.app` (personal Vercel forks) — can go down if the
  deployer's GitHub token (`PAT_1` env var) expires, or the deployment is paused.
- `github-readme-activity-graph.vercel.app` — was removed from the README (2026-09)
  after its Vercel deployment returned 402 Payment Required with no maintained
  alternative found.

Before merging any README change, verify every `![...](https://...)` image URL
actually returns real content (not just HTTP 200 — some of these services return a
200 status with an SVG *error card* embedded, e.g. "Maximum retries exceeded"). Check
the response body, not just the status code.

## Workflow notes

- Small wording/content fixes can go straight to `master`; larger content rewrites
  should go through a branch + PR.
- Delete branches (locally and on origin) after they're merged.
