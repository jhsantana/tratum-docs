# ABC Card Engineering

## Always-on engineering policy

- Read the affected code path and callers before editing. Reuse existing patterns and dependencies before adding new code.
- Implement the smallest complete change. Do not add abstractions, configuration, dependencies, or "for later" flexibility without a current need.
- Preserve validation, error handling, authorization, tenant isolation, and public API behavior. Do not expose credentials, tokens, or personal data in code, logs, commands, or responses.
- Add a focused test when behavior changes or logic has branches, loops, parsing, money, security, or persistence. Documentation-only and trivial changes do not need a new test.
- Validate with the narrowest relevant check first. State what was not verified and why.
- Treat database migrations, queues, partner calls, production changes, and destructive operations as explicit approval boundaries. Verify the intended target before acting.

## Repository conventions

- Do not overwrite or discard unrelated changes in a dirty worktree.
- Use `rg` or `rg --files` for discovery.
- Follow the repository's existing build, test, and deployment conventions.

## Git

- Never create a branch named `codex` or starting with `codex/`.
