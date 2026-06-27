# Molecular Dynamics Trajectory Analysis

> **Practical — Research Master's Degree in Bioinformatics (Bio Data Analytics)**  
> University of Manouba | Academic Year 2024–2025  
> Author: **Rania Derouich**

---

## Overview

This project provides a comprehensive analysis of a **molecular dynamics (MD) simulation trajectory** using Python and the `pytraj` library. The analysis covers key structural and thermodynamic metrics used to assess the stability, flexibility, and conformational dynamics of a protein system.

---

## Analyses Performed

| Analysis | Metric | Description |
|---|---|---|
| **RMSD** | Root Mean Square Deviation | Global structural stability relative to initial frame |
| **RMSF** | Root Mean Square Fluctuation | Per-residue flexibility along the trajectory |
| **Radius of Gyration** | Rg | Compactness and folding state of the protein |
| **Inter-residue Distance** | Distance (Å) | Distance between first and last residues over time |
| **PCA** | Principal Component Analysis | Dominant conformational motions (Cα atoms) |
| **Thermodynamic Properties** | Temp, Volume, Pressure, Energy | System equilibration and stability |

---

## Repository Structure

```
molecular-dynamics-analysis/
├── README.md
├── .gitignore
├── requirements.txt
├── molecular_dynamics_analysis.ipynb      # Full MD analysis pipeline
├── molecular_dynamics_analysis_v2.ipynb   # Refined version
└── data/                                  # ← Place your input files here (not tracked by git)
    ├── brad_dry.nc                        # MD trajectory (AMBER NetCDF) — not included
    └── topology_dry.prmtop               # Topology file (AMBER) — not included
```

---

## Input Data

| File | Format | Description |
|---|---|---|
| `data/brad_dry.nc` | AMBER NetCDF | MD trajectory file |
| `data/topology_dry.prmtop` | AMBER | Topology file |

> **Note:** Raw trajectory and topology files are **not included** in this repository due to their large size. Place your own files in the `data/` folder before running the notebooks.

---

## Setup & Usage

```bash
git clone https://github.com/your-username/molecular-dynamics-analysis.git
cd molecular-dynamics-analysis
pip install -r requirements.txt
```

Create the `data/` folder and place your input files there:

```
data/
├── brad_dry.nc
└── topology_dry.prmtop
```

Then open a notebook and run all cells in order. The paths are already set to:

```python
trajectory_file = 'data/brad_dry.nc'
topology_file   = 'data/topology_dry.prmtop'
```

---

## Requirements

- Python ≥ 3.10
- pytraj ≥ 2.0
- numpy ≥ 1.24
- matplotlib ≥ 3.7

---

## Technologies

| Tool | Usage |
|---|---|
| pytraj | MD trajectory loading and analysis |
| NumPy | Numerical computing |
| Matplotlib | Visualization and plotting |
| AMBER format | Trajectory (`.nc`) & topology (`.prmtop`) input |

---

## Author

**Rania Derouich**  
Research Master's in Bioinformatics — Bio Data Analytics  
University of Manouba, Tunisia

> *Academic project — 2024/2025*
