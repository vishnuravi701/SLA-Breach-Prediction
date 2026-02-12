
# SLA Breach Prediction (XGBoost)

This project builds a **binary classification model** to predict whether a support incident will miss its SLA at the time of ticket creation. Early prediction enables **proactive intervention** and **better resource allocation**.

---

## Problem Statement

- Can we accurately predict SLA breach risk using only information available **at ticket creation**?  
- Early identification allows support teams to **prioritize high-risk incidents** and manage resources effectively.

---

## Dataset

- **Records:** 119,998 real-world incident records  
- **Features:** 36 features (all post-creation fields excluded to prevent data leakage)

---

## Approach

- Aggregated **event-level logs** into **incident-level features**  
- Engineered **time-based**, **count-based**, and **categorical features**  
- Removed **post-creation data** to enforce realistic prediction constraints  
- Trained an **XGBoost classifier**  
- Evaluated using **train/test split** and **cross-validation**

---

## Performance

| Metric       | Score  |
|--------------|--------|
| ROC-AUC      | 0.895  |
| Precision    | 0.626  |
| Recall       | 0.881  |
| F1-Score     | 0.709  |

- Strong ranking performance (**ROC-AUC 0.895**)  
- High recall prioritizes **identification of potential SLA breaches**

---

## Tech Stack

- **Python**  
- **Pandas, NumPy**  
- **scikit-learn**  
- **XGBoost**  
- **Matplotlib, Seaborn**

---

