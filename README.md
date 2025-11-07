# WRF-XGBoost-FAHP-Urban-Hear-Stress
A hybrid modeling framework integrating WRF, XGBoost, and Fuzzy AHP for multi-year urban heat stress risk assessment in Tehran (2019–2022).

### 🧠 Overview
This repository provides the complete workflow, datasets, and scripts developed for the study:

> **“A Hybrid WRF–XGBoost–FAHP Framework for Multi-Year Urban Heat Stress Risk Assessment in Tehran (2019–2022)”**

The framework integrates **numerical modeling (WRF)**, **machine learning downscaling (XGBoost)**, and **multi-criteria decision-making (Fuzzy AHP)** to model and evaluate urban heat stress risk in Tehran.

---

### 🌍 Study Scope
- **Study area:** Tehran Metropolitan Region, Iran  
- **Period:** Four major heatwave events between **2019–2022**  
- **Objective:** Improve spatial resolution and interpretability of urban heat stress mapping  

---

### ⚙️ Methodological Workflow

#### 1️⃣ WRF-Based Numerical Downscaling
- Dynamic simulation of near-surface air temperature (**T2**)  
- Nested configuration refined from **0.25° → 1 km resolution**  
- Validation with ground-based meteorological stations  

#### 2️⃣ Machine Learning Downscaling (XGBoost)
- Further refinement of **T2 layer from 1 km → 100 m resolution**  
- Input features: LST, NDVI, NDBI, slope, elevation, and urban morphology indicators  
- Model optimized using **Bayesian hyperparameter tuning** and **5-Fold Cross-Validation**  
- Explainable AI (**SHAP**) applied for feature importance analysis  

#### 3️⃣ Heat Stress Risk Mapping (Fuzzy AHP)
- Integration of multi-year downscaled T2 maps with socio-economic and urban indicators  
- Weighted overlay using **Fuzzy Analytic Hierarchy Process (FAHP)**  
- Final outputs: multi-year averaged risk maps (2019–2022)  

---

### 📊 Key Results
| Model | Resolution | R² (%) | RMSE (°C) | MAE (°C) |
|--------|-------------|--------|------------|-----------|
| WRF T2 | 1 km | 73.34 | 0.885 | 0.677 |
| XGBoost Downscaled | 100 m | 79.14 | 0.753 | 0.603 |

✅ The hybrid approach improved spatial detail and reduced errors, demonstrating robust generalizability across multiple heatwave periods.

