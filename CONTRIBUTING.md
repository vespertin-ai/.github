# Contributing

Repositories in `vespertin-ai` enforce the following engineering invariants:

1. **Signed Conventional Commits:** Sign every commit with GPG or SSH (`git commit -S`) using `<type>(scope): <description>`. Unsigned commits are rejected by branch rulesets.
2. **Fast-Forward History:** Start short-lived branches from `main` and land via pull request with linear rebase and fast-forward history (no merge commits, no squash merges).
3. **Verified Gates:** Every change must pass automated formatting, lint, specification, and test checks before landing.
