# ADR_CBW
Artifacts of Delusions Research Team release of the Core Blocks Workflow suitable for all users, providing reliable and stable generative based diffusion images.
![1 1](https://github.com/user-attachments/assets/6d9d83c0-cdda-47c1-8bc2-df4759d9ca67)


**Artifacts of Delusions Research Team**

A stable, low-step diffusion workflow designed for reliable **one-shot image generation** with early semantic commitment and minimal variance.

This repository provides a **public reference implementation** of the Core Blocks Workflow, intended for broad community use, learning, and experimentation.

---

## Overview

ADR_CBW is a diffusion workflow built around the principle of **early basin lock**:
high-risk semantic decisions (subject identity, composition, style direction) are resolved early, with later stages restricted to refinement and polish only.

The workflow prioritizes:
- stability over novelty
- determinism over late correction
- low total step counts without sacrificing coherence

Typical results are achieved using **8–12 total steps across multiple samplers**, compared to traditional single-sampler workflows that often require 20–30+ steps.

---

## Key Characteristics

- **One-shot oriented**  
  Designed to converge cleanly in a single generation pass.

- **Multi-sampler structure**  
  Uses staged samplers for:
  - early structure commitment
  - controlled refinement
  - final polish only

- **Low compute cost**  
  Efficient enough for consumer GPUs while remaining stable on enterprise hardware.

- **Prompt hierarchy driven**  
  Structured positive conditioning enforces clarity instead of competition.

- **Public, auditable design**  
  No hidden steps, no black-box behavior.

---

## Prompt Hierarchy (Conceptual)

The workflow uses a **five-tier positive prompt structure**:

1. **Subject and Style**  
   Defines identity and core aesthetic.

2. **Quality / Style Stabilizer**  
   Enforces clarity, consistency, and readability.

3. **Main Subject and Composition**  
   Locks framing, pose, and spatial intent.

4. **Details and Subject Styling**  
   Adds controlled detail without altering structure.

5. **World and Vision Definition**  
   Establishes environment, mood, and context.

This hierarchy prevents late semantic drift and promotes calm diffusion behavior.

---

## Intended Use

This repository is intended as:

- a **daily-driver workflow** for fast, stable generations
- a **learning reference** for structured diffusion design
- a **baseline system** that can be extended or studied

It is **not** intended to represent the full internal research systems of the Artifacts of Delusions Research Team.

---

## What This Is *Not*

- Not a maximum-detail photorealism pipeline
- Not a prompt-roulette system
- Not an all-in-one enterprise solution

This workflow intentionally favors **clarity, reproducibility, and restraint**.

---

## License

This project is released under the **GNU General Public License v3.0 (GPL-3.0)**.

You are free to:
- use the workflow
- modify it
- redistribute it

Under the condition that:
- derivative works remain open
- modifications are disclosed when redistributed
- the same license is preserved

See the `LICENSE` file for full details.

---

## Acknowledgements

This release is provided by the **Artifacts of Delusions Research Team**,  
a small independent research group exploring the stability and behavior of diffusion-based generative systems.

---

## Status

**Public reference release — v1**

Future updates may include:
- documentation refinements
- example expansions
- optional variants

No guarantees are made regarding backward compatibility.

---

*Released in the spirit of shared learning and responsible openness.*
