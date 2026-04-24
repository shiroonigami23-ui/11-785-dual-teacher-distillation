# Contributing

Thanks for contributing to this project.

## Branch and PR workflow
1. Create a feature branch from `main`:
   - `git checkout -b feat/<short-topic>`
2. Make small, focused commits.
3. Push your branch and open a Pull Request.
4. Ask at least one teammate to review before merging.

## Commit style
Use clear commit messages, for example:
- `feat: add EER evaluation script`
- `fix: correct SV projection dimension mismatch`
- `docs: update report links`

## Contribution visibility (important)
To ensure each member's contribution appears on GitHub:
- Use your own GitHub account.
- Push from your own branch.
- Open PRs from your account.
- Avoid one person pushing everyone else's work.

## Code quality
- Keep notebook sections modular and documented.
- Do not commit large model checkpoints to git.
- Store heavy artifacts outside the repo or use Git LFS if needed.

## Pull Request Checklist

Before submitting a pull request, please ensure that:

- [ ] Your branch is up to date with `main`.
- [ ] Changes are limited to a single feature or fix.
- [ ] Code and notebooks have been tested locally.
- [ ] Documentation has been updated, if necessary.
- [ ] Commit messages follow the repository conventions.