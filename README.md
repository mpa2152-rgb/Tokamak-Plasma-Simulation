# Tokamak Vertical Stability Simulation

A Python simulation modeling the vertical stability of a SPARC-like tokamak plasma equilibrium, built using the TokaMaker package.

## What it does

This project simulates plasma equilibrium in a tokamak reactor based on MIT's SPARC design parameters, and analyzes how vertically stable the configuration is when plasma is introduced. High-elongation tokamaks like SPARC are inherently vertically unstable, so quantifying and visualizing this instability (a Vertical Displacement Event, or VDE) is a key part of reactor control design.

The simulation:
- Computes a vertical stability metric (growth rate) for the plasma equilibrium
- Plots VDE equilibrium snapshots over time, showing how the plasma boundary shifts as it becomes unstable
- Generates an animation visualizing plasma displacement over the course of a VDE

## Background

Built as part of a research project during a school program, using design parameters from MIT's SPARC tokamak:

| Quantity | Symbol | Value |
|---|---|---|
| Toroidal magnetic field | B_T | 12.2 T |
| Major radius | R0 | 1.85 m |
| Minor radius | a | 0.57 m |
| Elongation | κ | 1.97 |
| Triangularity | δ | 0.54 |
| Internal inductance | li | 0.85 |
| Poloidal beta | βp | 100% |

## Tech stack

- Python (Google Colab)
- [TokaMaker](https://github.com/hansec/OpenFUSIONToolkit) — plasma equilibrium solver
- NumPy
- Matplotlib

## How to run it

This notebook was developed in Google Colab. To run it:

1. Open the `.ipynb` file in [Google Colab](https://colab.research.google.com/) or Jupyter.
2. Install dependencies:
```bash
   pip install numpy matplotlib
   # + TokaMaker install instructions, if applicable
```
3. Run all cells. The notebook will generate the stability metric output, VDE snapshot plots, and the displacement animation.

## Results / Features

- Quantifies vertical instability growth rate for a SPARC-scale equilibrium
- Visualizes VDE progression through sequential equilibrium snapshots
- Animated plasma displacement over time

![VDE simulation animation](assets/2026-05-05_matthew_vde (1).gif)!



## What I'd improve

- Add configurable parameters to test other tokamak geometries beyond SPARC
- Compare growth rates against published SPARC stability studies
