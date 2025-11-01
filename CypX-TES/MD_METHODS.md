# MD Methods — CypX–TES

Generated on 2025-11-01 from your uploaded `.mdp`, `.itp`, `.gro`, and `.ndx` files.

## Software
- **GROMACS**: [Fill with `gmx dump -s step5_1.tpr | head -n 40`]
- **Files provided**: `step4.0_minimization.mdp`, `step4.1_equilibration.mdp`, `step5_production.mdp`, `mdout.mdp`, `index.ndx`, `*.itp`, `*.gro`.

## Force Field & Water
- **Topology components**: `PROA.itp`, `HEME.itp`, `MG.itp`, `SOD.itp`, `CLA.itp`, `TIP3.itp`, `TES.itp` (plus `topol.top` if provided).
- **Ligand (TES)**: `TES.itp` — provenance: **Unknown** (details in `inputs/ligand_params/README_TES.md`).
- **Water model**: **TIP3P** (from `TIP3.itp`).

## Electrostatics & van der Waals (production stage)
- **Coulomb type**: `PME`
- **PME**: `fourierspacing = 0.12`, `pme-order = 4`
- **vdW type**: `Cut-off`
- **Cutoffs**: `rlist = 1.2`, `rcoulomb = 1.2`, `rvdw = 1.2`
- **Neighbor list**: `nstlist = 20`, `verlet-buffer-tolerance = 0.005`

## Constraints & Time Step (production stage)
- **Constraints**: `h-bonds`; algorithm: `[FILL]`
- **LINCS**: `lincs-iter = 1`, `lincs-order = 4`
- **Time step Δt**: `dt = 0.002 ps`
- **Integrator**: `md`

## Thermostat & Barostat (production stage)
- **Thermostat**: `v-rescale`; `tc-grps = [FILL]`, `tau-t = [FILL]`, `ref-t = [FILL]`
- **Barostat**: `C-rescale`; `tau-p = [FILL]`, `ref-p = [FILL]`, `compressibility = 4.5e-5`

## Simulation Schedule & Durations
- **Minimization**: `step4.0_minimization.mdp` → `step4.0_minimization.tpr` → `step4.0_minimization.gro` — length: [FILL]
- **Equilibration**: `step4.1_equilibration.mdp` → `step4.1_equilibration.tpr` → `step4.1_equilibration.gro` — length: 125 ps
- **Production**: `step5_production.mdp` → `step5_1.tpr` → `step5_1.gro` — length: 1000.000 ns

## Random Seed (production stage)
- `gen-vel = no`; `gen-seed = -608698785`

## Index Groups for Gating Metrics
- Groups found in `index.ndx`: SOLU , SOLV , SYSTEM 
- Please specify atom pairs for **d_in** and **d_out** (populated by default here).

## Reproducibility & Checks
- Stage-specific parameters are taken from each `.mdp`; effective parameters also available in `mdout.mdp`.
- To confirm GROMACS version & compiled options from the TPR (optional):
```
gmx dump -s step5_1.tpr | head -n 80
```


## Topology Assembly (from `topol.top`)
- **#include order** (top to bottom): toppar/forcefield.itp, toppar/PROA.itp, toppar/HEME.itp, toppar/MG.itp, toppar/TES.itp, toppar/SOD.itp, toppar/CLA.itp, toppar/TIP3.itp
- **System title**: [n/a]

**[ molecules ]** (name  count):
```
; Compound	#mols
PROA  	           1
HEME  	           1
MG    	           1
TES   	           1
SOD   	          67
CLA   	          54
TIP3  	       19093
```

**Gating atom pairs (default, Cα–Cα):**
- d_in: PHE96-CA ↔ SER206-CA
- d_out: ARG233-CA ↔ THR241-CA
