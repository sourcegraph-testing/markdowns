# AGENTS.md

## Repository Purpose
This is a sandbox/test repository used to experiment with Sourcegraph Batch Changes.
It contains no production code. Do not treat it as a functional project.

## Language
All content is Markdown. There is no compiled or interpreted source code.

## Directory Structure
- `.github/workflows/blank.yml` — placeholder GitHub Actions CI (non-functional)
- `*.md` — various Markdown files used as targets for batch change experiments

## Build, Test, and Lint
There are no build, test, or lint commands. The CI workflow is a stub and performs no
meaningful checks. Do not attempt to run tests or linters — none exist.

## Making Changes
- All changes should be to `.md` files.
- There is no review process defined beyond the stub `CONTRIBUTING.md`.
- PRs targeting the `main` branch trigger the placeholder CI workflow, which
  always passes regardless of content.

## Key Constraints for Agents
- Do not add source code files; this repo is Markdown-only by design.
- Do not rely on CI green status as a signal of correctness — the workflow is a no-op.
- The `CHANGELOG.md`, `CONTRIBUTING.md`, and `TESTING.md` files are stubs; do not
  treat them as authoritative documentation.
