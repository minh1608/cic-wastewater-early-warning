# CIC Wastewater Early Outbreak Detection

This repository contains the Kaggle notebook and supporting artifacts for our **CDC wastewater-based COVID surveillance modeling** project.  
The pipeline ingests NWSS regional CSV data, engineers features, builds labels, and evaluates baseline vs. XGBoost models for two tasks:
- **Hotspot@14d classification**
- **Time-to-Threshold regression**

---

## ⚙️ Environment Setup

### Option 1 — pip
```bash
pip install -r requirements.txt
```

### Option 2 — conda
```bash
conda env create -f environment.yml
conda activate cic-wastewater
```

---

## 📑 Notebook Workflow

Steps implemented in the notebook:
1. Load and clean NWSS CSV  
2. Reshape and feature engineering  
3. Label creation (Hotspot@14d, Time-to-Threshold)  
4. Baseline models (Logistic, Linear)  
5. XGBoost models with walk-forward CV  
6. Sensitivity analysis (85/90/95 thresholds)  
7. Results tables (Markdown + LaTeX export)  
8. Figures and calibration plots  
9. Packaged outputs (`outputs_for_paper.zip`)

---

## 📦 Outputs

After running the notebook, you will find:
- Processed datasets: `nwss_long.csv`, `nwss_features.csv`, `nwss_features_labels.csv`
- Analysis tables: `ablation_classification.csv`, `ablation_regression.csv`, `threshold_sensitivity_results.csv`, `results_table.tex`
- Figures: multiple `.png` plots (threshold curves, PR curves, calibration, ablation, etc.)
- Combined archive: `outputs_for_paper.zip`

---

## 🚀 How to Run This Project

1. **Clone the repo**
   ```bash
   git clone https://github.com/minh1608/cic-wastewater-early-warning.git
   cd cic-wastewater-early-warning
   ```

2. **Setup environment**
   - Using pip:
     ```bash
     pip install -r requirements.txt
     ```
   - Or with conda:
     ```bash
     conda env create -f environment.yml
     conda activate cic-wastewater
     ```

3. **Run the notebook**
   - Open Jupyter or VS Code and run:
     ```
     notebooks/who-s-next.ipynb
     ```

4. **Reproduce results**
   - Outputs (CSV, figures, LaTeX table, ZIP) will be generated in the project root after running all notebook cells.
   - Main artifacts include:
     - `nwss_long.csv`, `nwss_features.csv`, `nwss_features_labels.csv`
     - `ablation_classification.csv`, `ablation_regression.csv`
     - `threshold_sensitivity_results.csv`, `results_table.tex`
     - Plots in `.png`
     - Combined `outputs_for_paper.zip`

5. **Publication**
   - Use `results_table.tex` in LaTeX papers for ready-to-go results table.
   - Figures can be inserted directly into your manuscript or slides.

---

## 📜 Citation

If you use this work, please cite:

```
Nguyen, P. M., et al. (2025). "Who’s Next? AI-Enhanced Wastewater Surveillance for Early Outbreak Detection in Underserved Communities."
Proceedings of the 2025 CIC/CDC Conference.
```
