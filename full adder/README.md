# Full Adder using Verilog

## Overview

This project implements a **1-bit Full Adder** using Verilog HDL.

A Full Adder is a combinational logic circuit that adds three binary inputs:
- A
- B
- Cin (Carry Input)

It produces two outputs:
- Sum
- Cout (Carry Output)

---

## Truth Table

| A | B | Cin | Sum | Cout |
|---|---|-----|-----|------|
| 0 | 0 | 0 | 0 | 0 |
| 0 | 0 | 1 | 1 | 0 |
| 0 | 1 | 0 | 1 | 0 |
| 0 | 1 | 1 | 0 | 1 |
| 1 | 0 | 0 | 1 | 0 |
| 1 | 0 | 1 | 0 | 1 |
| 1 | 1 | 0 | 0 | 1 |
| 1 | 1 | 1 | 1 | 1 |

---

## Logic Equations

**Sum**

```
Sum = A ^ B ^ Cin
```

**Carry**

```
Cout = (A & B) | (B & Cin) | (A & Cin)
```

---

## Files

| File | Description |
|------|-------------|
| full_adder.v | Verilog design |
| full_adder_tb.v | Testbench |
| simulation.png | Simulation waveform |
| README.md | Project documentation |

---

## Simulation

Compile

```bash
iverilog -o fulladder full_adder.v full_adder_tb.v
```

Run

```bash
vvp fulladder
```

Open Waveform

```bash
gtkwave fulladder.vcd
```

---

## Expected Output

The simulation verifies all possible input combinations of the Full Adder.

---

## Author

Your Name
