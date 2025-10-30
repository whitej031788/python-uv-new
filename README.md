# Python UV FastAPI Scaffold

A minimal FastAPI application managed with uv.

## Quickstart

1) Install dependencies (requires `uv`):

```
uv sync
```

2) Run the server:

```
uv run uvicorn main:app --reload
```

3) Verify it's running:

- Open the interactive docs: `http://127.0.0.1:8000/docs`
- Or hit the OpenAPI JSON: `http://127.0.0.1:8000/openapi.json`

4) Example request (register a user):

```
curl -X POST http://127.0.0.1:8000/api/v1/auth/register \
  -H 'Content-Type: application/json' \
  -d '{"username":"alice","password":"secret","email":"alice@example.com"}'
```

## Notes

- The app uses SQLite for workshop/demo convenience.
- CORS is permissive and security is intentionally relaxed for workshop purposes.
 - If you see `ImportError: email-validator is not installed`, run `uv sync` again after pulling the latest `pyproject.toml`.
