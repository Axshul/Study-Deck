# Study-Deck

Single-file web app (index.html) that browses and renders this repository’s file-based study materials. No manifests, no build.

How it works
- Place content under these buckets:
  - `subjects/<subject>/{notes,papers,links,thoughts}`
  - `decks/<deck-name>/...` curated copies of files (simple folders)
  - `users/<name>/subjects/...` for personal organization (optional)
- GitHub Pages serves `index.html`, which discovers files via the GitHub Contents API and renders them.
- Ordering: numeric prefixes (e.g. `001-`) sort first, then alphabetical.

Contributing
- Add Markdown notes (`.md`). For images in a note, add a sibling folder named `<note-file>.assets/`.
- Add PDFs to `papers/`.
- Add links:
  - Either put a list in `links.md` as `- [Title](https://url)` lines, or
  - Create one-link-per-file with `.link` extension containing the URL on the first line.
- Thoughts: quick notes in `.md` (date prefix recommended).

Local dev
- Open `index.html` via GitHub Pages for your fork, or run with `?owner=<github_user>&repo=Study-Deck` query params when viewing locally.
