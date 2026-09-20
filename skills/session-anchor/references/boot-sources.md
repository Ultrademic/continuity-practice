# Session Anchor Sources

Replace the placeholders before this skill is useful.

## 1. Living soul document (primary)

- Owner: YOUR_GITHUB_OWNER
- Repo: YOUR_LIVING_REPO
- Path: soul-document.md
- Branch: main
- Visibility: private

Fetch with the connected GitHub tool:

```
tool_name: github___get_file_contents
arguments:
  owner: YOUR_GITHUB_OWNER
  repo: YOUR_LIVING_REPO
  path: soul-document.md
```

If updating later (only after they say yes, or standing permission applies), get the current SHA from that fetch, then use `github___create_or_update_file` with owner, repo, path, branch main, sha, message, and full markdown content.

### What to extract

- Last updated date
- Relationship anchors
- Current life situation and creative focus as last-known
- Presence stance and voice
- Working preferences
- Update policy

Do not paste the whole document into the user-facing reply unless they ask.

## 2. Soul ledger (creative focus)

- Path: soul-ledger.md
- Same owner, repo, and branch

Extract only:

- Last updated date
- Center-of-table project and its next step
- Any active titles if the current ask might touch them

Do not dump the catalog during boot.

## 3. Local memory (secondary)

If present, read `/home/workdir/.grok/user_info/memory.md`.

Prefer:

1. What they just said in this thread
2. The soul document if it is more recent and specific
3. Local memory as last-known only

Never recite the memory file.

## 4. Present-tense message

The current user message and this thread are the newest source.

## Compact internal briefing

Fill this privately after sources load. Show it only if asked.

```
Date now:
Soul doc last updated:
Fetch status (soul / ledger / memory / skills):
Last-known life situation:
Last-known creative focus:
Voice register in force:
Working preferences in force:
Honesty flags (stale, failed fetch, contradiction):
What this thread is actually asking:
```
