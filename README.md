# SIGNAL-SET-CAPACITY
# Rotation Optimization in Multi-User Communication Systems

This repository contains simulation results for **rotation angle optimization** in 2-user and 3-user multi-user MIMO communication systems.  
The optimization aims to minimize the constellation cost function for different modulation schemes (**BPSK, QPSK, 8PSK, 8QAM**) over a range of SNR values.

---

## 📊 Overview of Findings

### General Trends
- **More users → higher potential improvement**  
  - Moving from **2 users** to **3 users** increases the optimization degrees of freedom, allowing significantly larger cost reductions at moderate and high SNR.
- **SNR dependency**  
  - At **low SNR (≤ 0 dB)**, improvements are small for both cases due to noise dominance.  
  - At **moderate-to-high SNR (≥ 6 dB)**, improvements grow substantially, especially for higher-order constellations.
- **Multiplicity**  
  - Symmetric constellations (BPSK, QPSK) have higher multiplicity in the 2-user case due to rotational symmetry.  
  - Multiplicity decreases in the 3-user case because of fewer equivalent optima when optimizing over two rotation angles.

---

## 📈 Constellation-Specific Observations

### BPSK
**2 Users**
- Optimal angle stays ~90° for low–moderate SNR, shifting slightly at high SNR.
- Improvement saturates at ~**2 units** beyond 6 dB.

**3 Users**
- At low SNR: (θ₂, θ₃) ≈ (60°, 120°)  
- At high SNR: shifts to (35°, 75°)  
- Improvement saturates near **12 units**, much larger than in the 2-user case.

---

### QPSK
**2 Users**
- Low-SNR improvement < 1.5 units.  
- From 4 dB upward, gains grow rapidly to ~**20 units** at 16 dB.
- Optimal θ alternates between large angles (~45°/135°) and smaller (~30°) depending on SNR.

**3 Users**
- At low SNR: (θ₂, θ₃) ≈ (30°, 60°) with small gains.  
- At high SNR: smaller coordinated angles (20°, 40°) outperform large single rotations.  
- Gains exceed **300 units** at 16 dB — far greater than the 2-user case.

---

### 8PSK
**2 Users**
- Negligible improvement (<0.001) until ~6 dB, then rapid increase to **79 units** at 16 dB.
- Optimal θ shifts from ~112.5° to ~75° or 150° as SNR rises.

**3 Users**
- Not fully tabulated here, but higher-order modulation trends suggest significantly greater improvement than in 2-user systems at high SNR.

---

### 8QAM
**2 Users**
- Gradual increase from 0.35 units at −2 dB to **48 units** at 16 dB.
- Optimal θ alternates between 45° and 135° depending on SNR.

**3 Users**
- Data not fully listed, but expected to follow the QPSK/8PSK pattern, with larger gains due to coordinated dual-angle optimization.

---

## 🚀 Key Takeaways
- **Higher number of users → greater benefit from rotation optimization.**
- **Optimal rotation angles are SNR-dependent.**
- **Higher-order constellations gain the most** from this technique.
