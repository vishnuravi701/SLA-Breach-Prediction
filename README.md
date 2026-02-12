# -IT-Ticket-Analysis-project

SLA Breach Prediction (XGBoost)

This project builds a binary classification model to predict whether a support incident will miss its SLA at the time of ticket creation.

The model was trained on 119,998 real-world incident records (36 features). All post-creation fields were excluded to prevent data leakage.

Problem

Can we accurately predict SLA breach risk using only information available when a ticket is created?

Early prediction enables proactive intervention and better resource allocation.

Approach

Aggregated event-level logs into incident-level features

Engineered time-based, count-based, and categorical features

Removed post-creation data to enforce realistic prediction constraints

Trained an XGBoost classifier

Used train/test split and cross-validation for evaluation

Performance
Metric	Score
ROC-AUC	0.895
Precision	0.626
Recall	0.881
F1-Score	0.709

The model achieves strong ranking performance (ROC-AUC 0.895) and high recall, prioritizing identification of potential SLA breaches.

Tech Stack

Python, Pandas, NumPy, scikit-learn, XGBoost, Matplotlib, Seaborn
