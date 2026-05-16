# Japan -> Kenya Car Import Advisory (Notebook Research)

Data science and AI/ML research workspace for building a car import advisory pipeline.

This repository documents the notebook-first workflow used to collect listing data, engineer features, train pricing models, and prototype landed-cost + ROI decision logic.

## Kaggle Notebook

Primary notebook (public):

- https://www.kaggle.com/code/mwauandrew/japan-kenya-car-import-advisory

## What this notebook project does

- Scrapes and structures Japan car listing data.
- Cleans/normalizes features for modeling.
- Trains and evaluates an ML model for vehicle price prediction.
- Prototypes import tax + landed cost calculation.
- Computes ROI and import/no-import decisions.

## Tools and platforms used

### 1. Kaggle (execution + experimentation)

- Notebook development and experiments were run in Kaggle.
- Used for iterative model training/evaluation and reproducible exploration.

### 2. Firecrawl (data extraction)

- Used to extract vehicle listing content from web sources.
- Helped collect structured attributes needed for model features.

### 3. Google Gemini API (LLM-assisted extraction/cleanup)

- Used in the notebook workflow to assist with content interpretation/structuring where needed.
- Supports extraction quality and consistency when raw listing text is messy.

### 4. Cloud database (PostgreSQL / Neon)

- Scraped/processed data is persisted in cloud Postgres.
- Dataset feeds downstream backend APIs and frontend dashboards.

## AI/ML workflow summary

1. Data ingestion
- Collect listing records from source pages.
- Persist raw/processed records to cloud DB.

2. Data preparation
- Handle missing/dirty values.
- Normalize categorical and numeric fields.
- Build engineered features (e.g., vehicle age and usage patterns).

3. Model training
- Train regression model for price estimation.
- Evaluate with standard regression metrics.
- Export artifact for API inference.

4. Decision analytics
- Estimate CIF/landed cost with tax assumptions.
- Convert USD->KES with live FX strategy in production.
- Compute margin/ROI and recommendation labels.

## Core assumptions prototyped in notebook

- Shipping default around `1200 USD`
- Insurance default around `0.2%`
- Clearing fee midpoint around `200,000 KES`
- KRA tax component logic for duty/excise/VAT/IDF/RDL

These assumptions were later operationalized in the backend service and can be tuned via environment/config.

## Repository scope

This repository is the notebook/research artifact.

Production app layers are maintained separately:

- Backend API repo: `Japan_Advisory_backend`
- Frontend app repo: `kenya-car-intel`

## Reproducibility notes (for data scientists)

- Start from the Kaggle notebook link above for the exact experimental path.
- Keep API keys and DB credentials in environment variables/secrets (never commit them).
- Version model artifacts and feature assumptions alongside evaluation outputs.

## Disclaimer

This project is decision-support tooling, not financial advice. Always validate regulatory/tax assumptions against current official Kenya sources before real transactions.
