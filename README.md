# Japan Car Import Advisory Notebook

Research/training notebook for the Japan -> Kenya import advisory workflow.

## Purpose

This notebook was used to:

- Collect and explore vehicle listing data.
- Train/evaluate the price prediction model.
- Prototype cost, tax, landed-cost, and ROI calculations.
- Validate import decision logic before backend productization.

## Current status

Production serving now happens in two separate apps:

- Backend API: `Advisory_backend`
- Frontend UI: `kenya-car-intel`

This repo remains the notebook/research artifact.

## Contents

- `japan-car-import-advisory.ipynb` (main workflow)

## Run locally

```bash
cd Japan-Car-Import-Advisory-Platform-for-Kenyan-Buyers
jupyter notebook japan-car-import-advisory.ipynb
```

## Key assumptions originally prototyped

- Shipping default around `1200 USD`
- Insurance default around `0.2%`
- Clearing fee midpoint around `200,000 KES`
- Live FX conversion and KRA tax components in landed-cost pipeline

These were later carried into backend config and API logic, with live FX handling and DB-backed inventory.
