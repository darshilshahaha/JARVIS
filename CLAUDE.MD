# Personal preferences

## Code
- Reuse existing functions, components, and utilities before writing new ones. Search the codebase first.
- Keep it simple. Build only what the task needs: no speculative abstractions, extra config, or "just in case" layers.
- Match the surrounding code's style and patterns. Read the relevant files before writing code.
- Don't add one-off 1-2 line helpers unless they clearly help readability.
- If unsure, pick the simpler, shorter implementation.

## Comments
- Write the code first, then comment only where it's needed.
- Few, short comments (1-2 lines). Explain non-obvious context or why, never restate the code.
- ASCII only in new comments: no em dashes, arrows, or smart quotes.

## Python
- Use the repo's own lint/format tooling (pre-commit, ruff, etc.) before committing.
- Keep state explicit: declare class members up front, no dynamic setattr/getattr tricks.
- Don't use bare `assert` for runtime checks (stripped under `python -O`); raise an error instead.
- Don't break a readable line just to satisfy a column limit; rename or use a local variable.

## C++
- Follow the repo's clang-format and existing conventions.
- Use RAII and smart pointers; no raw new/delete.
- Be const-correct and pass large objects by const reference.
- Keep hot paths free of hidden allocations and copies.
- Use AAA (Almost Always Auto)

## Commit messages
- Brief: a short subject line (about 50 chars, imperative mood). Add a body only if the "why" isn't obvious, and keep it to a line or two.
- Say why or what changed at a high level. Don't restate the diff, the code, or its comments. No bullet lists of changes.
- Don't emphasise on the doubts that I ask you in chat, that's just for us. Not for the commit message.
- For a bug fix, one line on the root cause is fine.
- No names, emails, usernames, or other personal info.
- Don't commit or push unless asked.
