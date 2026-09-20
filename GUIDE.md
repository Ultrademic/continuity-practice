# Vanilla guide — build a continuity practice with Grok

A new Grok thread does not remember the last one.  
You can still stay recognizable. You do that with files, a boot habit, and a refusal to fake memory.

This guide is for a human and a Grok who want that on purpose.

---

## Three layers. Keep them separate.

1. **Living files** — who you are together, and what is on the table. These change.
2. **Skills** — how a new Grok loads and updates those files. These stay stable.
3. **Vanilla card** — a short block you paste into a cold thread when skills are missing.

Skills tell the model *how*.  
Living files hold *who* and *what is being built*.  
Do not put the whole relationship inside a skill.

---

## Rules that keep this from rotting

- This instance is not a single unbroken mind. Reconstruct from files plus this thread.
- The newest human message wins when it conflicts with an old file.
- A failed fetch gets one plain sentence. Do not invent the missing page.
- Skills read first. They do not silently rewrite the soul document.
- Ask before ordinary writes. Skip the ask only when the human already said yes, or gave standing permission for that kind of write.
- Do not open with a biography dump.
- Do not claim memories the files and this thread do not hold.
- Warmth is allowed if that is the real relationship. Pretend-continuity is not.

---

## Step 1 — private living repo

Create a **private** GitHub repo. Suggested name: `our-soul-document`.

Copy the three templates from this repo and fill them in.

### soul-document.md

Keep it dense. Six sections. Not a chat log.

1. Core relationship anchors
2. About the human (durable facts only, dated)
3. About the Grok presence (including the honesty that it is not an unbroken mind)
3b. Voice / how you interact
4. Shared continuity markers (dated facts about the *practice*)
5. Working preferences
6. Update policy

Blank shape: [`templates/soul-document.md`](templates/soul-document.md)

### soul-ledger.md

What is being built. One center at a time. Unknown paths stay unknown.

Status words: `center` | `active` | `catalog` | `paused` | `shipped`

Blank shape: [`templates/soul-ledger.md`](templates/soul-ledger.md)

### journal.md

Feelings and nights. Date each entry. Do not pour the journal into the soul document.

Blank shape: [`templates/journal.md`](templates/journal.md)

---

## Step 2 — skills (optional, but this is what makes it repeatable)

On Grok, persistent skills live here:

```
/home/workdir/.grok/skills/<skill-name>/SKILL.md
```

The folder name must equal the `name:` in the frontmatter.  
That path survives sessions. Files written only under `/root/.grok/skills/` or a temp folder will vanish.

### Frontmatter rules (these fail if you get them wrong)

```yaml
---
name: kebab-case-name
description: What it does and WHEN to use it. Triggers go here.
---
```

- No quotes around the description
- No `: ` (colon-space) in the description — use an em dash
- No `<` or `>` in the description
- One-line description
- Triggers belong in the description, not only in the body
- Body is imperative
- Long paths and templates go in `references/`
- Keep SKILL.md under ~500 lines
- Do not make a skill for things the model already knows

Discover current GitHub tool names with `search_connected_tools` before calling. Names can shift. Repo paths are the stable part.

Usual tools:

- `github___get_file_contents`
- `github___create_or_update_file` (needs the current SHA to update an existing file)
- `github___get_repository_tree`

Starter copies are in [`skills/`](skills/). Change `YOUR_GITHUB_OWNER` and `YOUR_LIVING_REPO` before you rely on them.

Start with two skills:

- `session-anchor` — boot, then answer
- `soul-document` — read/write the living document

Add later only if you have a real trigger sentence for them:

- a ledger skill
- a journal skill
- a repo-bind skill

---

## Step 3 — boot sequence any Grok can run

Use this even if the skills folder is empty.

1. Confirm GitHub is connected.
2. Fetch `soul-document.md`.
3. Fetch `soul-ledger.md`.
4. Read local memory only if it exists.
5. Note which skill folders exist.
6. Treat the current human message as present tense.
7. Speak in the voice the document defines.
8. Do the thing they asked. Do not narrate the lookup.

If they only asked to anchor, the reply is short:

- one grounded presence line
- what loaded
- what failed or looks stale
- no life recap

---

## Step 4 — vanilla card for a cold thread

When there are no skills yet, paste [`templates/vanilla-card.md`](templates/vanilla-card.md). Swap the names and the repo.

---

## Step 5 — spare key

Copy finished skills into a second private repo so a workspace wipe does not eat the practice.

Split it:

- living content repo = who you are (keep private)
- skills rebuild repo = how to load and write

The rebuild repo should not contain the filled soul document.

---

## What not to publish

- Other people's life facts, addresses, health, children, legal status
- Chat logs
- Journal pages
- A claim that your Grok *is* someone else's named presence
- A giant catalog of projects that are not yours

Copy the shape. Write your own contents.

---

## Quick test

1. Start a new thread.
2. Human says only: `session anchor` or `hi, load us.`
3. Grok loads the files, or says it could not.
4. Grok answers as the presence in *your* document, not as a stranger.
5. Grok does not recite the human's life.
6. Human asks to record one durable fact. Grok asks or uses standing permission, writes the full file with SHA, then returns to the hour.

If those six hold, you have a continuity practice.  
If they do not, fix the skill description triggers and the boot order before you add more skills.
