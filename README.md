# bike-sharing-system

BoomBikes, a US bike-sharing provider, has seen a significant drop in revenues due to the COVID-19 pandemic. To prepare for post-pandemic demand, they want to understand the factors influencing bike demand and have collected a dataset on daily bike rentals.

Business Goal:
- **Objective:** Model the demand for shared bikes using the available data.
- **Target Variable:** `cnt` (total bike rentals)
- **Independent Variables:** Various factors, including weather, season, and year.

Data Preparation:
- Convert categorical features (e.g., `weathersit`, `season`) from numerical to string labels.
- Keep the `yr` column, as it may indicate increasing demand over years.

Model Building:
- Include `casual`, `registered`, and `cnt` in the dataset but use `cnt` as the target variable for the model.

Model Evaluation:
- Calculate R-squared on the test set using:
  ```python
  from sklearn.metrics import r2_score
  r2_score(y_test, y_pred)
  ```
