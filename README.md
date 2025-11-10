# Plankd2025-Qubit-Curious

# Bridging Adiabatic Quantum Computation and QAOA  
### 🏆 Planck’d 2025 – Quantum Algorithms Track  
**Team:** Qubit Curious  
**Members:** Aryan Nair, Ansh Goel  

---

## 🧠 Overview
This project explores the deep connection between **Adiabatic Quantum Computation (AQC)** and the **Quantum Approximate Optimization Algorithm (QAOA)** — two leading paradigms for quantum optimization.

Through simulation, visualization, and noise modeling, we demonstrate how QAOA can be interpreted as a **discretized, variational form** of adiabatic evolution, bridging the continuous-time and gate-based models of quantum computation.

This repository was developed as part of **Problems 6–8** of the Planck’d 2025 Quantum Algorithms Track.

---

## 📘 Abstract
We simulate adiabatic evolution for a 2-qubit system and construct a QAOA implementation for a 3-node MaxCut instance, confirming that QAOA acts as a digitized, variationally optimized version of adiabatic evolution.

We further introduce **open-system dynamics** (amplitude damping noise) and **measurement-induced feedback**, showing how decoherence and adaptive correction influence quantum optimization.  

Our results highlight:
- Robust performance of both AQC and QAOA under mild noise  
- Graceful degradation at higher depths  
- Entanglement stabilization under adaptive measurement  

---

## 🧩 Repository Structure
├──code/qaoa_maxcut.ipynb # Main Jupyter notebook with code, simulations, and plots
├── report.pdf # Final write-up (Problems 6–8) submitted to Planck’d 2025
├── README.md # You are here

## 🔬 Problem Breakdown

### **Problem 6 — Adiabatic Quantum Computation**
- Constructed and visualized interpolating Hamiltonian:  
  \( H(s) = (1 - s) H_0 + s H_p \)
- Simulated instantaneous spectra and spectral gaps  
- Verified adiabatic condition through fidelity scaling  
- Observed **quantum walk-like behavior** at the interpolation midpoint

**Result:** Adiabatic success probability scales as \( P_{succ} \propto T^{0.26} \), with fidelity ≥ 0.9 for \( T ≥ 10 \).

---

### **Problem 7 — QAOA as a Discretized Adiabatic Algorithm**
- Implemented 3-node **MaxCut** QAOA using Hamiltonians:
  \( H_p = C = ½[(1 - Z₁Z₂) + (1 - Z₂Z₃) + (1 - Z₃Z₁)] \)
  \( H_m = X₁ + X₂ + X₃ \)
- Compared QAOA expectation values with continuous adiabatic evolution  
- Analyzed the parameter landscape \( ⟨C(γ, β)⟩ \) for depths p = 1, 2, 3  
- Demonstrated **warm-start parameter transfer** for faster convergence  

**Result:** QAOA matches adiabatic-limit fidelity at p ≈ 2 and shows strong robustness to initialization jitter.

---

### **Problem 8 — When the Environment Watches**
- Simulated **amplitude-damping noise** and **measurement-induced entanglement**  
- Identified crossover from **volume-law** to **area-law** entanglement scaling  
- Implemented **adaptive feedback correction** to stabilize coherence  

**Result:** Adaptive feedback stabilizes entropy at moderate measurement rates (pm ≈ 0.1), exhibiting a mild **quantum Zeno-like effect**.

---

