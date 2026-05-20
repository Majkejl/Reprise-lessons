# Reprise — Lessons Repository

This repository publishes official first-party lesson content for the [Reprise](https://github.com/your-org/reprise) exam revision PWA.

`index.json` lists all available lessons. The Reprise app syncs from this repository to make lessons available offline.

## Structure

- `index.json` — manifest listing all lessons (currently empty; add entries as lessons are authored)

## Adding lessons

1. Author a lesson JSON file that validates against the schema in the `template/` repo.
2. Add a pointer to `index.json`.
3. Push — the validation workflow will confirm the JSON is well-formed.
