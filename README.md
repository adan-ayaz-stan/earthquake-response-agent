# Flood Disaster Agent

Intelligent Flood Disaster Prediction & Decision System

**Dataset Domain:** Flood Risk / Disaster (rainfall, river levels, humidity, temperature → flood risk level)

**Objective:** Build a full intelligent pipeline: raw data → ML prediction → AI agent → CSP → Knowledge Base → Frontend

## Branching Strategy

- **main**: production — always deployable. Protect with branch rules; only merge tested release PRs.
- **dev**: staging — integration branch for QA and preview environments.
- **feature/***: short-lived feature branches off `dev` (naming: `feature/<short-desc>`). Open PRs into `dev` when ready.
- **hotfix/***: branch off `main` for urgent fixes; merge back into both `main` and `dev`.

Keep it simple: develop in `feature/*` → PR to `dev` → test in staging → merge to `main` for release.

## How to Run

- First set up virtual env at root by `python -m venv venv`.
- Activate source by `source venv/bin/activate`.
- Install deps by `pip install -r requirements.txt`.
- Run the backend server by `uvicorn app.main:app --reload`.
- Access API docs at `http://localhost:8000/docs`.

Frontend is in `frontend/` — run with `npm install` and `npm start` to access at `http://localhost:3000`.
