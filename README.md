📦 Stockout Forecasting — LabelVie Simulation Project
⚠️ Disclaimer: The dataset used in this project is a simulation and does not reflect real business data due to confidentiality constraints.

📍 Project Overview
This project aims to predict stockout risks at the product level using historical demand data, calendar effects, and store-product features. It follows a complete machine learning pipeline: data ingestion, cleaning, feature engineering, modeling, and evaluation.

The project was inspired by a real-world use case from LabelVie and developed as a final internship project.

🧰 Tools & Technologies
Python (Pandas, NumPy, Scikit-learn, CatBoost)

Jupyter Notebooks

Git for version control

📁 Project Structure
bash
Copier
Modifier
├── data_tables_sources.ipynb         # Data loading and merging from various sources
├── Descreption de données.ipynb     # Initial data exploration and visualization
├── feature_engeneering V1.ipynb     # Feature creation (lags, rolling, calendar, encoding)
├── modeling.ipynb                   # ML modeling (classification: stockout risk)
├── README.md                        # You are here
🔬 Feature Engineering Highlights
The dataset includes key transformations such as:

Time-based features: Day of week, Month, Day of year

Demand lags: lag_1, lag_7, lag_14

Rolling averages and std: rolling_mean_7, rolling_std_7

Seasonality signals: sin_doy, cos_doy

Calendar events: Ramadan, Aïd, Public Holidays

Categorical variables were encoded using frequency and label encodings (e.g. store_id, DEP, RAY, GRP).

🧠 Model Used
CatBoostClassifier (for binary classification of stockout_occurred)

Evaluation metrics:

Accuracy

Precision / Recall

ROC AUC

Confusion Matrix

📈 Business Insight
This forecasting pipeline enables supply chain teams to:

Anticipate product-level stockout risks

Prioritize replenishment actions

Improve service levels with proactive stock management

🚫 Limitations
Synthetic data: Not suitable for production use

Focused only on binary stockout classification (0/1), not demand regression

Time range: Jan–Apr 2025

