# Parameterized FIFO Design and Verification Using SystemVerilog Assertions

## Overview

This project implements a **parameterized synchronous FIFO (First-In-First-Out)** using Verilog and verifies its functionality using a SystemVerilog-based verification environment.

The project focuses on both **RTL design** and **verification**, covering:

- Parameterized FIFO design
- Circular buffer implementation
- Full and empty detection
- Read and write pointer management
- Scoreboard-based verification
- SystemVerilog Assertions (SVA)
- Verification of invalid FIFO operations

The FIFO parameters can be modified to support different data widths and FIFO depths without changing the core RTL design.

---

## Features

- Parameterized data width
- Parameterized FIFO depth
- Synchronous read and write operations
- Circular buffer architecture
- Full and empty detection
- Separate read and write pointers
- Scoreboard-based data verification
- SystemVerilog Assertions
- Reset verification
- Protection against writing when FIFO is full
- Protection against reading when FIFO is empty
- Pointer stability verification

---

## FIFO Configuration

The default configuration used in this project is:

| Parameter | Value |
|-----------|-------|
| Data Width | 8 bits |
| FIFO Depth | 4 entries |
| Clock Period | 10 ns |

The FIFO can be instantiated with different configurations.

For example:

```verilog
fifo #(
    .DATA_WIDTH(16),
    .DEPTH(8)
) dut (
    ...
);
