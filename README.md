# Fayna Digital — `.github`

Org-wide defaults for the `fayna-digital` GitHub organization. This repo is the
single source of truth for community health files and CI templates that apply to
every repository in the org.

## Contents

| Path | Purpose |
| :--- | :--- |
| `profile/README.md` | Organization profile shown on the org landing page. |
| `.github/PULL_REQUEST_TEMPLATE.md` | Default PR template (firm-gate checklist). |
| `.github/ISSUE_TEMPLATE/bug.md` | Bug report template. |
| `.github/ISSUE_TEMPLATE/feature.md` | Feature request template. |
| `.github/workflows/ci.yml` | Default CI: ruff + pytest + gitleaks. |
| `.github/CODEOWNERS` | Org-wide default code owners. |
| `CONTRIBUTING.md` | Contribution rules: naming, Conventional Commits, SemVer, artifacts. |

## How it works

GitHub automatically applies the org-level community health files
(`CONTRIBUTING.md`, PR/Issue templates, `CODEOWNERS`) to every repo that does
**not** define its own. Repos that need a custom CI copy the workflow from
`.github/workflows/ci.yml` into their own `.github/workflows/`.

## REPO_STANDARD

The full standard (naming, required artifacts, About metadata, cleanliness,
commits, CI) lives in the org's `REPO_STANDARD.md` and is enforced by
`firm-gate.sh`. Every new repo must pass the gate before publication.
