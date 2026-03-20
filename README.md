# XSBFEM-XGBoost Crack Frequency Prediction

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![DOI](https://img.shields.io/badge/DOI-Pending-blue.svg)](https://doi.org/...) 

This repository contains the dataset, pre-trained models, and source code associated with the research paper: **"Hybrid XSBFEM-Machine Learning Framework for Accurate Free Vibration Prediction of Cracked BDFGM Plates with SHAP-Based Interpretability."**

Our work proposes a novel hybrid framework that integrates the numerical rigor of the Extended Scaled Boundary Finite Element Method (XSBFEM) with the rapid predictive capabilities of Machine Learning (ML), specifically a BCMO-tuned XGBoost model. 

## 🚀 Key Features
* **High-Fidelity Dataset:** A comprehensive dataset of 3,000 vibration scenarios for cracked Bidirectional Functionally Graded Material (BDFGM) plates, generated using our highly stable XSBFEM solver.
* **Pre-trained ML Models:** Includes the highly accurate BCMO-XGBR model (R² = 0.999), capable of real-time natural frequency prediction.
* **Efficiency Verification Data:** Additional datasets generated via Latin Hypercube Sampling (LHS) specifically designed to test and verify the computational efficiency and generalization of the models.
* **SHAP Interpretability:** Tools to quantify how boundary conditions, grading indices, and crack length influence dynamic responses.
* **XSBFEM Benchmark Code:** Open-source XSBFEM code for a classic fracture mechanics benchmark (an inclined center crack under uniform tensile loads), including the computation of Mode I and Mode II Stress Intensity Factors (SIFs).

## 📁 Repository Structure

```text
├── Data/
│   ├── training_data_3000.csv       # Original dataset generated via XSBFEM
│   └── lhs_efficiency_test.csv      # LHS generated data for efficiency testing
├── Models/
│   ├── bcmo_xgboost_model.pkl       # Pre-trained BCMO-XGBR regression model
│   └── shap_analysis.py             # Script for generating SHAP summary plots
├── XSBFEM_Code/                     
│   ├── inclined_crack_benchmark.m   # Main script for the inclined center crack example
│   ├── mesh_generation/             # Subdomain and quadtree mesh generation
│   └── utils/                       # SIF calculation (Mode I & II) functions
├── Results/
│   └── SIF_comparisons/             # Analytical vs. Numerical SIF plots
├── requirements.txt
└── README.md
