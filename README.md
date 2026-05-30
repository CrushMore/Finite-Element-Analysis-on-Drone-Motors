# Finite-Element-Analysis-on-Drone-Motors
FEA modal analysis of a high-performance drone motor arm using Ansys Mechanical to prevent structural resonance failure
# Modal Analysis of a High-Performance Drone Motor Arm

## Project Overview
This repository contains a Finite Element Analysis (FEA) project focused on validating the structural integrity and dynamic safety of a proposed drone motor arm design. Using **Ansys Mechanical Workbench 2025 R2**, a modal analysis was performed to determine the component's natural frequencies and guarantee safe operations free from catastrophic resonance failure under dynamic loads.

## Problem Statement & Objective
High-speed drone motors generate forced mechanical vibrations during operation. If the motor's operating excitation frequency matches any of the natural frequencies of the structural arm, it causes **resonance**, leading to infinite displacement amplification and structural failure. 

* **Operating Parameters:** Maximum motor speed of 12,000 RPM (Excitation Frequency: 200 Hz).
* **Danger Zone (Safety Margin):** 180 Hz to 220 Hz ($\pm10\%$).
* **Objective:** Extract the first 6 natural mode shapes and frequencies of the cantilevered arm to verify that none fall within the designated danger zone.

## Simulation Methodology & Boundary Conditions
* **Geometry:** Hollow square tube profile (Length: 200 mm, Cross-section: 15 mm x 15 mm, Thickness: 2 mm).
* **Material:** Aluminum Alloy (Standard Ansys Library Material).
* **Meshing:** High-quality fine mesh optimized for vibration analysis with a 2 mm element size, yielding 19,740 nodes and 2,800 elements.
* **Boundary Conditions:** * Fixed support applied to the base face (simulating attachment to the drone body).
  * A point mass of 0.5 kg applied to the tip face to accurately simulate motor weight, inertia, and gravity effects without adding mesh complexity.

## Key Simulation Results
The first 6 natural frequencies were successfully extracted via Ansys:

| Mode Shape | Natural Frequency (Hz) | Status / Evaluation |
| :---: | :---: | :--- |
| **Mode 1** | 72.081 Hz | Safe (Passes through resonance briefly only during motor spin-up) |
| **Mode 2** | 72.330 Hz | Safe (Passes through resonance briefly only during motor spin-up) |
| **Mode 3** | 2010.2 Hz | Safe (Extremely far above operating frequency; zero risk of excitation) |
| **Mode 4** | 2185.7 Hz | Safe |
| **Mode 5** | 2408.7 Hz | Safe |
| **Mode 6** | 2643.9 Hz | Safe |

## Conclusion
**DESIGN PASS:** The structural natural frequencies completely avoid the 180–220 Hz operational danger zone at the top speed of 12,000 RPM. The analysis confirms that the cantilevered square tube geometry provides exceptional structural safety and dynamic stability under maximum structural operations.
