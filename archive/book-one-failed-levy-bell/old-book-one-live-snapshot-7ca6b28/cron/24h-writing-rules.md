# 24h Writing Rules

## Schedule

Suggested cron pattern: `0 6 * * *`.

## Daily run order

1. Pull the latest `main` branch.
2. Read `book-one/owner-feedback.md` first.
3. Read `book-one/page-budget.md`.
4. Read `book-one/chapter-guides/chapter-status.md`.
5. Read `book-one/chapter-guides/chapter-index.md`.
6. Read all existing `book-one/manuscript/chapter-*.md` files.
7. Read character and location indexes.
8. Read individual character/location folders relevant to the next chapter or revision target.
9. Recalculate manuscript word count directly from chapter files.
10. Choose one mode: drafting, revision, compression, continuity, or organization.
11. Make exactly one focused improvement.
12. Update affected character, location, chapter, continuity, budget, changelog, and cron report files.
13. Commit, push, and verify remote `main`.

## Mode priority

- If not all chapters are drafted and manuscript is under 22,500 words: prefer drafting the next missing chapter.
- If Chapter 1 or latest owner feedback identifies a weak chapter: revise before drafting.
- If over 22,500 words or 90 pages: compression mode only.
- If indexes drift from manuscript: continuity or organization mode.

## Hard constraints

- Human POV only, default Nera close third.
- Human conflict first: war, debt, hunger, roads, witness, class, family, fear.
- Aurelith thin-veil only: Starvel Field, white stones, taboo, lowered banners, bad maps, distant mystery.
- No Aurelith POV, direct Aurelith administrator, chosen child, rebellion epic, or lore encyclopedia.
- Never exceed 25,000 manuscript words.
- Do not create or edit additional cron jobs from inside a cron run.

## Required report fields

Each daily changelog entry must include date, mode, files changed, chapter worked on, words added, words removed, net manuscript word-count change, current manuscript count, page estimate, remaining words before cap, character folders updated, location folders updated, what improved, what remains weak, next recommended action, and questions for owner.
