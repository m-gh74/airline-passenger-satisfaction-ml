# ✈️ Airline Passenger Satisfaction — ML Classification



> **Last updated:** 2025-10-06

---

## 📦 Dataset
- Source: Kaggle —(https://www.kaggle.com/datasets/teejmahal20/airline-passenger-satisfaction)
- Columns typically include: passenger demographics, loyalty, travel type, class, service ratings (wifi, seat comfort, entertainment, booking, cleanliness, ...), departure/arrival delays, and the label **`satisfaction`**.


---

## ▶️ Open in Colab

https://colab.research.google.com/drive/1X56ZzDbTdNiZpzRFMnyC04ZzNTyVPDHj

---

## 🚀 Quickstart (Local)
```bash
pip install -r requirements.txt




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
