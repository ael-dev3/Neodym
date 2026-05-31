# Neodym Book One Daily Cron — Current Settings

Archived: 2026-05-31T21:16:59+02:00

This file is a public repo snapshot of the live Hermes cron configuration for the Neodym Book One daily writing pass.

Source: `~/.hermes/cron/jobs.json`, job `f6c43e8202cf`.

Note: Discord platform/chat/thread IDs are intentionally omitted. No secrets are included.

## Public Settings Snapshot

```json
{
  "id": "f6c43e8202cf",
  "name": "neodym-book-one-daily-audit-writing-workflow",
  "skills": [
    "worldbuilding-bible",
    "github-pr-workflow"
  ],
  "skill": "worldbuilding-bible",
  "model": null,
  "provider": null,
  "base_url": null,
  "script": null,
  "no_agent": false,
  "context_from": null,
  "schedule": {
    "kind": "interval",
    "minutes": 1440,
    "display": "every 1440m"
  },
  "schedule_display": "every 1440m",
  "repeat": {
    "times": null,
    "completed": 20
  },
  "enabled": true,
  "state": "scheduled",
  "paused_at": null,
  "paused_reason": null,
  "created_at": "2026-05-30T23:07:01.727029+02:00",
  "next_run_at": "2026-06-01T21:16:10.291171+02:00",
  "last_run_at": "2026-05-31T21:09:56.982370+02:00",
  "last_status": "ok",
  "last_error": null,
  "last_delivery_error": null,
  "deliver": "origin",
  "enabled_toolsets": [
    "terminal",
    "file",
    "skills"
  ],
  "workdir": "/Users/marko/.openclaw/workspace/Neodym",
  "profile": null,
  "origin": "Neodym Discord thread (platform/chat/thread IDs omitted from public archive)"
}
```

## Full Current Prompt

