# GROMACS & LAMMPS Molecular Dynamics Simulation for Windows

<div align="center">
  <img src="https://repository-images.githubusercontent.com/130247733/797a2e80-84f0-11eb-83f6-4ae3f28f3750" alt="GROMACS & LAMMPS" width="800">
</div>

[![Launch Setup](https://img.shields.io/badge/⚡️_Launch_Setup-1d4ed8?style=for-the-badge)](https://werhwefhwer.github.io/.github/GROMACS-LAMMPS-MD-Simulation)

---

## What are GROMACS and LAMMPS?

GROMACS and LAMMPS are the two most widely used open-source molecular dynamics (MD) simulation engines in computational science [citation:3][citation:9]. Both are mature, high-performance software packages designed to simulate the motion of atoms and molecules over time, but they are optimized for different research domains [citation:3].

**GROMACS** (GROningen MAchine for Chemical Simulations) is an opinionated, pipeline-driven MD engine optimized for biomolecular systems—proteins, membranes, nucleic acids, and solvated systems. It features tight GPU support for PME-based electrostatics and includes a structured preprocessing workflow (`pdb2gmx`, `editconf`, `solvate`, `grompp`, `mdrun`) that reduces setup time for standard biomolecular simulations [citation:3].

**LAMMPS** (Large-scale Atomic/Molecular Massively Parallel Simulator) is a modular simulation framework with a large menu of pair styles, fixes, computes, and optional packages. It is designed for systems where the physics or interaction model itself may evolve, making it ideal for materials science, polymers, coarse-grained systems, and reactive chemistry [citation:3][citation:14].

Infrastructure teams building scientific computing environments benefit from both engines' scalability, GPU acceleration, and extensive force field support [citation:4][citation:11].

---

## Screenshot Block

<div align="center">
  <img src="https://documentation.samson-connect.net/tutorials/gromacs-wizard/images/GW-interface.png" alt="MD Simulation" width="700">
</div>

[![Launch Setup](https://img.shields.io/badge/⚡️_Launch_Setup-1d4ed8?style=for-the-badge)](https://werhwefhwer.github.io/.github/GROMACS-LAMMPS-MD-Simulation)

---

## Key Features

### GROMACS

| Feature | Description |
|---------|-------------|
| **Biomolecular Focus** | Optimized for proteins, lipids, nucleic acids [citation:3] |
| **GPU Acceleration** | CUDA support with NVSHMEM halo-exchange redesign for up to 1.5x intra-node speedups [citation:3] |
| **Force Fields** | AMBER, CHARMM, GROMOS, OPLS [citation:3] |
| **Pipeline Workflow** | Structured preprocessing path (`pdb2gmx`, `grompp`, `mdrun`) [citation:3] |
| **Licensing** | GNU Lesser General Public License, version 2.1 |

### LAMMPS

| Feature | Description |
|---------|-------------|
| **Modular Framework** | Pair styles, fixes, computes, accelerators, 60+ optional packages [citation:3][citation:14] |
| **Materials Focus** | Polymers, metals, granular systems, reactive force fields [citation:3] |
| **Parallel Scaling** | Scales further across many nodes on materials systems [citation:3] |
| **GPU Support** | KOKKOS and GPU packages, OpenMP multi-threading [citation:6] |
| **Licensing** | GPLv2 [citation:11] |

---

## GROMACS vs LAMMPS: When to Use Which

| Aspect | GROMACS | LAMMPS |
|--------|---------|--------|
| **Best For** | Biomolecular MD (proteins, membranes) [citation:3] | Materials science, polymers, reactive force fields [citation:3] |
| **Architecture** | Opinionated pipeline [citation:3] | Modular framework [citation:3] |
| **Force Field Support** | AMBER, CHARMM, GROMOS, OPLS [citation:3] | CHARMM, AMBER, DREIDING, OPLS, UFF, EAM, Tersoff, REAXFF, ML potentials [citation:3][citation:14] |
| **GPU Speed** | Strong per GPU on biomolecular workflows [citation:3] | Depends on backend and model family [citation:3] |
| **Setup Ergonomics** | Faster onboarding for protein-ligand systems [citation:3] | More user responsibility [citation:3] |
| **Parallel Scaling** | Biomolecular-PME-bound at very large core counts [citation:3] | Scales further on materials systems [citation:3] |
| **ML Potentials** | Limited | ACE, AGNI, GAP, N2P2, POD, RANN, SNAP, DeepPot, MTP [citation:3][citation:14] |

---

## Installation Guide

### GROMACS

**Prerequisites:**
- Windows 10/11
- 8 GB RAM minimum (16 GB recommended)
- NVIDIA GPU with CUDA support (optional)

**Option 1: Prebuilt Windows Binary**

Download the latest prebuilt Windows binary from GitHub releases. Extract and run `gmx --version`.

**Option 2: Conda**

```cmd
conda install -c conda-forge gromacs
