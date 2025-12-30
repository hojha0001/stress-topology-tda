# Stress State Discovery using Topological Data Analysis (TDA)

## Overview
This project presents an unsupervised, geometry-based approach to discover latent stress states from wearable biometric data. 
Instead of predicting a stress score, the system models the *topology of physiological states* using Topological Data Analysis (TDA).

The approach is label-agnostic and focuses on uncovering hidden structures, transitions, and recurrent patterns in stress-related signals.

---

## Motivation
Traditional stress monitoring systems rely on:
- Threshold-based rules
- Supervised classification
- Binary stress vs no-stress labels

These approaches fail to capture:
- Transitional stress states
- Recovery dynamics
- Repetitive/chronic stress patterns

This project addresses those gaps using **Topological Data Analysis**.

---

## Dataset
- **SWELL Dataset (Interim version)**
- Signals used:
  - Electrodermal Activity (EDA)
  - (Extendable to HRV / RRI)

Data is processed at subject level and segmented into overlapping time windows.

---

## Methodology

### 1. Signal Preprocessing
- Detrending
- Z-score normalization
- Sliding window segmentation (256 samples)

### 2. High-Dimensional Representation
Each window is treated as a high-dimensional physiological snapshot.

### 3. Topological Mapping
- Lens: PCA (2D)
- Covering: Hypercubes
- Clustering: DBSCAN
- Tool: Kepler Mapper

This produces a topological graph where:
- Nodes represent stable physiological states
- Edges represent transitions between states

---

## Output
- Interactive topological graph (`stress_topology.html`)
- Nodes encode stress-related physiological regimes
- Graph structure reveals:
  - Stable states
  - Transitional bridges
  - Recurrent loops (possible chronic stress)

---

## Key Insights
- Stress is not binary; it exists on a continuous manifold
- Transitional stress states are critical early-warning indicators
- Topological loops may indicate repetitive stress exposure

---

## Tech Stack
- Python
- NumPy, Pandas, SciPy
- Scikit-learn
- Kepler Mapper
- Jupyter Notebook

---

## Future Extensions
- Multi-modal fusion (EDA + HRV)
- Temporal persistence analysis
- Subject-independent stress topology
- Deployment on real-time wearable streams

---

## Author
Himanshu Ojha  
(Data Science | Machine Learning | Unsupervised Learning | TDA)
