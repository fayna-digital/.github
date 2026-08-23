# Contributing to Fayna Digital

Thank you for contributing. Every repository in the `fayna-digital` org follows
the **REPO_STANDARD** — clean, sellable, portfolio-grade code. Please read this
before opening a PR.

## Repository naming

- Repo name: `fayna-<essence>` (lowercase kebab-case, no version/tech prefix).
  Example: `fayna-ksef-margin`, NOT `l10n_pl_ksef_margin`.
- The **README H1** must match the repo name.
- The **GitHub description** is one sentence: what it is + stack.
- **Topics** (up to 20) reflect the stack: `odoo, python, ksef, e-invoice, …`.

## Conventional Commits

Every commit message uses the Conventional Commits format:

```
<type>(<scope>): <short summary>
```

Types: `feat`, `fix`, `docs`, `refactor`, `test`, `ci`, `chore`.
Examples:
- `feat: add VAT margin calculation`
- `fix: resolve memory leak in background worker`
- `docs: update API documentation`

## Versioning (SemVer)

- Public repos follow **SemVer** (`MAJOR.MINOR.PATCH`).
- Odoo modules use the Odoo schema `17.0.x.x` internally; the public
  `CHANGELOG.md` still tracks releases by SemVer.
- `CHANGELOG.md` follows **Keep a Changelog** (`## [Unreleased]`, then dated
  releases).

## Required artifacts (root of every repo)

- `README.md` — title = repo name, badges (stack/license), case
  (problem → solution → result → stack), quick start.
- `LICENSE` — LGPL-3 / OPL-1 / MIT as appropriate.
- `CHANGELOG.md` — Keep a Changelog.
- `docs/TZ.md` — spec-driven (6 areas).
- `docs/PLAN.md` — phase plan.
- `tests/` — pytest.
- `.gitignore` — excludes `.env`, `*.pem`, `*.key`, `*.crt`, `*token*`.
- `pre-commit` — ruff + ruff-format + mypy + gitleaks + no-ai-signature.

## Forbidden

- `CLAUDE.md`, `.claude/`, `.roo/` — process trace (hard fail).
- AI co-author trailers (`Co-Authored-By: …`) in commits or files.
- Secrets: `.env`, API keys, tokens, `*.pem`/`*.key`/`*.crt`.

## Pull Request checklist

Use the PR template. Confirm every item before requesting review:

- [ ] README updated if behavior changed
- [ ] LICENSE present
- [ ] CHANGELOG updated under `## [Unreleased]`
- [ ] Tests added/updated and passing
- [ ] `ruff check .` and `ruff format --check .` clean
- [ ] `mypy .` clean
- [ ] No AI signatures, no `CLAUDE.md`/`.claude/`/`.roo/`
- [ ] No secrets
- [ ] Conventional commit title

## CI

Every repo has `.github/workflows/ci.yml` (ruff + pytest + gitleaks) that runs
on every PR. A red CI blocks merge.
