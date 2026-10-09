# Power Electronics Lab: AC Rectifiers & DC–DC Converter Simulations
### MATLAB/Simulink Circuit Simulations — Single-Phase & 3-Phase Rectifiers, Buck-Boost Converters

**Course:** ENE312 – Power Electronics  
**Instructor:** Eng. Anas Alswaeer  
**Department:** Department of Energy Engineering, School of Applied Technical Sciences  
**Institution:** German Jordanian University (GJU)

---

## Overview

This repository contains the MATLAB/Simulink circuit simulation models and pre-lab analytical reports completed for **ENE312: Power Electronics**.

The lab work covers the full progression of power conversion circuits:

- **Uncontrolled AC–DC rectification** — half-wave and full-wave topologies, single-phase and 3-phase
- **Controlled AC–DC rectification** — thyristor (SCR) phase-control for single-phase and 3-phase bridges
- **DC–DC switching conversion** — Buck and Buck-Boost converter topologies

---

## Lab Modules

### Lab 1 — Single-Phase Uncontrolled Rectifiers
**Simulation:** `simulations/Single_Phase_Full_Wave.slx`  
**Report:** `docs/PreLab1_Single_Phase_Uncontrolled_Rectifier.pdf`

- Full-wave bridge rectifier (4-diode) and center-tapped full-wave rectifier configurations.
- Analysis of DC output voltage, ripple voltage, and diode current waveforms.
- Effect of resistive and resistive-inductive (R-L) loads on output waveform shape.

**Key relationship:**
$$V_{dc} = \frac{2V_m}{\pi}$$

---

### Lab 2 — 3-Phase Uncontrolled Rectifiers
**Simulation:** `simulations/Half_Wave_3_Phase.slx`, `simulations/Three_Phase_Full_Wave.slx`  
**Report:** `docs/PreLab2_Three_Phase_Uncontrolled_Rectifiers.pdf`

- Half-wave 3-phase rectifier (3-pulse) and full-wave 3-phase bridge (6-pulse) topologies.
- Observation of reduced output ripple compared to single-phase counterparts.
- Phase voltage and line voltage relationships and their effect on rectified output.

**Key relationship (6-pulse bridge):**
$$V_{dc} = \frac{3\sqrt{3}}{\pi} V_m$$

---

### Lab 3 — Controlled Single-Phase Rectifier
**Simulation:** `simulations/Controlled_Single_Phase.slx`  
**Report:** `docs/PreLab3_Controlled_Single_Phase_Rectifier.pdf`

- SCR (thyristor) phase-controlled full-wave bridge rectifier.
- Firing angle $\alpha$ control to vary the average DC output voltage.
- Waveform analysis for resistive and inductive loads, including freewheeling diode effect.

**Key relationship:**
$$V_{dc} = \frac{2V_m}{\pi}\cos\alpha$$

---

### Lab 4 — Controlled 3-Phase Rectifier
**Simulation:** `simulations/Three_Phase_Controlled.slx`  
**Report:** `docs/PreLab4_Controlled_Three_Phase_Rectifier.pdf`

- 3-phase fully controlled thyristor bridge (6-pulse) with variable firing angle $\alpha$.
- Output voltage control range and transition between rectifier and inverter modes.
- Impact of firing angle on DC voltage and harmonic content.

**Key relationship:**
$$V_{dc} = \frac{3\sqrt{3}}{\pi} V_m \cos\alpha$$

---

### Lab 5 — DC–DC Buck-Boost Converter
**Simulation:** `simulations/Buck_Converter.slx`  
**Report:** `docs/PreLab5_Buck_Boost_DC_DC_Converter.pdf`

- Buck converter: step-down switching converter with MOSFET switch, inductor, and freewheeling diode.
- Buck-Boost converter: combined topology capable of output voltage above or below input.
- Steady-state analysis: duty cycle $D$ control, inductor current ripple, and output voltage ripple.
- Continuous Conduction Mode (CCM) vs. Discontinuous Conduction Mode (DCM) boundary conditions.

**Key relationships:**
$$V_{out,Buck} = D \cdot V_{in}, \quad V_{out,BuckBoost} = \frac{D}{1-D} V_{in}$$

---

## Repository Structure

```text
├── simulations/
│   ├── Single_Phase_Full_Wave.slx          # Single-phase uncontrolled bridge rectifier
│   ├── Full_Wave_Center_Tapped.slx         # Center-tapped full-wave rectifier
│   ├── Controlled_Single_Phase.slx         # SCR-controlled single-phase rectifier
│   ├── Half_Wave_3_Phase.slx               # 3-phase half-wave (3-pulse) rectifier
│   ├── Three_Phase_Full_Wave.slx           # 3-phase full-wave (6-pulse) rectifier
│   ├── Three_Phase_Controlled.slx          # 3-phase controlled thyristor bridge
│   └── Buck_Converter.slx                  # DC-DC Buck converter simulation
├── docs/
│   ├── PreLab1_Single_Phase_Uncontrolled_Rectifier.pdf
│   ├── PreLab2_Three_Phase_Uncontrolled_Rectifiers.pdf
│   ├── PreLab3_Controlled_Single_Phase_Rectifier.pdf
│   ├── PreLab4_Controlled_Three_Phase_Rectifier.pdf
│   └── PreLab5_Buck_Boost_DC_DC_Converter.pdf
├── .gitignore
└── README.md
```

---

## How to Open the Simulations

1. Open MATLAB (R2021a or later recommended).
2. Navigate to the `simulations/` directory.
3. Open any `.slx` file — the Simulink model will load.
4. Press **Run** to execute the simulation and view scope outputs.

> **Note:** The Simscape / SimPowerSystems (Electrical) toolbox is required to run the power circuit models.

## GitHub Preview

GitHub can display the laboratory PDFs, but it cannot run or render Simulink `.slx` models in the browser. Download a model and open it locally in MATLAB/Simulink to inspect the block diagram and reproduce the waveforms.
