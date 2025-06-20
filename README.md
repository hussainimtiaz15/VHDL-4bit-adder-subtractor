# VHDL-4bit-adder-subtractor
A 4-bit adder/subtractor implemented in VHDL with a control signal for operation selection. Includes testbench, waveform analysis, and simulation using GHDL.

This project implements a 4-bit arithmetic module in VHDL that performs either addition or subtraction based on a control input. It includes a testbench with input stimulus and waveform validation using GHDL and GTKWave.

---

## 💡 Functionality

- Inputs:
  - `A` (4-bit)
  - `B` (4-bit)
  - `Op` (1-bit): Operation selector
    - `0` → Addition (A + B)
    - `1` → Subtraction (A - B)
- Output:
  - `Result` (4-bit)
  - `CarryOut` or `Borrow` flag (optional)

---

## 📁 Files Included

- `adder_subtractor.vhdl` – RTL module for 4-bit arithmetic
- `adder_sub_tb.vhdl` – Testbench with stimuli for both operations
- `waveform.png` – Simulation waveform output
- `README.md` – Project details and usage instructions

---

## ▶️ Simulation Instructions

Run using GHDL:

```bash
ghdl -a adder_subtractor.vhdl adder_sub_tb.vhdl
ghdl -e adder_sub_tb
ghdl -r adder_sub_tb --vcd=wave.vcd
gtkwave wave.vcd
