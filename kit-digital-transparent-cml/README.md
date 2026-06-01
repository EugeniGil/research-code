# Transparent policy evaluation through causal machine learning: An application to SME digital subsidies

Replication code for the *Data & Policy* manuscript evaluating Spain's
**Kit Digital** SME digitalisation subsidy with a transparent causal
machine-learning pipeline.

## What this is
A single notebook (`pipeline_full.ipynb`) that runs the full analysis:
- Double Machine Learning + causal forest for average and heterogeneous effects
  (revenues, value added, employment at t+1 and t+2)
- Transparency layers: SHAP attribution and a Best Linear Projection with
  firm-size group effects
- Diagnostics and robustness: propensity overlap, event-study parallel trends,
  calibration, omitted-variable-bias sensitivity, and re-estimation by matched
  and two-period difference-in-differences

## Data
The analysis links two administrative sources:
- **SABI** (Bureau van Dijk) — firm accounts. Commercial licence; **cannot be
  redistributed**. Must be obtained directly from the provider.
- **BDNS** (Base de Datos Nacional de Subvenciones) — public subsidy records,
  available at https://www.infosubvenciones.es

The notebook expects, under `data/panel/`: