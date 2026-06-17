# app — cookbook target

A tiny TypeScript module used as a **real target** for your prompt cookbook
(Task A): tests, review, refactor, docs, debug prompts all point here.

```bash
cd app
npm install
npm test          # vitest — smoke tests pass
npm run typecheck
```

## What's inside

- `src/money.ts` — integer-cent money helpers (`formatCents`, `parseAmount`,
  `splitEvenly`, `applyDiscount`).
- `src/money.test.ts` — minimal smoke tests that pass.

## On purpose

`src/money.ts` has at least one **subtle correctness gap** (look at how
`splitEvenly` handles remainder cents) and a couple of missing-validation spots.
Don't hand-fix them — use a cookbook prompt (e.g. `/review` or `/add-tests`) to
surface and fix them. That's the exercise.
