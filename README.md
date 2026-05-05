# flu_Rt_IHR_mobility

Reproducible code and input files for generating weekly state-level influenza Rt estimates using ARGO(X)-adjusted ILI predictions and a humidity-forced SEIRS + EAKF framework.

## Repository structure

- `notebooks/01_reproduce_argox_seirs_eakf_rt_FIXED.ipynb`  
  Main reproducible notebook.

- `data/`  
  Required input files:
  - `state_preds_argo_step2_long.csv`
  - `state_preds_argo_step2.csv`
  - `ah_daily_allstates.csv`
  - `ah_weekly_WMON_aligned.csv`

- `outputs/`  
  Notebook-generated Rt outputs.

## How to run
Steps to clone the repository. 

1. In a terminal:
bash
git clone https://github.com/bcristol93/flu_Rt_IHR_mobility.git
cd flu_Rt_IHR_mobility
jupyter lab
2. Open the notebook in JupyterLab or Jupyter Notebook.
3. Run all cells from top to bottom.
4. Outputs will be written to the `outputs/` folder.

The notebook uses relative paths, so it should run from the repository root regardless of local computer username or working directory.

## Expected outputs

- `outputs/rt_state_weekly.csv`
- `outputs/Rt_weekly_wide.csv`

## Model summary

Weekly ARGO(X)-adjusted ILI predictions are assimilated into a humidity-forced SEIRS compartmental model using an Ensemble Adjustment Kalman Filter. The final output is weekly posterior Rt by state.
