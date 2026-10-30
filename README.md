# Low-Power Analysis of an 8-Bit PIPO Register Using Data-Driven Clock Gating

## Project Overview

This project investigates power reduction in an 8-bit Parallel-In Parallel-Out (PIPO) register using Data-Driven Clock Gating (DDCG).

Three architectures are considered:

1. Conventional 8-bit PIPO Register
2. Shared Data-Driven Clock Gating
3. Fixed 4-Bit Grouped Data-Driven Clock Gating

The main objective is to compare the power consumption of shared and grouped clock-gating architectures and study the effect of dividing a register into smaller groups.

## Architectures

### 1. Conventional PIPO Register
An 8-bit register consisting of eight D flip-flops connected to a common clock.

### 2. Shared DDCG
Eight XOR gates detect data changes. Their outputs are combined using a common OR reduction, which controls one clock-gating circuit.

### 3. Fixed 4-Bit Grouped DDCG
The register is divided into two independent 4-bit groups. Each group has its own change-detection reduction and clock-gating circuit.

## Experimental Results

| Architecture | Measured Power |
|---|---:|
| Shared DDCG | 188.336 mW |
| Fixed 4-Bit Grouped DDCG | 175.422 mW |

**Measured power difference:** 12.914 mW

**Relative power reduction:** 6.8569%

The percentage reduction is calculated relative to the shared DDCG architecture.

## Tools Used

- DSCH
- Microwind 3.0
- CMOS circuit simulation and layout analysis

## Repository Contents

- Circuit schematics
- DSCH implementation files
- Microwind layouts
- Power measurement screenshots
- Simulation waveforms
- Research paper and technical documentation

## Future Work

- Measure the conventional PIPO power baseline.
- Investigate four 2-bit groups and individual per-bit gating.
- Extend the study to 16-bit and 32-bit registers.
- Evaluate additional input switching patterns.

## References

The project is based on published research on data-driven clock gating, flip-flop grouping, and low-power VLSI design. Refer to the Research_Paper directory for the complete bibliography.

## Author

Sai Ram Ruttala

Department of Electronics and Communication Engineering  
IIIT Nagpur
