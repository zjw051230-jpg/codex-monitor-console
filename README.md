# Codex Monitor Console

A local workbench for running repository automation tasks and inspecting each step from a browser. It combines a React/Vite client, a Node server, task persistence, skill loading, audit previews, and end-to-end smoke tests.

## Run locally

```bash
npm ci
npm run db:init
npm run dev
```

On Windows, `start-workbench.bat` starts the workbench with the repository's default setup.

## Useful commands

```bash
npm test                # unit and integration tests
npm run build           # production client build
npm run smoke           # basic smoke test
npm run skills:audit    # validate installed skills
npm run smoke:e2e-real:dry-run
```

## Repository layout

- `src/`: browser client and adapters.
- `server/`: local API, task runner, and persistence.
- `skills/`: task skills used by the runner.
- `schemas/`: shared task and artifact schemas.
- `e2e/`: browser-level checks.
- `scripts/`: setup, verification, and smoke-test entry points.
- `agent(2)/`: earlier Python agent implementation kept for reference.

The workbench is intended for local development. Keep provider keys and repository-specific credentials in local environment files, not in Git.
