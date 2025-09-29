# FPGA Matrix Multiplication Accelerator

This project implements **matrix multiplication in hardware** using Verilog, progressively optimizing performance across multiple architectures on an FPGA:

- **Single-MAC design** – Baseline implementation using one Multiply-Accumulate (MAC) unit to compute an 8×8 matrix product sequentially. (~640 cycles)
- **Dual-MAC design** – Adds parallelism with two MAC units and dual-port memory, halving computation time. (~387 cycles)
- **Optimized design** – Scales up with 8 MACs and a cache-fed architecture, cutting execution down to **~89 cycles**.

Key techniques:
- Custom MAC units for signed arithmetic.
- Dual-port RAM for parallel memory access.
- Finite State Machines (FSMs) to orchestrate load/compute/write stages.
- Throughput gains via parallelism and pipelining.

**Results:** Efficient use of embedded multipliers and memory, verified through ModelSim simulation, Quartus synthesis, and FPGA resource utilization reports.
