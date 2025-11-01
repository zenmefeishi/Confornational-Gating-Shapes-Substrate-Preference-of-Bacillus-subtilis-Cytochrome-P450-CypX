# CypX–PIY — MD Reproducibility Pack

This folder provides minimal inputs & commands to verify the PIY complex MD setup
of *Bacillus subtilis* CYP134A1 (CypX).

> Generated on 2025-11-01 from your uploaded PIY files.

## What’s included

- Topology include order & molecules table have been extracted from `topol.top` and appended to `metadata/MD_METHODS.md`.
- `metadata/MD_METHODS.md` — Methods summary (auto‑filled from stage `.mdp` + `mdout.mdp`).
- `prep_commands.txt` — Three commands for **min → eq → prod**.
- Stage inputs: `step4.0_minimization.mdp/.tpr/.gro`, `step4.1_equilibration.mdp/.tpr/.gro`, `step5_production.mdp/.tpr/.gro`
- Topology & params: `PROA.itp`, `HEME.itp`, `MG.itp`, `SOD.itp`, `CLA.itp`, `PIY.itp`, `TIP3.itp`
- Index: `index.ndx` (default gating pairs are noted in MD_METHODS.md)

## Quick start
```bash
bash prep_commands.txt
```

## Notes
- JCIM does not require `.xtc/.trr/.edr` trajectories; they are intentionally omitted.
- If PIY uses different gating atom pairs from the default (Cα–Cα: PHE96–SER206; ARG233–THR241),
  update them in `metadata/MD_METHODS.md` and/or provide named groups in `index.ndx`.
