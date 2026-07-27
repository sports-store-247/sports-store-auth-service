# sports-store-auth-service

FastAPI microservice handling user registration, login, and JWT issuance/verification
for the Sports Store platform. Owns the `auth_db` MongoDB database. Every other
backend service trusts the shared `JWT_SECRET` to verify tokens this service issues.

## Stack

FastAPI, MongoDB (Motor), pytest.

## Local development

```bash
cp .env.example .env
pip install -r requirements.txt
uvicorn main:app --reload
```

Health check: `GET /health`.

## Branching convention

- `feature/<short-description>` — new functionality
- `bugfix/<short-description>` — non-urgent fixes
- `hotfix/<short-description>` — urgent production fixes

All changes land on `main` via pull request with at least 1 approval (enforced by repository ruleset).
