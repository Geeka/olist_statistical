# Olist Freight and Revenue: Statistical Analysis

Two Jupyter notebooks on the Olist Brazilian E-Commerce dataset (Kaggle), delivered orders only. They extend the capstone's [Part 2](https://github.com/Geeka/Part_2_EDA_Hypothesis_Visualizations) analysis of weight and freight, and the statistical notebook reproduces Part 2's result (F = 8,011.32) before building on it.

| Notebook | Questions | Key results |
|---|---|---|
| `olist_statistical_analysis.ipynb` | Does freight differ by weight, and by how much? Which factors drive freight, and do the model's assumptions hold? | Weight tier explains about 13% of freight variation (eta-squared 0.130); Heavy minus Light is 12.92 (95% CI 12.68 to 13.17). Weight and freight: Pearson r = 0.61, Spearman rho = 0.45. Regression: 2.26 more freight per kg, R-squared 0.539. |
| `olist_forecast_regression.ipynb` | How well can next month's revenue be forecast? How well can freight be predicted on unseen orders? | A naive forecast was best (MAPE 8.5%). Linear regression on a holdout set: R-squared 0.543, RMSE 10.24 against 15.15 for a baseline. Gradient boosting: R-squared 0.590. |

**To run:** download [`cleaned_combined_view.csv`](https://github.com/Geeka/Part_2_EDA_Hypothesis_Visualizations/blob/main/cleaned_combined_view.csv) from the Part 2 repo, place it beside the notebooks, and run all cells. Needs pandas, numpy, scipy and matplotlib; the second notebook also needs scikit-learn.

Data credit: Olist, Brazilian E-Commerce Public Dataset (Kaggle).
