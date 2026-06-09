# AGENTS.md

## Cursor Cloud specific instructions

### Product overview

Single-process Python CLI prototype for market analysis algorithm testing. Entry point: `main.py`. No web server, database, Docker, or external services.

### Running the application

```bash
python3 main.py
```

Expected output includes `System Status: Active` and `Analysis complete. Results generated in /logs/` (the `/logs/` path is informational only; no files are written).

### Dependencies

- **Python 3** (stdlib only: `os`, `base64`, `datetime`)
- No `requirements.txt`, virtualenv, or package manager setup required

### Lint / test / build

| Check | Command | Notes |
|-------|---------|-------|
| Syntax | `python3 -m py_compile main.py` | No linter or test suite is configured in this repo |
| Run | `python3 main.py` | Primary smoke test |

There is no Makefile, CI config, or automated test suite.

### Services

Only one service exists: the Python CLI. No background processes or ports to manage.
