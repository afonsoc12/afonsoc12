# Claude Instructions

## Project Overview
- Repository: `afonsoc12`
- Main focus: GitHub profile README improvements and badge/styling updates.
- Primary file edited most often: `README.md`.

## Editing Guidelines
- Keep changes small and targeted.
- Preserve existing HTML/Markdown structure and alignment style.
- Prefer updating existing badge URLs instead of replacing full sections.
- Keep badge colors and spacing consistent across sections.
- Do not remove sections unless explicitly requested.

## Badge Conventions
- Top badges use `for-the-badge`.
- Stack badges use `flat-square`.
- Keep social colors consistent:
  - GitHub: dark/black tone.
  - LinkedIn: blue (`0077B5` unless user asks otherwise).
  - Contact/site: match latest requested tone.
  - Make sure to link badges to the provder, e.g., clicking on AWS badge should navigate to https://aws.amazon.com

## Daily Quote
- Quote card service: `https://quotes-github-readme.vercel.app/api`
- Current URL params: `?type=horizontal&theme=nord&quote=<encoded>&author=<encoded>`
- Quote is rendered between `<!-- QUOTE -->` and `<!-- END_QUOTE -->` markers in README.md.
- Updated daily at midnight UTC by `.github/workflows/update-quote.yml`.
- Quote source API: `https://zenquotes.io/api/random` (returns single-item array `[{q, a}]`).
- URL encoding done via `jq`'s `@uri` filter in the workflow shell script.
- Workflow also triggers on push to `develop` branch for testing.
- Workflow has 3 retries with 30s delay; logs HTTP codes, errors, quote text and author.

## Common Tasks
- Add/remove/reorder badges.
- Adjust badge color tones.
- Center content and keep spacing consistent.
- Update links to user repos/sites.
