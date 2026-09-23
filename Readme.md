# 3.3V Linear Power Delivery Module

## Overview
This repository contains the KiCad design files for a custom 5V to 3.3V power delivery network. Built around the AMS1117-3.3 Low-Dropout (LDO) regulator, this module is designed to provide stable, filtered power for mixed-signal microcontrollers by implementing both high-frequency and bulk decoupling strategies. 

## Visuals
<img width="1723" height="921" alt="5V to 3 3V LDO" src="https://github.com/user-attachments/assets/66e9589f-a955-478e-82c4-5592d5b3d65c" />
<br>
<img width="1548" height="824" alt="image" src="https://github.com/user-attachments/assets/4257f85b-7969-4c97-af3f-d91f6fa15fa2" />

*(Note: Ensure image files are uploaded to the root of the repository so these links render correctly)*

## Design Highlights
* **Dual-Stage Decoupling:** Utilizes a 100µF bulk capacitor for instantaneous current spikes and a 0.1µF bypass capacitor for high-frequency noise filtration on both the input and output rails.
* **Thermal Management:** The LDO tab is coupled to a solid copper ground plane on the PCB to act as a thermal heatsink during high-current draw.
* **Trace Routing:** Calculated trace widths used for the +5V and 3V3 nets to safely handle required current without excessive voltage drop.

## Bill of Materials (BOM)

| Ref | Qty | Component Details | Package | Source Link |
| :--- | :---: | :--- | :--- | :--- |
| **C1, C3** | 2 | 0.1µF, 50V MLCC (KEMET C0805C104K5RAC7210) | SMD 0805 | [Robu.in](https://robu.in/product/c0805c104k5rac7210-kemet-cap-smd-mlcc-0-1-%C2%B5f-50-v-0805-pack-of-1/) |
| **C2, C4** | 2 | 100µF, 6.3V MLCC (MURATA 21BR60J107ME15K) | SMD 0805 | [Robu.in](https://robu.in/product/21br60j107me15k-murata-cap-smd-mlcc-100%C2%B5f-6-3-v-0805-pack-of-1/) |
| **D1** | 1 | 5mm Red DIP LED | THT 5.0mm | [Robu.in](https://robu.in/product/5mm-red-dip-led-pack-of-50/) |
| **J1, J2** | 2 | 2.54mm Pitch Male Header (Breakable) | THT 2.54mm | [Robu.in](https://robu.in/product/pcb-male-header-40-pin-kit-6-colours-5pcs-each/) |
| **R1** | 1 | 68Ω, 125mW Resistor (Yageo RC0805JR-0768RL) | SMD 0805 | [Robu.in](https://robu.in/product/rc0805jr-0768rl-yageo-smd-chip-resistor-68-ohm-%25c2%25b1-5-125-mw-0805-2012-metric-thick-film-general-purpose/) |
| **U1** | 1 | AMS1117-3.3V 1A LDO Voltage Regulator | SMD SOT-223 | [Robu.in](https://robu.in/product/ams1117-3-3v-1a-sot-223-voltage-regulator-ic-pack-of-5-ics/) |

## Fabrication Specs
* **Layers:** 2 (Front Cu, Back Cu)
* **Design Rule Check (DRC):** 0 Violations
* **EDA Tool:** KiCad 10.0
