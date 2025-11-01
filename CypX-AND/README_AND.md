# CypX–AND (B. subtilis CYP134A1 + Androstenedione)

This directory contains **machine‑readable inputs** and the **exact commands** to reproduce
the AND system setup and production MD used in the manuscript *“Conformational Gating Shapes Substrate Preference of Bacillus subtilis Cytochrome P450 CypX”*.

## Contents (current snapshot)
- `AND.itp`
- `CLA.itp`
- `CypX_TES.rar`
- `EST.itp`
- `HEME.itp`
- `MD_METHODS.md`
- `MG.itp`
- `PIY.itp`
- `PROA.itp`
- `README_AND.md`
- `README_EST.md`
- `SOD.itp`
- `TES.itp`
- `TIP3.itp`
- `a13ed066f5407eccda673a9148fa0348.jpeg`
- `bootstrap_cypx_from_complex_wsl.sh`
- `cypx_1us_segment_runner.sh`
- `cypx_AND_all_in_one_wsl.sh`
- `cypx_APO_all_in_one_wsl.sh`
- `cypx_EST_all_in_one_wsl.sh`
- `cypx_PIY_all_in_one_wsl.sh`
- `cypx_TES_all_in_one_wsl.sh`
- `cypx_full_from_pdb_1us.sh`
- `forcefield.itp`
- `index.ndx`
- `mdout.mdp`
- `prep_commands.txt`
- `run_cypx_AND_wsl.sh`
- `run_cypx_APO_wsl.sh`
- `run_cypx_EST_wsl.sh`
- `run_cypx_PIY_wsl.sh`
- `run_cypx_TES_wsl.sh`
- `step3_input.gro`
- `step4.0_minimization.gro`
- `step4.0_minimization.mdp`
- `step4.0_minimization.tpr`
- `step4.1_equilibration.gro`
- `step4.1_equilibration.mdp`
- `step4.1_equilibration.tpr`
- `step5_1.gro`
- `step5_1.tpr`
- `step5_production.mdp`
- `topol.top`

> After running the production commands in `prep_commands.txt`, you will obtain `seg_01…seg_20` (1 µs total).

## Quick Start
1. Check GROMACS availability: `gmx --version`  
2. Run the commands in **`prep_commands.txt`**.  
3. After `seg_01…seg_20` finish, concatenate with the commands at the bottom.

## Methods Summary
See **metadata/MD_METHODS.md** for force field, PME/cutoffs, thermostat/barostat, dt, stage durations, and seeds.

## Ligand Parameter Provenance (AND.itp)
Document how `AND.itp` was generated (e.g., **CGenFF 2.x/ParamChem** or **GAFF2 + ACPYPE** with **AM1‑BCC**).
Include exact commands & tool versions; keep any log file for traceability.

## Notes
- Trajectories are **not** distributed here; inputs and commands suffice for review and reproducibility tests.
- If required for peer review, consider a **Zenodo** private record and place its URL in your JCIM “Data & Software Availability” statement.
