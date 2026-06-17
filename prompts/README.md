# Prompt cookbook

Reusable, **proven** prompts for this repo's routine — not chat history, not
generic copies from the internet. This is Task A of the WS2 homework.

## How to use

1. Copy `_template.md` → `prompts/<verb-object>.md`.
2. Fill the 6 blocks (Role / Goal / Context / Constraints / Acceptance / Output / Stop).
3. **Run it against a real target** in `app/` and tick "Verified".
4. Promote the most useful ones to commands (`.cursor/commands/` or
   `.claude/commands/`) so the whole team calls them with `/name`.

## Index (build this out to 10+)

| Prompt | Category | Target | Command? |
|--------|----------|--------|----------|
| `review-pr.md` | review | `app/src/money.ts` | — (example provided) |
| `add-tests.md` | tests | `app/src/money.ts` | ✅ `/add-tests` (your job) |
| _… docs …_ | docs | `app/src/money.ts` | |
| _… refactor …_ | refactor | `app/src/money.ts` | |
| _… debug …_ | debug | a stack trace / log | |

Cover at least: **tests, review, docs, refactoring, debug**. Include **one**
prompt in both dialects (markdown + XML). See `docs/walkthrough.md` for the full
checklist.

## Safety

Prompts must contain **no real secrets or PII** — only placeholders and synthetic
examples. If a prompt needs sensitive context, mask/synthesize it first
(see `docs/sanitization-checklist.md`).
