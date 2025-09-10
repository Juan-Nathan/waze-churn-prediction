# 🚗 Waze User Churn Prediction

This project applies advanced data analytics in Python to predict monthly **user churn** in the Waze application using a synthetic **dataset that simulates real-world application usage and user behavior**. Churn measures the number of users who either uninstalled or stopped using the Waze app.

An effective model will help determine which users are most likely to churn, why they churn, and when churn occurs.

These insights can enable Waze to proactively engage at-risk users, optimize retention strategies, and make data-driven decisions to improve user experience and business growth.

## Dataset

- `waze_dataset.csv`
- **Source**: Synthetic dataset created in partnership with Waze
- **Observations**: 14,999
- **Variables**:

| Column Name                | Description                                                                                         |
|-------------------------   |-----------------------------------------------------------------------------------------------------|
| `ID`                       | A sequential numbered index                                                                         |
| `label`                    | Binary **target** variable ("retained" vs "churned") indicating if a user churned during the month  |
| `sessions`                 | Number of times a user opened the app during the month                                              |
| `drives`                   | Number of times a user drove at least 1 km during the month                                         |
| `device`                   | Type of device a user starts a session with                                                         |
| `total_sessions`           | Estimated total number of sessions since a user onboarded                                           |
| `n_days_after_onboarding`  | Number of days since a user signed up for the app                                                   |
| `total_navigations_fav1`   | Total navigations since onboarding to the user’s favorite place                                     |
| `total_navigations_fav2`   | Total navigations since onboarding to the user’s second favorite place                              |
| `driven_km_drives`         | Total kilometers driven during the month                                                            |
| `duration_minutes_drives`  | Total driving duration in minutes during the month                                                  |
| `activity_days`            | Number of days the user opened the app during the month                                             |
| `driving_days`             | Number of days the user drove (at least 1 km) during the month                                      |

- **Class Distribution**:
  - Churned: 18%
  - Retained: 82%

## Technologies Used

- **Language**: Python
- **Environment**: Jupyter Notebook
- **Libraries**: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scipy`, `statsmodels`, `sklearn`, `imblearn`, `xgboost`
  
## Project Structure
 
 1. **`01_eda.ipynb`**: Initial exploratory data analysis (EDA) to examine the data and uncover usage patterns and churn trends.
 2. **`02_further_eda_visualization.ipynb`**: Further EDA with visualizations to gain a deeper understanding of the story that the data tells.
 3. **`03_statistical_analysis.ipynb`**: Statistical analysis (hypothesis testing and confidence intervals) to draw more insights from the data.
 4. **`04_logistic_regression.ipynb`**: Binomial logistic regression modeling, including data preprocessing and multicollinearity testing using the Variance Inflation Factor.
 5. **`05_tree_models.ipynb`**: Tree-based modeling (Random Forest and XGBoost), including data preprocessing.

## Modeling Results

Two models delivered the best performance in predicting churn:

- **Logistic Regression**  
  - Developed with **feature engineering** and **Elastic Net regularization** on data balanced using the **Synthetic Minority Oversampling Technique**.
  - **Performance**: 74% recall and AUC of 0.70, effectively identifying likely churners while providing fair discriminative ability.
- **XGBoost**  
  - Built with **feature engineering** and **hyperparameter tuning** via cross-validation.  
  - **Performance**: 83% recall and AUC of 0.69, excelling at capturing users at risk of churn while maintaining acceptable discriminative ability.

## How to Run

1. Clone this repository or download it as a ZIP from GitHub. 
2. Open the project folder in your preferred environment.
3. Open the notebooks sequentially (or in any order you prefer) and run the cells.

## Author

Developed by Juan Nathan.
