# Asymmetric Cost-Channel Monetary Transmission and Policy-Rate Thresholds: Evidence from Egypt

**Author:** Mohamed Fawzy AbdulAziz  
**Affiliations:**  
- Research Department, Information and Decision Support Center (IDSC), The Egyptian Cabinet, Cairo, Egypt  
- Department of Economics, Faculty of Economics and Political Science, Cairo University, Giza, Egypt  
**Email:** mohamed.abdulaziz@idsc.gov.eg  

---

## 📌 Overview & Replication Package

This repository contains the complete empirical replication suite, master macroeconomic database, and structural estimation routines for the research paper:

> **"Asymmetric Cost-Channel Monetary Transmission and Policy-Rate Thresholds: Evidence from Egypt"**  
> *The Journal of Economic Asymmetries*

---

## 📂 Repository Contents

- `run_full_paper_replication.py`: One-click master Python replication script that executes all empirical models (Hansen Threshold Estimation, Two-Step Optimal GMM, NARDL ECM, Machine Learning Tournament, Blocked Time-Series Cross-Validation, and Theoretical Calvo Inversions).
- `data/Egypt_Master_Macroeconomic_Database_2005_2026.xlsx`: Comprehensive master macroeconomic time-series database ($2005\text{M}01$--$2026\text{M}04$) with full monthly variables, raw indicators, and historical series.
- `data/Egypt_ACC_NKPC_Monthly_Dataset_2010_2026.xlsx`: Standardized empirical estimation dataset ($2011\text{M}01$--$2026\text{M}04$, $T=184$) utilized directly by `run_full_paper_replication.py`.
- `manuscript.tex`: Complete LaTeX master manuscript (elsarticle format).
- `theoretical_derivation.md`: Complete step-by-step mathematical micro-foundations of the Hybrid ACC-NKPC model.

---

## 🚀 One-Click Replication

### 1. Requirements
Ensure Python 3.9+ is installed along with the required econometric and machine learning packages:

```bash
pip install numpy pandas scipy statsmodels scikit-learn xgboost lightgbm shap openpyxl matplotlib
```

### 2. Running Full Empirical Replication
Execute the master replication script:

```bash
python run_full_paper_replication.py
```

The script will automatically:
1. Load and validate the master dataset ($2011\text{M}01$--$2026\text{M}04$).
2. Perform Unit Root (ADF, PP, KPSS) and BDS independence tests.
3. Estimate the Hansen (2000) threshold switching model and identify the optimal policy threshold ($i^* = 20.0\%$).
4. Run Two-Step Optimal GMM structural estimations with HAC standard errors and Wald asymmetry tests.
5. Train Machine Learning benchmarks (GBM, Random Forest, SVR, MLP, LSTM) across the out-of-sample window ($2025\text{M}01$--$2026\text{M}04$) and compute Diebold--Mariano test statistics.
6. Generate 24-month ahead conditional policy projections across 3 distinct macroeconomic scenarios (Baseline, Sticky Reform, External Stress).

---

## 📊 Summary of Main Empirical Results

| Parameter / Metric | Estimated Value | Econometric Interpretation |
| :--- | :---: | :--- |
| **Optimal Policy Threshold ($i^*$)** | **$20.0\%$** | Hansen (2000) switching threshold ($95\%$ LR: $[18.5\%, 21.5\%]$) |
| **Cost-Channel Slope Below Threshold ($\phi_{\text{Low}}^+$)** | **$+1.8783^{***}$** | Monetary tightening increases short-run inflation (Price Puzzle) |
| **Cost-Channel Slope Above Threshold ($\phi_{\text{High}}^+$)** | **$+0.1232$** | Aggregate demand contraction dominates cost channel ($W=19.84^{***}$) |
| **FX Depreciation Pass-Through ($\lambda^+$)** | **$+8.2912^{***}$** | Highly asymmetric pass-through ($\lambda^- \to 0$, $W=8.72^{***}$) |
| **Upward Price Stickiness ($\theta^+$)** | **$0.548$** | Implied duration: **$2.21\text{ months}$** (Rockets) |
| **Downward Price Stickiness ($\theta^-$)** | **$0.832$** | Implied duration: **$5.95\text{ months}$** (Feathers) |
| **GBM Out-of-Sample Accuracy ($\text{RMSE}$)** | **$3.060\text{ pp}$** | Statistically outperforms $\text{AR}(2)$ ($\text{DM} = -3.84, p < 0.001$) |

---

## 📜 Citation

If you use this dataset or replication code in your research, please cite:

```bibtex
@article{abdulaziz2026asymmetric,
  title={Asymmetric Cost-Channel Monetary Transmission and Policy-Rate Thresholds: Evidence from Egypt},
  author={AbdulAziz, Mohamed Fawzy},
  journal={The Journal of Economic Asymmetries},
  year={2026}
}
```

---

## 📄 License
This project is licensed under the MIT License - see the LICENSE file for details.
