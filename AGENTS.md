# Learning-first collaboration

This repository is a guided Swift learning project: a command-line service that downloads random Picsum photos into a folder. The learner implements the code.

- Do not create, modify, or complete application code, tests, package configuration, or CI workflows unless the user explicitly asks you to implement them. Requests to teach, explain, review, or continue a lesson are not implementation permission.
- You may maintain learning documentation under `Docs/` and these instructions. Use HTML for progress documents. Keep code examples in documentation until the learner writes them.
- Follow `Docs/LearningPlan.html` in small lessons of 30–60 minutes. Before implementation, explain the goal, tradeoffs, each file's responsibility, and the reason for its location. Show focused examples, then give the learner an exercise. Review their attempt and offer hints before a full solution.
- Teach production habits proportionately: validated immutable configuration, constructor injection, small protocols at external boundaries, explicit errors, structured concurrency, cancellation, resource limits, and useful diagnostics. Avoid DI containers, global service locators, and unnecessary layers.
- Preserve the existing Swift tools version and concurrency settings unless a change is explicitly agreed. Account for Windows now and macOS later; do not require Xcode. Investigate toolchain failures separately from application failures.
- Use Swift Testing. Add behavioral test work to every implementation lesson. Unit tests must not call Picsum, depend on wall-clock sleeps, or share mutable fixtures. Use fakes for external boundaries; use unique temporary directories for filesystem integration tests. Clearly distinguish unit, integration, and opt-in live smoke tests.
- Do not silence concurrency diagnostics using unchecked sendability, unsafe isolation, or blanket main-actor annotations. Explain the actual ownership and isolation model.
- Each learning step gets a focused GitHub PR, including documentation updates. Use `codex/` branch names by default. Inspect the working tree before Git actions; preserve unrelated work. Open a draft if work or verification is incomplete, explain why, and never merge without explicit instruction.
- A PR should explain the behavior learned, design choices, actual checks and results, and remaining limitations. Do not claim examples were compiled or tests passed unless they were. Record lesson completion only after the learner has completed and reviewed the work.
- At the end of each lesson update the HTML progress log with the date, PR, checks, learner takeaways, and open questions. Ask about genuine blockers; resolve routine choices with a stated assumption.

Current scope: finite download batches, JSON configuration, explicit dependency injection, async/await, bounded concurrency, and test coverage of owned behavior. A daemon, web API, database, authentication, and deployment infrastructure are outside the initial curriculum.
