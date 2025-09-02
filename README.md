# 🚗 User Churn Prediction from Waze App Usage Data

This project uses data analytics and machine learning in Python to predict monthly user churn in the Waze application. By analyzing app-usage patterns, the model identifies which users are most likely to leave, why they churn, and when churn is most likely to occur. These insights help Waze proactively engage at-risk users, optimize retention strategies, and make data-driven decisions to improve user experience and business growth. The project is based on a synthetic dataset created to simulate real-world application usage.

## Dataset

- `waze_dataset.csv`
- **Source**: Synthetic dataset created in partnership with Waze
- **Features**:

| Column name              | Description                                                                                     |
|------------------------- |-------------------------------------------------------------------------------------------------|
| ID                       | A sequential numbered index                                                                     |
| label                    | Binary target variable ("retained" vs "churned") indicating if a user churned during the month  |
| sessions                 | Number of times a user opened the app during the month                                          |
| drives                   | Number of times a user drove at least 1 km during the month                                     |
| device                   | Type of device a user starts a session with                                                     |
| total_sessions           | Estimated total number of sessions since a user onboarded                                       |
| n_days_after_onboarding  | Number of days since a user signed up for the app                                               |
| total_navigations_fav1   | Total navigations since onboarding to the user’s favorite place                                 |
| total_navigations_fav2   | Total navigations since onboarding to the user’s second favorite place                          |
| driven_km_drives         | Total kilometers driven during the month                                                        |
| duration_minutes_drives  | Total driving duration in minutes during the month                                              |
| activity_days            | Number of days the user opened the app during the month                                         |
| driving_days             | Number of days the user drove (at least 1 km) during the month                                  |

- **Observations**: 14999
- **Class Distribution**:
  - Churned: 17.8%
  - Retained: 82.2%

## Technologies Used

- **Language**: Python
- **Environment**: Jupyter Notebook
- **Libraries**: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scipy`, `sklearn`, `statsmodels`, `imblearn`, `xgboost`
  
 ## Project Breakdown
 1. **`01_waze_eda`** : Initial exploratory data analysis (EDA) to inspect the data and uncover usage patterns and churn trends in it.
 2. **`02_waze_further_eda_visualization`**: Further EDA with visualizations to gain a deeper understanding of the story that the data tells.
 3. **`03_waze_statistical_analysis`**: Statistical analysis (hypothesis testing and confidence intervals) to draw more insights from the data.
 4. **`04_waze_logistic_regression`**: Binomial logistic regression modeling.
 5. **`05_waze_tree_models`**: Tree-based modeling (Random Forest and XGBoost).

## Modeling Results

Two models delivered the best performance in predicting churn:

- **Logistic Regression**  
  Built with feature engineering, Elastic Net regularization, and Synthetic Minority Oversampling Technique (SMOTE) to address class imbalance.  
  **Performance**: 74% recall and AUC of 0.7, indicating decent discriminative ability while effectively capturing churned users.

- **XGBoost**  
  Developed with feature engineering and hyperparameter tuning via cross-validation.  
  **Performance**: 83% recall and AUC of 0.69, excelling at capturing churned users while maintaining acceptable discriminative ability.

## How to Run

1. Clone this repository or download it as a ZIP from GitHub. 
2. Open the project folder in your preferred environment.
3. Open the notebooks sequentially (or in any order you prefer) and run the cells.

## Author

Developed by Juan Nathan.
