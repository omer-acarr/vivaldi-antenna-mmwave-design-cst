# 30-60 GHz Ultra-Wideband Vivaldi Antenna: From Simulation to PCB Manufacturing

This repository contains the full design cycle of an ultra-wideband (UWB) Vivaldi antenna, covering **CST Studio Suite 2025** simulations and **Altium Designer** PCB layout/manufacturing files. The design is optimized for millimeter-wave (mmWave) applications, specifically targeting the Ka and V bands.

## 🚀 Project Overview
Vivaldi antennas (Tapered Slot Antennas) are known for their high gain and stable radiation patterns. This project bridges the gap between electromagnetic simulation and physical realization by providing production-ready Gerber files on specialized high-frequency substrates.

### Technical Specifications
* **Frequency Range:** 30 GHz - 60 GHz
* **Substrate:** Taconic RF-60A (lossy)
    * **Permittivity ($\epsilon_r$):** 6.15
    * **Loss Tangent ($\tan \delta$):** 0.0028
    * **Thickness:** 0.2 mm
* **Feed Mechanism:** Microstrip line transition to an exponential taper.

---

## 📊 Phase 1: Simulation (CST Studio Suite)
The antenna geometry was parameterized and optimized for maximum bandwidth and impedance matching.

* **S-Parameters ($S_{11}$):** Achieved excellent matching below -10 dB across the entire 30-60 GHz band, with resonance points near 32 GHz and 48 GHz.
* **Mesh Optimization:** Configured with ~13,440 cells to balance simulation accuracy and computational speed.

---

## 🛠 Phase 2: PCB Layout & Manufacturing (Altium Designer)
The CST model was exported via DXF and reconstructed in Altium Designer to ensure a production-ready design.

### Key Layout Features
* **Dual-Layer Structure:**
    * **Top Layer:** 0.25 mm microstrip feed line with a dedicated 0.3mm x 0.5mm soldering pad for mmWave connectors.
    * **Bottom Layer:** Exponentially tapered Vivaldi wings acting as the ground plane and radiator.
* **Precision Alignment:** The microstrip-to-slotline transition was cross-verified in 3D to ensure perfect electromagnetic coupling at 60 GHz.
* **Board Shape:** Optimized 12mm x 9mm form factor defined on the Mechanical layer for precise CNC routing.



### Manufacturing Package
The repository includes a complete production folder containing:
* **Gerber Files (RS-274X):** Top/Bottom copper, Solder Mask, and Board Outline.
* **NC Drill Files:** Precise board cutout coordinates.
* **Fabrication Notes:** Specifications for **Taconic RF-60A**, **0.2 mm thickness**, and **ENIG (Immersion Gold)** surface finish.

