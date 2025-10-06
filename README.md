# ✈️ Airline Passenger Satisfaction — ML Classification



> **Last updated:** 2025-10-06

---

## 📦 Dataset
- Source: Kaggle —(https://www.kaggle.com/datasets/teejmahal20/airline-passenger-satisfaction)
- Columns typically include: passenger demographics, loyalty, travel type, class, service ratings (wifi, seat comfort, entertainment, booking, cleanliness, ...), departure/arrival delays, and the label **`satisfaction`**.
- **Please review and state the dataset's license/terms of use here.**

> **Do not commit the full dataset.** Use the auto-download cell below and keep only a tiny sample in `data/sample/`.

---

## ▶️ Open in Colab
After you push this repo, replace the placeholders below with your own GitHub user/repo:

https://colab.research.google.com/drive/1X56ZzDbTdNiZpzRFMnyC04ZzNTyVPDHj

---

## 🚀 Quickstart (Local)
```bash
pip install -r requirements.txt
# Then open the notebook in notebooks/ and run the "Download dataset" cell
```

### 📥 Kaggle auto-download cell (add to your notebook)
```python
# Install Kaggle CLI
!pip -q install kaggle

# Put your kaggle.json once (do NOT commit it)
!mkdir -p ~/.kaggle
!cp kaggle.json ~/.kaggle/
!chmod 600 ~/.kaggle/kaggle.json

# Download (change the dataset slug if you used a different one)
import os; os.makedirs("data/raw", exist_ok=True)
!kaggle datasets download -d teejmahal20/airline-passenger-satisfaction -p data/raw
!unzip -o "data/raw/*.zip" -d data/raw
```

---

## 🔁 Reproducibility
Add a top cell that fixes seeds and prints package versions:
```python
import sys, platform, random, os, numpy as np, pandas as pd
SEED = 42
random.seed(SEED); np.random.seed(SEED)
print("Python:", sys.version.split()[0])
print("Platform:", platform.platform())
print("Pandas:", pd.__version__)
os.makedirs("data/raw", exist_ok=True); os.makedirs("data/processed", exist_ok=True)
```

---

## 📁 Project Structure
```
.
├─ notebooks/
│  └─ Airline_Passenger_Satisfaction_Project.ipynb
├─ src/                      # Optional: modules/scripts
├─ data/
│  ├─ sample/                # Tiny demo subset
│  ├─ raw/                   # Raw data (gitignored)
│  └─ processed/             # Processed data (gitignored)
├─ reports/
│  └─ figures/               # Plots and exported figures
├─ scripts/                  # Helper scripts (optional)
├─ requirements.txt
├─ .gitignore
└─ LICENSE
```

---

## 🧱 Preprocessing (typical)
- Encode binary categoricals (e.g., Gender, Customer Type, Type of Travel, satisfaction).
- Ordinal map for `Class`: `{'Eco': 0, 'Eco Plus': 1, 'Business': 2}` (if applicable).
- Train/validation split with `stratify=y` and a fixed `random_state`.

---

## 🤖 Models (examples)
- Logistic Regression
- RandomForestClassifier (with RandomizedSearchCV)
- LightGBM (basic tuning)

> Print `classification_report` and `roc_auc_score` and save key plots (ROC/PR, SHAP) to `reports/figures/`.

### 📈 Results (fill with your numbers)
| Model | Accuracy | ROC-AUC |
|---|---:|---:|
| Logistic Regression | ... | ... |
| Random Forest (tuned) | ... | ... |
| LightGBM (tuned) | ... | ... |

---

## 🧠 Explainability
If you use SHAP:
- Add `shap.Explainer` and export `summary_plot` to `reports/figures/`.
- Briefly discuss the top features and whether they align with domain intuition.

---

## ✅ Publication Checklist
- [ ] Replace `<GITHUB_USER>/<REPO_NAME>` and dataset link
- [ ] Add the "Download dataset" cell (no absolute Colab/Drive paths)
- [ ] Clear heavy notebook outputs before committing
- [ ] Add a tiny sample CSV to `data/sample/`
- [ ] Document dataset **license**

---

## 📝 Citation
If others use this work or the dataset, include appropriate citations. For the dataset, use the citation suggested on its Kaggle page.

---

## 📄 License
MIT (see `LICENSE`).
