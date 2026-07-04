# Project Tracker — Customer Churn Prediction

> Status legend: ⬜ Not Started · 🟨 In Progress · ✅ Done

This tracker breaks the project into small, incremental, testable features. Each step builds on the previous one. Anyone (human or AI) opening this file should immediately understand **what's done, what's next, and what depends on what.**

---

## Progress Snapshot

| Phase | Status | % Complete |
|---|---|---|
| Phase 1: Setup | ✅ | 100% |
| Phase 2: Data & EDA | ✅ | 100% |
| Phase 3: Preprocessing | ✅ | 100% |
| Phase 4: Modeling | ✅ | 100% |
| Phase 5: Evaluation | ✅ | 100% |
| Phase 6: Insights & Wrap-up | ⬜ | 0% |
| Phase 7 (Optional): Deployment | ⬜ | 0% |

---

## Phase 1 — Project Setup
- [x] Create project folder structure (`data/`, `notebooks/`, `src/`, `models/`)
- [x] Set up virtual environment / install dependencies
- [x] Download Telco Customer Churn dataset into `data/` (public source not reachable in this environment)
- [x] Create `churn_analysis.ipynb` notebook skeleton

**Depends on:** nothing (first step)
**Unlocks:** Phase 2

---

## Phase 2 — Data Loading & EDA
- [x] Load dataset with pandas, inspect shape/dtypes/nulls
- [x] Check target variable balance (`Churn` column: Yes/No split)
- [x] Univariate analysis: tenure, monthly charges, contract type distributions
- [x] Bivariate analysis: churn rate by contract type, payment method, internet service
- [x] Correlation heatmap for numeric features
- [x] Summarize 3–5 key churn patterns found (write in notebook markdown)

**Depends on:** Phase 1
**Unlocks:** Phase 3
**Output artifact:** EDA charts + written findings in notebook

---

## Phase 3 — Data Preprocessing / Feature Engineering
- [x] Drop irrelevant columns (e.g. `customerID`)
- [x] Handle missing values (e.g. blank `TotalCharges`)
- [x] Encode categorical variables (Label Encoding / One-Hot Encoding)
- [x] Scale numeric features (StandardScaler)
- [x] Split data into train/test sets (e.g. 80/20, stratified)
- [x] Apply SMOTE (or `class_weight='balanced'`) to handle class imbalance

**Depends on:** Phase 2
**Unlocks:** Phase 4
**Output artifact:** `X_train, X_test, y_train, y_test` ready for modeling

---

## Phase 4 — Model Building
- [x] Train Logistic Regression (baseline model)
- [x] Train Random Forest Classifier
- [x] Train XGBoost Classifier
- [x] Save each trained model temporarily for comparison

**Depends on:** Phase 3
**Unlocks:** Phase 5
**Output artifact:** 3 trained model objects

---

## Phase 5 — Model Evaluation
- [x] Generate confusion matrix for each model
- [x] Calculate Accuracy, Precision, Recall, F1-score for each model
- [x] Calculate & plot ROC-AUC curve for each model
- [x] Build comparison table of all 3 models side-by-side
- [x] Select best-performing model (based primarily on Recall + ROC-AUC)

**Depends on:** Phase 4
**Unlocks:** Phase 6
**Output artifact:** Model comparison table + ROC curve plot

---

## Phase 6 — Insights & Wrap-up
- [ ] Extract feature importance from best model (RF/XGBoost)
- [ ] Translate top features into plain-English business insights
      (e.g. "Customers on month-to-month contracts are X% more likely to churn")
- [ ] Write final summary section in notebook / README
- [ ] Export best model using `joblib`

**Depends on:** Phase 5
**Unlocks:** Phase 7 (optional) or Project Complete
**Output artifact:** `models/best_model.pkl`, final insights write-up

---

## Phase 7 — Optional: Deployment / Demo
- [ ] Build simple Streamlit app for live churn prediction
- [ ] Load `best_model.pkl` inside app
- [ ] Add input form for customer features
- [ ] Display churn probability + risk label

**Depends on:** Phase 6
**Unlocks:** N/A (stretch goal)

---


## Notes for future contributors (human or AI)
- Always update the checkbox **and** the Progress Snapshot % when a task is completed.
- If a step is blocked, mark it 🟨 and add a one-line reason next to it.
- Keep insights in plain English — this project is meant to be business-readable, not just technically correct.
