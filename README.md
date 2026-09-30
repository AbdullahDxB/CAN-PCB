<h1 align="center">CAN Bus MCP2518 Transceiver Node</h1>

<p align="center">
  <b>High-Integrity Industrial Communication Board</b><br>

</p>

<p align="center">
  <img src="https://img.shields.io/badge/KiCAD_9.0-314CB6?style=for-the-badge&logo=kicad&logoColor=white" alt="KiCAD"/>
  <img src="https://img.shields.io/badge/CAN_Bus-00599C?style=for-the-badge&logo=can&logoColor=white" alt="CAN Bus"/>
  <img src="https://img.shields.io/badge/PCB_Design-A59B6A?style=for-the-badge&logo=pcb&logoColor=white" alt="PCB Design"/>
</p>

<div align="center">
  
  **[View the 3D Board Render](./docs/3DVIEW.png)** &nbsp;&nbsp;•&nbsp;&nbsp; **[View Complete Schematic (PDF)](./docs/Schematic.pdf)**

</div>

---

## 🎯 Project Overview

A robust, two-layer CAN bus transceiver node designed for high-noise industrial environments. Built around the **MCP2518**, this board facilitates reliable, high-speed differential communication. The project demonstrates a strict adherence to layout guidelines, differential pair routing, and rigorous design rule checking (DRC).

## 🛠️ Hardware & Design Stack

* **Transceiver IC:** MCP2518
* **Protocol:** Controller Area Network (CAN)
* **EDA Tool:** KiCAD 9.0 (Schematic Capture, PCB Layout, 3D Rendering)
* **Manufacturing Prep:** Gerber Generation, BOM Management

---

## ⚙️ Design Challenges & Hardware Architecture

1. **Custom Footprint Engineering:** Discovered a critical discrepancy between the default KiCAD footprint library and the manufacturer's datasheet for the transceiver IC. To prevent solder bridging and assembly failure, I manually cross-referenced the physical dimensions and designed a custom footprint from scratch, validating pad spacing against strict DRC parameters.
2. **Differential Pair Routing:** CAN High (CANH) and CAN Low (CANL) traces were strictly routed as differential pairs, ensuring matched impedance and minimizing electromagnetic interference (EMI) in noisy industrial settings.
3. **Design Validation:** Zero errors on both the Electrical Rules Check (ERC) and Design Rules Check (DRC) prior to generating final production files.

---

## 📂 Repository Structure

* **[`hardware/`](./hardware):** Core KiCAD 9.0 project files (`.kicad_sch`, `.kicad_pcb`, `.kicad_pro`).
* **[`docs/`](./docs):** High-resolution schematic PDFs, top/bottom layer copper exports, 3D board renders, and DRC/ERC reports.
* **[`manufacturing/`](./manufacturing):** Generated Bill of Materials (BOM) and production-ready Gerber files.
* **[`datasheets/`](./datasheets):** Component reference documentation.

---
*Created by Abdullah Ajmal - August 2026*
