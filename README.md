# 32-bit Array Multiplier – Cadence Virtuoso

## Overview

This project implements a **32-bit Array Multiplier** using **Half Adders (HA)** and **Full Adders (FA)** and was designed and simulated using **Cadence Virtuoso**.

The design follows a structured array-multiplier architecture in which partial products are generated and accumulated using cascaded Half Adder and Full Adder stages.

The project focuses on understanding the design, hierarchical construction, and functional verification of a digital multiplier at the circuit level.

---

## Objectives

- Design a Half Adder at the circuit level.
- Design a Full Adder using basic logic circuitry.
- Use Half Adders and Full Adders to construct an Array Multiplier.
- Implement the design using Cadence Virtuoso.
- Verify the functionality through simulation.
- Analyze the generated simulation waveforms.

---

## Design Architecture

The multiplier is constructed hierarchically using:

```text
              ┌─────────────────────┐
              │     Input A         │
              └──────────┬──────────┘
                         │
                         ▼
                Partial Product
                   Generation
                         │
                         ▼
              ┌─────────────────────┐
              │                     │
              │   HA / FA Array     │
              │                     │
              │  Partial Product    │
              │    Accumulation     │
              │                     │
              └──────────┬──────────┘
                         │
                         ▼
              ┌─────────────────────┐
              │   Multiplier Output │
              └─────────────────────┘
```

The basic building blocks are:

```text
Half Adder
     │
     ▼
Full Adder
     │
     ▼
Array Multiplier
```

---

## Design Hierarchy

The project is organized into three major design levels:

### 1. Half Adder

The Half Adder forms one of the fundamental building blocks of the multiplier.

It performs binary addition of two input bits and produces:

- Sum
- Carry

The Half Adder schematic and its simulation result are included in the repository.

---

### 2. Full Adder

The Full Adder is used for adding partial products while considering an input carry.

It produces:

- Sum
- Carry

The Full Adder was designed and simulated in Cadence Virtuoso before being used as a building block for the multiplier.

---

### 3. Array Multiplier

The Array Multiplier combines multiple partial-product generation and addition stages.

The Half Adders and Full Adders are arranged systematically to accumulate the generated partial products and produce the multiplication result.

The complete multiplier schematic is included in the `schematics/` directory.

---

## Simulation and Verification

Functional verification was performed using **Cadence Virtuoso simulation**.

Simulation results are provided for:

- Half Adder
- Full Adder
- Array Multiplier

The multiplier simulation waveforms are included in the `simulations/` directory.

These simulations were used to verify the expected behavior of the individual building blocks and the complete multiplier.

---

## Repository Structure

```text
32-bit-Array-Multiplier-Cadence/
│
├── design/
│   ├── full_adder/
│   ├── half_adder/
│   └── multiplier/
│
├── schematics/
│   ├── full_adder.jpeg
│   ├── half_adder.jpeg
│   ├── multiplier_image.png
│   ├── multiplier_image2.png
│   └── multiplier_image3.png
│
└── simulations/
    ├── full_adder.jpeg
    ├── half_adder.jpeg
    ├── multiplier_cont_waveform.jpeg
    └── multiplier_waveform.jpeg
```

---

## Tools Used

- Cadence Virtuoso
- Schematic Editor
- Cadence Simulation Environment
- Analog/Digital Circuit Design

---

## Key Concepts Demonstrated

- Digital arithmetic circuits
- Half Adder design
- Full Adder design
- Partial-product generation
- Array multiplier architecture
- Hierarchical circuit design
- Schematic capture
- Functional simulation
- Waveform analysis
- Cadence Virtuoso workflow

---

## Project Outcomes

Through this project, I gained practical experience in:

- Building digital arithmetic circuits hierarchically.
- Designing and verifying Half Adder and Full Adder circuits.
- Combining basic arithmetic blocks into a larger multiplier architecture.
- Using Cadence Virtuoso for circuit schematic design.
- Running simulations and analyzing waveforms.
- Understanding the relationship between individual circuit blocks and a complete digital datapath.

---

## Future Work

Possible extensions of this project include:

- Transistor-level optimization.
- Power and delay analysis.
- Area analysis.
- PVT/corner analysis.
- Layout implementation.
- Design Rule Check (DRC).
- Layout Versus Schematic (LVS).
- Parasitic extraction and post-layout simulation.
- Comparison with other multiplier architectures.

---

## Author

**Sudeep T. Gotur**

Electronics and Communication Engineering
