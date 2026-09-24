# ALU-Digital-Systems

# FPGA Digital Design Project

![Intel Quartus](https://img.shields.io/badge/Intel_Quartus_Prime-0071C5?style=for-the-badge&logo=intel&logoColor=white)
![HDL](https://img.shields.io/badge/HDL-Verilog%20%2F%20VHDL-blue?style=for-the-badge)
![Target](https://img.shields.io/badge/Target-FPGA_Board-brightgreen?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge)

## 📌 Overview

This repository contains the full hardware design and implementation for **ALU-Digital-Systems**. The project is designed, compiled, synthesized, and analyzed using **Intel Quartus Prime** and deployed directly onto an **FPGA board** for real-time hardware validation.

> **Note:** Replace this text with a brief 2-3 sentence overview of what your specific digital system does (e.g., "This project implements a 32-bit ALU / Traffic Light Controller / VGA signal generator").

---

## ✨ Key Features

- **Hardware-level Optimization:** Fully synthesizable HDL code developed specifically for Intel/Altera FPGAs.
- **On-Board Verification:** Tested directly on hardware using physical switches, push buttons, LEDs, and 7-segment displays.
- **Structured Architecture:** Clean separation between RTL source files, testbenches, and Quartus synthesis/project files.
- **Timing & Resource Analysis:** Evaluated using the Quartus Compilation Report and Timing Analyzer.

---

## 🛠️ Tools & Hardware

| Category | Component / Tool |
| :--- | :--- |
| **EDA Tool** | Intel Quartus Prime (Lite / Standard Edition) |
| **Hardware Target**| FPGA Development Board (e.g., Cyclone IV, Cyclone V) |
| **HDL Language** | Verilog / SystemVerilog / VHDL |
| **Programming** | Quartus Programmer via USB-Blaster |

---

## 📁 Project Structure

```text
.
├── rtl/                  # Top-level and sub-module HDL source files (.v / .vhd)
├── tb/                   # Testbenches for simulation (.v / .vhd)
├── quartus/              # Quartus project files (.qpf, .qsf, output_files)
├── docs/                 # Schematics, state diagrams, and other documentation
└── README.md             # Project documentation
```

---

## 🚀 Getting Started

Follow these steps to compile the project and flash it onto your FPGA board.

### Prerequisites

1. Install **Intel Quartus Prime** (Version 18.1 or newer recommended).
2. Install the appropriate device family support package for your specific FPGA.
3. Connect your FPGA development board to your computer via **USB-Blaster**.

### Compilation & Flashing Workflow

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/your-username/your-repo-name.git](https://github.com/your-username/your-repo-name.git)
   cd your-repo-name
   ```

2. **Open the Project:**
   - Launch Intel Quartus Prime.
   - Go to `File > Open Project` and navigate to the `quartus/` directory to open the `.qpf` file.

3. **Compile the Design:**
   - Click **Start Compilation** (or press `Ctrl + L`) to perform Synthesis, Fitter (Place & Route), Assembler, and Timing Analysis.
   - Ensure there are no critical errors in the compilation report.

4. **Program the FPGA:**
   - Ensure your FPGA board is powered on and connected.
   - Open **Tools > Programmer**.
   - Click **Hardware Setup** and select your `USB-Blaster`.
   - Click **Auto Detect** or manually add the generated `.sof` file from the `quartus/output_files/` directory.
   - Check the "Program/Configure" box and click **Start** to flash the bitstream.

---

## 🔌 Hardware Pin Mapping

Below is the mapping of the top-level module ports to the physical FPGA pins:

| Signal Name | Direction | Hardware Component | FPGA Pin |
| :--- | :---: | :--- | :---: |
| `clk` | Input | 50 MHz On-Board Oscillator | `PIN_...` |
| `reset_n` | Input | Push Button (Active Low) | `PIN_...` |
| `sw[3:0]` | Input | Slide Switches | `PIN_...` |
| `ledr[3:0]` | Output | Red LEDs | `PIN_...` |

> *Note: Update the pin assignments table above according to your specific board's user manual or your Quartus `.qsf` file.*

---

## 📸 Results & Hardware Validation

* Images... *

---

## 🤝 Contributing

Contributions... 

---

## 📜 License

This project is distributed under the MIT License. See the `LICENSE` file for more information.
