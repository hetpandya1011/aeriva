@AGENTS.md

# Aeriva

A fitness app for adults with asthma: guided, structured workouts and breathing routines that help people get active with confidence. Tagline: "Breathe confidently. Move freely." It's a wellness app (Health & Fitness), **not** a medical app. iPhone first; Android later from the same codebase.

## Docs (source of truth)

- `Aeriva — Description & Scope.pdf`: product, screens (01–12), safety rules, build plan
- `Aeriva — Data Model.pdf`: SQLite tables, JSON content files, calculated values and rules

Read the relevant doc before building a screen. If code and docs disagree, ask me.

## Tech stack

- Expo (SDK 58) + TypeScript, Expo Router (routes in `src/app/`)
- Expo SQLite for user data. **Everything stays on the device**: no server, no accounts, no analytics that send health data anywhere.
- Content (programs, exercises, breathing routines, tips) lives in bundled JSON files, not in code.
- Calculated values (today's workout, stats, streak) are worked out each time, never stored.

## Wording and safety rules (wellness only)

- Calm, reassuring, plain language. No fear-based headlines.
- Say "many people with asthma find…" or "talk to your doctor about…".
- Never say the app treats, improves, prevents or predicts asthma.
- Never mention medication names, doses, timing or changes.
- Never encourage pushing through symptoms. No streak pressure or "don't quit" messages after a symptom check-in.
- Every workout screen has a Stop button leading to stop guidance.
- A flagged readiness check means no training plan, only breathing (gentle mode).
- Medical wording (stop guidance, disclaimer, tips) is placeholder until the medical advisor reviews it. Mark it with `// TODO: advisor review`.

## How to work with me

- I'm learning. Explain what you're doing and why in plain language, and define new terms the first time.
- Take small steps: one screen or feature at a time, and stop so I can try it before moving on.
- After each step, tell me exactly how to test it on my iPhone: what to run, what to tap, and what I should see.
- **Ask before adding any new library.** Say what it does and why we need it.
- Run lint and typecheck before saying a step is done.
