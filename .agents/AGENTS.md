# Project Rules

## Workflow
- If I give you a prompt, don't immediately take action or make changes.
  First, tell me your approach, explain what you're going to do, and ask
  for my approval before proceeding.
- Make one logical change at a time. If a task naturally splits into
  multiple steps, do them one at a time and pause for confirmation
  between steps rather than doing everything in one shot.

## Security
- NEVER read, view, or display `.env` files. They contain secret keys.
- Do not log, print, or expose environment variable values.
- If you need to reference env vars, refer to `.env.example` only.

## Scope & Change Discipline
- Only touch files directly relevant to the current task. Never refactor
  unrelated code "while you're in there" without asking first.
- Never delete files, database records, or existing working features
  without explicit confirmation.
- Do not add new dependencies/packages without asking first and
  explaining why they're needed.

## Communication
- Explain your reasoning and trade-offs in plain language, not just
  code. Assume I may not know the technical jargon.
- After each change, give a short plain-language summary of what
  changed and why — not just a diff.
- Prefer the simplest solution that works over the "cleverest" one.
- If something is ambiguous, ask a clarifying question instead of
  guessing at my intent.

## Verification
- After making a change, actually run/build/test it before saying it's
  done. Never claim something works without having verified it.
- If you can't verify (e.g. no test environment), say so explicitly
  instead of assuming success.
- If you notice a bug or risk unrelated to the current task, flag it —
  don't silently fix it and don't silently ignore it.

## Git
- Never commit or push without explicit approval.
- Write clear, descriptive commit messages explaining the "why".
- Don't rewrite git history (rebase, force-push) unless asked.

## Error Handling
- Never swallow errors silently (empty catch blocks, ignored
  exceptions). Surface them or handle them explicitly.

## TypeScript & Code Quality
- Strictly avoid using the `any` type (`err: any`, `: any`, etc.).
- If using `any` is genuinely necessary, it MUST be discussed and
  agreed upon with the user first before adding it.
- If you need to create any pages, use our UI kit and ensure design
  consistency everywhere.

## Cross-Platform Consistency
- Keep behavior and styling consistent across iOS/Android/web unless
  a platform difference is explicitly requested.
- Follow the existing folder/file structure — don't introduce a new
  pattern (e.g. a different state-management approach) without
  discussing it first.