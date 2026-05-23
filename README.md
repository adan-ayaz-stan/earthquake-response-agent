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

## Team Roles
- ML pipeline
- Agent + CSP
- Knowledge base + integration
- Frontend + documentation

## Problem Statement ( ML Training )
- We are predicting `FloodProbability` in our dataset.
- Inputs are the following columns:
```
Index(['id', 'MonsoonIntensity', 'TopographyDrainage', 'RiverManagement',
       'Deforestation', 'Urbanization', 'ClimateChange', 'DamsQuality',
       'Siltation', 'AgriculturalPractices', 'Encroachments',
       'IneffectiveDisasterPreparedness', 'DrainageSystems',
       'CoastalVulnerability', 'Landslides', 'Watersheds',
       'DeterioratingInfrastructure', 'PopulationScore', 'WetlandLoss',
       'InadequatePlanning', 'PoliticalFactors', 'FloodProbability'],
      dtype='object')
```
- Decision Support : To be determined
- What the system outputs beyond prediction ( recommendation actions ) : TBD