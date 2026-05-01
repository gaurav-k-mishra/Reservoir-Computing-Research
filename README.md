# Reservoir Computing Research

## Overview
This repository contains the numerical simulation code supporting the paper **"Weak-localization-induced temporal dynamics in disordered metals and implications for reservoir computing"** by Ashutosh Tiwari and Gaurav Mishra, Department of Materials Science and Engineering, University of Utah.

## What is this research about?
When electricity flows through a disordered piece of metal, electrons bounce around and create complex interference patterns. This paper proposes that those patterns can be harnessed as a **natural computing system** — no traditional processor needed. The metal itself does the computation.

This concept is called **Reservoir Computing**: instead of training a complex neural network, you use a physical system's natural dynamics as your "reservoir," and only train a simple output layer to read the results.

## My Contribution
The theoretical framework was developed by Prof. Ashutosh Tiwari. **My role was to build the numerical simulations that proved the theory works in practice.** This involved:

- Building the entire interference reservoir model from scratch in Python
- Running benchmark tests to validate computational performance
- Tuning key physics parameters to optimize the system
- Demonstrating that the simulated reservoir could accurately predict complex nonlinear sequences

## Repository Structure

**`reservoir_core.ipynb`** — The core simulation. Builds the interference reservoir, runs it through standard computational benchmarks (memory capacity and NARMA-10 sequence prediction), and produces the key results figures from the paper.

**`reservoir_NM_tuning.ipynb`** — Explores how reservoir size affects performance. Finds the minimum number of interference loops and probe electrodes needed before performance plateaus.

**`reservoir_alpha_tuning.ipynb`** — Tunes how strongly each interference loop responds to the input signal, optimizing sensitivity across the reservoir.

**`reservoir_tau_tuning.ipynb`** — Tunes the memory timescale of each loop, finding the optimal range for temporal information processing.

## Results
The simulations demonstrated that an ensemble of quantum interference trajectories can successfully perform temporal computing tasks, achieving a normalized mean squared error (NMSE) of ~0.15 on the NARMA-10 benchmark — validating the core theoretical claims of the paper.

## Dependencies
