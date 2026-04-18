# 🔬 Dual-Fuel NOx Analysis

This project investigates the drivers of NOx emissions in a dual-fuel engine dataset, comparing linear, regularised, and tree-based models to assess whether model complexity improves predictive performance.

---

## 🎯 Objective

- Identify key variables influencing NOx emissions  
- Compare multiple modelling approaches (Linear, Ridge, Random Forest)  
- Evaluate whether complex models outperform simple physical relationships  
- Assess dataset realism and limitations  

---

## 📊 Key Findings

- NOx emissions are almost entirely driven by **fuel injection pressure**
- All models achieved similar performance (**R² ≈ 0.98**)
- A **single-variable model** performs as well as multi-feature and non-linear models
- Model complexity provides **no meaningful performance gain**

---

## 🤖 Model Comparison

| Model | R² (CV Mean) |
|------|-------------|
| Linear (all features) | ~0.983 |
| Ridge | ~0.983 |
| Random Forest | ~0.981 |
| Linear (Injection Pressure only) | ~0.983 |

---

## 🧠 Interpretation

The results indicate that predictive performance is dominated by a simple underlying relationship rather than complex interactions.

This highlights an important analytical insight:

> High model performance does not necessarily indicate a strong or realistic model, but may instead reflect dataset simplicity.

---

## ⚠️ Limitations

- Expected physical relationships (e.g. EGR reducing NOx) are not observed  
- The dataset exhibits highly deterministic behaviour  
- Limited interaction between variables  
- Likely simplified or synthetic data generation  

These factors limit real-world applicability of the model.

---

## 📥 Data Source

Dataset sourced from Kaggle:

https://www.kaggle.com/datasets/ziya07/dual-fuel-engine-combustion-dataset

Please download the dataset and place it in the `data_in/` folder to reproduce the analysis.

---

## ⚠️ Note

The notebook outputs are pre-rendered.  
To rerun the analysis, the dataset must be downloaded and placed in the correct directory.
