# ⚙️ Comminution Process Analysis

**End-to-end data science workflow applied to the grinding stage of a copper concentrator.**

> ⚠️ The dataset (`dataset_conminucion_simulado.csv`, 1,000 daily records) was **artificially generated** to simulate plant operation. The goal is to demonstrate the workflow and process reasoning, not to report real plant results.

---

## 🎯 Objectives
- Clean and validate operational data with metallurgical criteria.
- Explore relationships between operating variables and grinding performance.
- Build a model to predict output **P80** from key process parameters.

## 🔢 Variables
Shift, ore type (supergene / hypogene / mixed), Bond work index (BWI), throughput (TPH), energy consumption, P80 in/out, % solids, mill RPM, operating hours, kWh/t.

---

## 🧹 1. Data cleaning
- Imputed 30 missing values (BWI, TPH, energy, mill RPM) with a moving average, checking that mean and standard deviation stayed stable.
- Removed 10 records with output P80 far above the acceptable range (100–300 µm) and 10 with % solids well below 55% (1% each).
- Removed 20 records with “Unknown” ore type (2% of the data).

## 🔍 2. Exploratory analysis — main findings
- Specific energy (kWh/t) decreases as throughput increases.
- For **mixed ore**, operating at **66–70% solids** is associated with greater size reduction.
- Shift A operates at different % solids than shifts B and C for the same ore types — a candidate for standardization.
- No relevant seasonal patterns were found.

## 🤖 3. Predictive model
- `RandomForestRegressor` to predict output P80, tuned with `RandomizedSearchCV` (5-fold CV).
- **Result: no predictive power** — test R² ≈ −0.02 and RMSE ≈ 51 µm after tuning. This is consistent with the EDA: the synthetic data contains no real relationships between features and target.
- Key takeaway: model performance is bounded by the information in the data — tuning cannot create signal that isn't there.

---

## 🛠️ Stack
Python · pandas · NumPy · Matplotlib · seaborn · scikit-learn

## 📂 Files
- `project_en.ipynb` — full analysis (English)
- `dataset_conminucion_simulado.csv` — simulated dataset

## 📞 Contact
**Bastián Albornoz** — Metallurgical Civil Engineer
[LinkedIn](https://www.linkedin.com/in/bastian-albornoz-e/) · bastian.alejandro.a@gmail.com
