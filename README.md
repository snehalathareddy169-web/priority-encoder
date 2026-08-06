# 4-to-2 Priority Encoder using Verilog

## Overview

This project implements a **4-to-2 Priority Encoder** in Verilog HDL. A priority encoder outputs the binary code of the highest-priority active input. In this implementation, **I3** has the highest priority and **I0** has the lowest.

## Priority Table

| Inputs | Output (Y) | Valid |
|--------|------------|-------|
|1xxx|11|1|
|01xx|10|1|
|001x|01|1|
|0001|00|1|
|0000|00|0|

## Inputs

- `I[3:0]` – Four input lines

## Outputs

- `Y[1:0]` – Binary code of the highest-priority active input
- `Valid` – Indicates whether any input is active

## Project Structure

```
priority-encoder-verilog/
├── src/
├── tb/
├── sim/
├── images/
└── README.md
```

## Simulation

Compile:

```bash
iverilog -o encoder src/priority_encoder.v tb/priority_encoder_tb.v
```

Run:

```bash
vvp encoder
```

Open the waveform:

```bash
gtkwave priority_encoder.vcd
```

## Applications

- Interrupt controllers
- Keyboard encoding
- Request arbitration
- Digital communication systems
- FPGA and ASIC designs

## License

MIT License