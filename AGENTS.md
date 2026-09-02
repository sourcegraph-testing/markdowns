# AGENTS.md

Guidance for coding agents working in this repository.

## Project overview

This is a test fixture repository, not a real project. Its README states that it
exists to exercise Sourcegraph batch changes. It contains only Markdown files
plus a placeholder CI workflow — there is no application code.

Some files exist specifically to test text-handling edge cases: `TRAILING.md`
and `NONTRAILING.md` differ in whether the file ends with a trailing newline.

## Repository layout

Flat, single level — there are no source directories.

| Path | Purpose |
| --- | --- |
| `README.md` | Placeholder; states the repo is for testing batch changes |
| `CONTRIBUTING.md` | Heading only, no content |
| `CHANGELOG.md` | Single trivial entry |
| `ANOTHER.md`, `RANDOM.md`, `TESTING.md`, `TESTINGGG.md` | Placeholder Markdown |
| `TRAILING.md`, `NONTRAILING.md` | Fixtures for trailing-newline behavior |
| `.github/workflows/blank.yml` | Unmodified GitHub Actions starter template |
| `.gitignore` | Ignores `.DS_Store` and `.env` |

## Setup, build, test, lint

There is nothing to set up, build, test, or lint. The repository has no package
manager manifest, no Makefile, and no linter configuration. Do not add build
tooling unless a task explicitly asks for it.

`.github/workflows/blank.yml` is the default GitHub Actions starter workflow; it
echoes a greeting and validates nothing. A green CI run here does not mean a
change is correct.

## Conventions

- Content is plain Markdown. No style guide or linter is enforced.
- No formatter runs over this repository, so avoid reflowing or reformatting
  files you were not asked to change.

## Gotchas

- Preserve each file's existing trailing-newline state. `TRAILING.md` and
  `NONTRAILING.md` are fixtures for exactly this; normalizing them defeats their
  purpose.
- Scope edits narrowly. Because the files are near-identical placeholder text, a
  broad find-and-replace can easily touch fixtures a task did not intend to
  modify.
- Treat this repository as disposable test data. Do not rely on anything here as
  an example of production conventions.
