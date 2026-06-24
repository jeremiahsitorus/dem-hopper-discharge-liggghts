# DEM Hopper Discharge Simulation

Discrete Element Method (DEM) simulation of bulk material (gravel) flow through a hopper with rotary valve, conducted as part of the *Discrete Element Method* course at Otto-von-Guericke-Universität Magdeburg.

**Solver:** LIGGGHTS (open-source DEM based on LAMMPS)

---

## Problem Description

A hopper system is fed by a conveyor belt delivering gravel at 55 kg/s. After the hopper reaches ~190 kg filling mass, a rotary valve at the outlet 
opens and discharges the material. The simulation investigates:
- Flow regime characterization (mass flow vs. funnel flow)
- Dead zone identification and quantification
- Particle segregation during filling
- Rotary valve performance: mass flow rate, resistance torque, impact forces

## Simulation Setup

| Parameter | Value |
|---|---|
| Solver | LIGGGHTS |
| Contact model | Hertz-Mindlin |
| Particle material | Gravel (ρ = 3200 kg/m³) |
| Particle radius | 5.0 – 11.0 mm (6 fractions) |
| Young's modulus | 1×10⁷ Pa |
| Wall friction (steel-bulk) | 0.5 |
| Rolling friction | 0.8 |
| Inlet mass flow rate | 55 kg/s |
| Filling mass | ~190 kg |
| Rotary valve speed | 20 rpm |
| Hopper half angle α | 45° |
| Inlet inclination β | 10° |

---

## Repository Structure
├── hopper_discharge.lmp       # Main LIGGGHTS input script

├── hopper_excl                

├── funnel1.stl

├── funnel2.stl

├── hopper_open.stl

├── inlet_planar.stl

├── outlet_planar.stl

├── rotary_planar.stl

│── rotor.stl

├── measurements/              # Extracted simulation data

└── ss/                   # Plots and screenshots

---

## Key Results
**Mass Flow Rate of the Rotary Valve**
<img width="3840" height="2160" alt="massflow" src="https://github.com/user-attachments/assets/c7ac1282-e522-43d7-ace9-0502bf66fbc9" />

**Resistance Torque and Torque Course**
<img width="3840" height="2160" alt="torque" src="https://github.com/user-attachments/assets/464137ad-0c53-42db-a982-ec22b5b2a675" />
