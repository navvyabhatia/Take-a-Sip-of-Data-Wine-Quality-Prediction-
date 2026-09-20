# Take-a-Sip-of-Data-Wine-Quality-Prediction-
By: Navya Bhatia, Joane Sarfati, Sami Shikhare, Mrudhvika Sirineni, and Mya Stewart

Developed an advanced machine learning pipeline to predict red and white wine quality using 6,400+ samples and 11 chemical features. Benchmarked Random Forest, Gradient Boosting, and Bagging through cross-validation and tuning. Random Forest performed best (R² = 0.49), enabling automated scoring and identifying the main chemical drivers of quality.

# Project Objective
Wine quality is traditionally evaluated by expert tasters using sensory characteristics such as flavor, aroma, color, and balance. Although valuable, this process can be subjective, time-consuming, and costly. This project explores a data-driven alternative by using physicochemical measurements to estimate expert-assigned quality scores.

Separate models were developed for red and white Vinho Verde wines to account for differences between the two wine types. The project combines exploratory data analysis, feature interpretation, cross-validation, hyperparameter tuning, and model comparison to determine the most reliable prediction approach.

# Objectives
- Predict wine quality scores from measurable chemical properties.
- Compare Random Forest, Gradient Boosting, and Bagging regressors.
- Evaluate model accuracy and generalization using multiple regression metrics.
- Identify the most influential quality drivers for red and white wine.
- Translate the results into recommendations for wine producers and sellers.

# Dataset
The project uses the Wine Quality Dataset from the UCI Machine Learning Repository. The data contains laboratory measurements and expert quality ratings for Portuguese Vinho Verde wines.

# Technologies Used
- Python
- Jupyter Notebook
- pandas
- NumPy
- Matplotlib
- Seaborn
- scikit-learn

# Repository Structure

```text
wine-quality-prediction/
│
├── README.md
│
├── notebooks/
│   └── MLFinalProject-FINAL.ipynb
│
├── reports/
│   ├── ML-Final-Project-Report.pdf
│   └── ML-Final-Project-Presentation.pdf
│
├── data/
│   ├── winequality-red.csv
│   └── winequality-white.csv
```

# Input Features
1. Fixed acidity
2. Volatile acidity
3. Citric acid
4. Residual sugar
5. Chlorides
6. Free sulfur dioxide
7. Total sulfur dioxide
8. Density
9. pH
10. Sulphates
11. Alcohol

# Analytical Workflow
1. Loaded and inspected the red and white wine datasets.
2. Checked data quality and confirmed there were no missing values.
3. Explored quality distributions, feature correlations, and chemical relationships using bar charts, heatmaps, and scatterplots.
4. Split each dataset into 80% training and 20% testing data using random_state=42.
5. Standardized the predictors with StandardScaler for a consistent modeling pipeline.
6. Trained three ensemble regression models separately for red and white wine.
7. Tuned model hyperparameters with GridSearchCV and 10-fold cross-validation using negative mean squared error.
8. Evaluated test performance using R-squared, MSE, RMSE, and MAE.
9. Compared feature importance rankings and predicted-versus-actual results.

# Key Findings
- Alcohol was the strongest overall predictor of quality for both red and white wine.
- Sulphates had substantially more influence on red-wine quality than on white-wine quality.
- Free and total sulfur dioxide were more influential for white wine.
- Volatile acidity was important for both wine types.
- Random Forest captured nonlinear relationships effectively and delivered the most consistent performance across the two datasets.
- Predictions followed the overall pattern of actual quality ratings, but exact scores remained difficult to estimate because ratings were concentrated in a narrow middle range.

# Dataset Source:

Cortez, P., Cerdeira, A., Almeida, F., Matos, T., and Reis, J. (2009), Wine Quality Dataset, UCI Machine Learning Repository.
