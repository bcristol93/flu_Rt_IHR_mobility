# Project Overview

This repository contains reproducible workflows for influenza Rt estimation using ARGO(X)-adjusted ILI observations with a humidity-forced SEIRS-EAKF framework.

Primary notebook:
- notebooks/01_reproduce_argox_seirs_eakf_rt_FIXED.ipynb

Current implemented scope:
- Weekly state-level Rt estimation
- ARGO-adjusted ILI inputs
- Absolute humidity forcing
- SEIRS + EAKF assimilation

Planned/ongoing extensions:
- Mobility analyses
- IHR/severity integration
- Influenza subtype clustering
- Validation workflows

Important input data:
- state_preds_argo_step2_long.csv
- state_preds_argo_step2.csv
- ah_daily_allstates.csv
- ah_weekly_WMON_aligned.csv

Guidelines:
- Preserve reproducibility
- Do not overwrite raw inputs
- Save new outputs into separate folders
- Avoid modifying archived notebooks unless explicitly requested
- Prefer additive edits over destructive rewrites
- Explain major modeling changes before implementing

Research context:
This work supports dissertation aims focused on influenza transmission dynamics, mobility, and severity modeling.
