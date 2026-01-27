# 30-60 GHz Wideband Vivaldi Antenna Design

This repository contains the design, modeling, and simulation results of a wideband Vivaldi antenna, developed using CST Studio Suite 2025. The design is optimized for mmWave (millimeter-wave) frequency bands, specifically targeting high-performance communication systems.

## Technical Overview
The antenna is designed on a substrate with a dielectric constant of 4.1 and a thickness of 0.2 mm. The design utilizes exponential tapering to achieve wideband impedance matching across the 30-60 GHz spectrum.

### Key Parameters
The design is fully parameterized to allow for easy optimization:
* **subw (Substrate Width):** 3 mm
* **sL (Slot Length):** 1 mm
* **h (Substrate Thickness):** 0.2 mm
* **k (Dielectric Constant):** 4.1
* **Frequency Range:** 30 GHz to 60 GHz

## Simulation Results
The simulation was performed using the Transient Solver in CST Studio Suite.

### S-Parameters (Return Loss)
The S1,1 results demonstrate:
* Strong impedance matching (below -10 dB) across the primary operating band.
* A significant resonance peak observed at approximately 48.7 GHz with a return loss better than -20 dB.
* Broadband characteristics suitable for 5G and radar applications.

![3D Model](media/3d_model.jpg)
![S-Parameter Plot](media/s_parameter_plot.jpg)

## Repository Structure
* `vivaldiantenna.cst`: The main project file (CST Studio Suite 2025).
* `/media`: Contains screenshots of the 3D model and S-parameter plots.
* `.gitignore`: Configured to exclude heavy simulation data (ModelCache, Result folders).

## How to Run
1. Clone the repository.
2. Open `vivaldiantenna.cst` with CST Studio Suite 2025 or later.
3. Run the Transient Solver to recalculate the results if necessary.
