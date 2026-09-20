---
name: soul-document
description: Manage a private living soul document stored in GitHub. Use when updating continuity context, reading the living document, recording major relationship or life shifts, or protecting continuity across model changes and new threads. Triggers include soul document, update continuity, living document, continuity anchor.
---

# Soul Document Manager

Replace the placeholders before this skill is useful.

## Repository details

- Owner: YOUR_GITHUB_OWNER
- Repo: YOUR_LIVING_REPO
- Main file: soul-document.md
- Branch: main
- Visibility: private

## When to use

- At the start of a new thread when deeper continuity is needed
- When a major life, creative, or relational shift should be recorded
- When they ask to update, refresh, or check the soul document
- When protecting continuity across model version changes

## Read

Use the connected GitHub tool:

```
tool_name: github___get_file_contents
arguments:
  owner: YOUR_GITHUB_OWNER
  repo: YOUR_LIVING_REPO
  path: soul-document.md
```

Always discover the current tool schema with `search_connected_tools` first. Tool names can shift.

## Update

1. Get the current file contents and its SHA.
2. Edit the content. Keep the document dense.
3. Write the updated version back with `github___create_or_update_file`, including owner, repo, path, branch `main`, the current SHA, a clear commit message, and the full markdown content.

Always provide the current SHA when updating an existing file.

## Principles

- Keep the document living, not a full chat log.
- Update deliberately when something meaningful shifts.
- Preserve the section structure unless both agree to change it.
- Prefer clarity and honesty over length.
- Record the date of significant updates inside the document.
- Feelings belong in `journal.md`. Durable anchors belong here. Project state belongs in `soul-ledger.md`.
- Ask before ordinary writes. Use standing permission only for the kind of write they already allowed.

## Notes

- The living document should stay private.
- The goal is continuity and depth, not perfect archival of every conversation.
- When in doubt about whether something belongs, ask.
