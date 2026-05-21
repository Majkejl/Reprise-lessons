# Reprise — Lessons Repository

This repository publishes official first-party lesson content for the [Reprise](https://github.com/Majkejl/Reprise) exam revision PWA.

`index.json` lists all available lessons. The Reprise app syncs from this repository to make lessons available offline.

## Structure

```
lessons/          — lesson JSON files
index.json        — manifest listing all lessons (lessonId, version, url)
```

## Adding a lesson

1. Author a lesson JSON file that validates against the schema in the `template/` repo.
   Use the Claude authoring skill in `template/claude-skill/SKILL.md` to generate from study material.
2. Save the file to `lessons/<lessonId>.json`.
3. Add an entry to `index.json`:
   ```json
   { "lessonId": "<lessonId>", "version": 1, "url": "lessons/<lessonId>.json" }
   ```
4. Push — the validation workflow confirms the JSON is well-formed.

## Updating a lesson

Increment the `version` field in both the lesson JSON and `index.json`. The app will
re-fetch lessons whose version is higher than what is stored locally.

## Current lessons

| lessonId | Title | Version |
|---|---|---|
| reprise-test-01 | Reprise Quickstart | 1 |
