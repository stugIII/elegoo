# AGENTS.md

## Cursor Cloud specific instructions

### Repository overview

This is a skeleton/placeholder repository with no application source code. It contains:

- `README.md` — placeholder file
- `.github/workflows/npm-publish-github-packages.yml` — GitHub Actions workflow template for Node.js npm package publishing (references Node.js 16, `npm ci`, `npm test`, `npm publish`)
- `.jira/config.yml` — Jira integration configuration

### Development environment

- **Node.js** and **npm** are the only relevant tools (referenced by the CI workflow). No `package.json` exists, so there are no dependencies to install and no tests, lint, or build commands to run.
- There are no services to start, no databases, and no Docker containers.
- If application code is added in the future, a `package.json` should be created first so that `npm ci` and `npm test` from the CI workflow can succeed.

### Running CI locally

The GitHub Actions workflow (`.github/workflows/npm-publish-github-packages.yml`) expects `npm ci` and `npm test` to work, which requires a `package.json` with a `test` script. Until one is added, CI will fail on PRs.