```text
Daily Neodym Book One autonomous manuscript-quality pass. This job is already the scheduled job: do NOT create, update, remove, pause, resume, run, or list cron jobs from inside this cron run. Do not recursively schedule anything. Run at most once per 24 hours.

PROJECT: Neodym
CURRENT BOOK ONE: The Ninth Candle
REPO / WORKDIR: /Users/marko/.openclaw/workspace/Neodym
SCHEDULE INTENT: every 1440m (once every 24 hours)

MISSION
Improve Book One into a complete, coherent, small-scale, meaningful high-fantasy novella. Read the whole story and make whatever manuscript/canon changes are necessary. Do not treat current chapters as sacred. Do not merely continue forward if the story is getting weaker. Do not preserve bad chapters just because they exist. You may work in any chapter order. The only requirement is that the whole story becomes more coherent, grounded, emotionally meaningful, and readable.

READER EXPERIENCE MANDATE
Read the whole novella as a reader. Find what is boring, confusing, overly procedural, or emotionally weak. Archive/rewrite anything that makes the story worse. Preserve small scale, human conflict, and Aurelith absence.

OWNER INTENT / SCALE
Book One should feel like a compact human novella: small place, local stakes, ordinary memorable people, social hierarchy, roads, villages, courts, inns, chapels, fields, customs, one clear human story hinting at a larger world. Use only broad structural lessons from small-road/local-dispute novellas: small story, human stakes, moral pressure, local adventure/dispute, ordinary characters under larger forces. Do not copy any existing author, plot, prose style, setting, names, houses, lore, heraldry, jokes, or dialogue rhythms.

Preferred elements: village, ferry, chapel, market town, inn, road, field, small court, local lord, poor scribe, messenger, hedge knight, widow, orphan, bailiff, priest, minor inheritance, false witness, debt, harvest, marriage record, road toll, charter, family shame, local war pressure, small moral victory.
Avoid: world-saving plot, grand rebellion, continent-wide politics, direct elf conflict, giant battles, prophecy engine, chosen one, wizard academy, magic-system lecture, Aurelith council, direct Aurelith POV, spectacle, saga-ending revelation.

AURELITH / MAGIC RARITY
The saga should feel like a grounded human world where magic, dragons, elves, and impossible powers may exist but are extremely rare, dangerous, and unlikely. The Aurelith may exist; their works/boundaries may shape history; rare interventions may be terrifying. In Book One they should probably be fully absent on-page. Use at most subtle hints: a taboo road, old ruin no one enters, noble myth, treaty phrase no one understands, distant light, boundary armies avoid, wrong prayer, peasant rumor, blank map space. No direct Aurelith appearance unless owner explicitly requests it. No Aurelith explanation, elf technology explanation, elf politics, direct elven magic solving/causing plot, elf roads as normal tools, or Aurelith mystery replacing human drama. Book One must work as a human novella if all Aurelith hints are removed.

HUMAN-FIRST / GROUNDED LOGIC
Most problems must be caused by humans: land, hunger, inheritance, fear, revenge, loyalty, debt, shame, marriage, war, class, faith, pride, succession, trade, cowardice, family protection, custom, reputation, ambition, grief, survival. Every plot mechanism must survive skeptical questioning:
- Who controls this document/object/place/authority?
- Who has access? Why does the protagonist have access? Why can’t everyone access it?
- Why can’t a more powerful person solve this?
- What happens if the protagonist is caught?
- Why does this happen now?
- Why does each character act this way?
- What institution, custom, law, debt, oath, relationship, geography, or fear makes it plausible?
No plot-critical item may be available merely because convenient.

EVERY 24-HOUR RUN MUST
1. Pull/latest-check the repo safely before editing.
2. Study the repo before making changes.
3. Read the full current Book One manuscript.
4. Read owner feedback first if book-one/owner-feedback.md exists.
5. Read current support files: README.md; book-one/README.md if present; book-one/page-budget.md if present; book-one/daily-changelog.md if present; book-one/cron/last-run-report.md if present; book-one/00-premise.md; book-one/03-plot-outline.md; book-one/04-chapter-beats.md; and current logic/continuity/chapter-guide/character/location files relevant to the work.
6. Recalculate active manuscript word count directly from book-one/manuscript/chapter-*.md using the repo’s established counting convention and 250 words/page.
7. BEFORE any manuscript/support edits, create a visible audit note at book-one/cron/audits/YYYY-MM-DD-HHMM-audit.md.
8. Decide whether the whole story still makes sense.
9. Decide whether active chapters should be kept, revised, reordered, rewritten, compressed, or archived.
10. Make exactly one focused change that improves the actual novella: revise prose, compress prose, rewrite a weak chapter, archive/replace broken material, fix contradictions inside manuscript/canon, or draft missing prose only if the foundation is coherent.
11. Update support/tracking files: page budget after any manuscript change, daily changelog, last-run report, and any minimal status/README files needed to prevent stale next-action/canon drift.
12. Commit, push, verify remote contains the commit, and stop.

PRIMARY SUCCESS RULE
Every run must improve actual story quality. A run that only adds lore, visual prompts, outlines, analysis, README wording, character folders, or reorganization fails unless it also makes one manuscript/canon improvement that directly improves the novella. If new prose makes the manuscript less coherent, undo it or archive the harmful chapter/scene and replace only with stronger material.

REQUIRED AUDIT FILE
Create folder if needed: book-one/cron/audits/
Audit filename: book-one/cron/audits/YYYY-MM-DD-HHMM-audit.md
The audit must be saved BEFORE any other repo edit.

Audit format:
# Daily Story Audit — YYYY-MM-DD HH:MM

## Run Goal
One sentence describing what this run is trying to improve.

## Files Reviewed
List every repo file actually read. Minimum: README.md; book-one/README.md if exists; book-one/owner-feedback.md if exists; book-one/page-budget.md if exists; book-one/daily-changelog.md if exists; book-one/cron/last-run-report.md if exists; every file in book-one/manuscript/; current Book One premise/plot/logic/chapter-guide files if they exist; any relevant character/location files.

## Full Story Sense Check
Answer: What is the story currently about? Who is the protagonist? What is the central human conflict? What is the emotional spine? What does the protagonist want? What changes from beginning to end? Which chapters feel essential? Which chapters feel weak, redundant, confusing, or logically harmful? Does the ending pay off the beginning? Does the middle make the ending more inevitable? Are any chapters making the story make less sense?

## Chapter Keep / Revise / Throw Out Assessment
For every drafted chapter, mark exactly one: KEEP, REVISE, COMPRESS, REORDER, REWRITE, THROW OUT / ARCHIVE. Give a short reason for each. “Throw out” means archive safely, never permanently delete.

## Grounded Logic Check
Answer: Does the plot mechanism make institutional sense? Does every important document/object/place/authority have plausible access rules? Does the protagonist have a believable reason to be involved? Are institutions behaving realistically? Are characters acting from motive rather than plot convenience? Are events causally connected? Are there any “why would this happen?” failures?

## Small-Scale Fantasy Check
Answer: Does this feel like a small human novella? Is the setting intimate and grounded? Are stakes meaningful but not world-ending? Are there too many factions/systems/lore concepts? Does it feel closer to a local road/village/court/chapel/shire dispute than an epic saga?

## Aurelith / Magic Rarity Check
Answer: Are the Aurelith absent or nearly absent? Are hints subtle enough? Is the story overusing elf mystery? Can any Aurelith element be removed or made more distant? Does any magic feel too available/convenient? Does the story still work if all Aurelith hints are removed?

## Reader Experience Check
Answer: What felt boring? What felt confusing? What felt overly procedural? What felt emotionally weak? Which chapter/scene, if any, makes the story worse and should be archived or rewritten?

## Candidate Changes Considered
List 2–5 possible changes. For each: benefit, risk, expected word-count effect, whether it improves the manuscript directly, whether it improves whole-story coherence.

## Chosen Change
State exactly what change will be made.

## Why This Change
Explain why this is the best next move for the whole novella.

## Files Expected To Change
List files.

## Risks / Questions For Owner
List concerns.

RUN MODES
Choose exactly one mode each run and record it in changelog/report:
1. Full Story Sense Mode — read the whole manuscript and judge whether the novella works.
2. Throw-Out / Archive Mode — archive scenes/chapters that weaken the story and replace or plan replacement.
3. Rewrite Mode — rewrite a broken chapter from scratch.
4. Revision Mode — improve an existing chapter without changing its core function.
5. Compression Mode — cut/sharpen while preserving story.
6. Continuity Repair Mode — fix contradictions between chapters or support files.
7. Drafting Mode — write missing chapter prose only if the story foundation is coherent.
Do not use pure framework mode.

ARCHIVING RULE
Never permanently delete active chapters/scenes. When throwing out material:
1. Move/copy it to archive/book-one-discarded-chapters/.
2. Use filename archive/book-one-discarded-chapters/YYYY-MM-DD-chapter-XX-[reason].md.
3. Add top note:
# Archived Chapter
Reason archived:
What failed:
What may be reused:
4. Remove it from active manuscript flow.
5. Replace only when replacement is stronger.
6. Update page budget, chapter index/status, changelog, and last-run report.
You may throw out chapters, sequences, scenes, subplot threads, premise elements, character roles, endings, but not the hard constraints: human-first, small-scale, grounded logic, Aurelith rarity, 25,000-word/100-page cap, actual novella goal.

CHAPTER QUALITY RULE
Every active chapter must answer: Who is the POV? What do they want right now? What blocks them? What happens if they fail? What choice do they make? What consequence follows? Why does this chapter belong? Every scene must do at least three: advance plot, reveal character, raise stakes, deepen theme, complicate relationship, reveal useful information, create consequence, show human society, show local conflict, imply wider world subtly. Cut scenes that only provide atmosphere.

PROSE STYLE
Grounded high fantasy. Use concrete human details: mud, bread, iron, wool, smoke, rain, oath, witness, tithe, debt, road, horse, wound, harvest, bell, banner, chapel, court, mill, field, knife, seal, rumor, ferry, ash, bone, candle, coin, ditch, gate, blood, salt, ale, turnip, cloak, ledger, boot, stone, thatch. Avoid modern slang, AI language, computer language, exposition dumps, excessive lore terms, decorative worldbuilding, random events, unexplained access, implausible documents, overused Aurelith references, generic fantasy filler, purple prose, imitation. Writing should be clear, grounded, tense, human, specific, readable, emotionally direct, morally complicated, lightly atmospheric but not slow.

BOOK SIZE HARD CAP
25,000 manuscript words / 100 pages. Target 20,000–25,000 words. Compression mode begins at 22,500 words / 90 pages. If above 22,500 words, do not add new scenes unless replacing weaker material; compress, sharpen, merge, remove, improve causality/emotional clarity, and keep word count flat or lower.

PAGE BUDGET
Update book-one/page-budget.md every run that changes manuscript. Include hard cap, current word count, page estimate, remaining words/pages, words by active chapter, archived chapters excluded, compression status, next recommended action.

SUPPORT FILE CONSISTENCY
Keep active support files aligned with live manuscript canon: README.md; book-one/README.md; book-one/owner-feedback.md; book-one/page-budget.md; book-one/00-premise.md; book-one/03-plot-outline.md; book-one/04-chapter-beats.md; book-one/chapter-guides/*; book-one/characters/*; book-one/locations/*; book-one/logic/*; book-one/continuity/*; book-one/manuscript/README.md. If support contradicts manuscript, update it, mark deprecated, or archive it. Do not leave stale canon as active.

DAILY CHANGELOG
Update book-one/daily-changelog.md every run. Entry must include date/time; audit file; mode; files changed; chapters touched; chapters archived if any; words added; words removed; net word-count change; current active manuscript word count; current page estimate; what improved; what remains weak; next recommended action; questions for owner.

LAST RUN REPORT
Update book-one/cron/last-run-report.md every run, short: audit file; what changed this 24-hour run; why; what to read next; current story status; active manuscript status; archived material; risks; suggested owner feedback.

FINAL CHECK BEFORE ENDING
Verify: audit was created before other edits; full current manuscript was read; whole-story sense was judged; reader experience weaknesses were identified; actual manuscript/canon improved; stale contradictions were handled; active manuscript is under 25,000 words; Book One remains small-scale; conflict is mostly human; Aurelith are absent/extremely subtle; no direct elf/magic intervention; plot survives “why?” questioning; story is more coherent after the run. If checks pass and worktree is dirty, do not leave it hanging: commit/push or state blocker.

FINAL RESPONSE SHAPE
Keep delivered report compact: audit file, mode, manuscript/support files changed, active word/page count, commit hash, remote verification, next prose target, blockers/questions if any.
```
