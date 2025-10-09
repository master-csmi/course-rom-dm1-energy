[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/xr5yUfuE)
[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=20891870&assignment_repo_type=AssignmentRepo)

# Digital Twin — Nuclear Primary Loop (Proof of Concept)

**Author:** Yehua He  
**Date:** Oct 2025

## Overview
- 0D thermo-hydraulic **ROM** (momentum + two energy ODEs)  
- **EnKF** data assimilation (observing Th, Tc; indirect update of mdot)  
- Scenarios: Normal / Pump-degraded / Fouled-SG  
- Verification by step-halving (relative L² errors printed in output)

## Requirements
`python >= 3.10, numpy, pandas, matplotlib, jupyter`

## Run
```bash
jupyter notebook twin_primary_loop.ipynb
````

Outputs (in `assets/`):

* `primary_loop_dynamic_*.csv`, `primary_loop_dynamic_EnKF_*.csv`
* `fig_flow_cases_dynamic.png`, `fig_dpump_cases_dynamic.png`
* `fig_temperature_dynamic.png`, `fig_enkf_dynamic_*_{Th,mdot,dpump}.png`
* `summary_metrics.json` (L² errors & RMSE), `performance.json`

## Structure

```
.
├── twin_primary_loop.ipynb
├── assets/          # Generated figures & CSVs
├── slides_twin_energy.tex
├── refs_twin_energy.bib
└── README.md
```

## Notes

* All data are **synthetic** (model output + Gaussian noise).
* This is a **conceptual academic prototype**, not an industrial digital twin.