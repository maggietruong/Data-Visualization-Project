# NCAA Basketball Data Visualization & Modeling

### 📊 A Statistical Analysis of Factors Influencing Team Success (2021–2024)

## 👥 Contributors
DevonGrace Tax, Maggie Truong, Michael Helm, John Ramirez, Smyan Jaipuriyar

## 📝 Project Overview
This project explores key statistical factors that contribute to NCAA Division I basketball team success. Our analysis focuses on data from the 2021–2024 seasons and investigates two core questions:

1. **Does a team’s defensive efficiency affect its NCAA tournament performance?**
2. **How do offensive metrics like 3-point shooting accuracy and free throw rate impact win percentage and postseason outcomes?**

## 📁 Dataset
- Source: [Kaggle – College Basketball Dataset](https://www.kaggle.com/datasets/andrewsundberg/college-basketball-dataset)
- Filtered seasons: **2021–2024**
- Variables of interest include:
  - Adjusted Defensive Efficiency (ADJDE)
  - Offensive 3-Point Percentage (Offp_3p)
  - Free Throw Rate (FTR)
  - Win Percentage (Win_P)
  - Postseason Performance (POSTSEASON)

## 🔍 Methods

### 🔹 Exploratory Data Analysis (EDA)
- Dealt with NA values logically for postseason data.
- Generated descriptive statistics and correlation heatmaps.
- Key finding: Strong positive correlation between defensive efficiency and win percentage.

### 🔹 Hypothesis 1: Classification Model
- **Goal**: Predict postseason stage using ADJDE.
- **Model Used**: Multinomial Logistic Regression
- **Result**: 51.94% accuracy. Good performance for early round prediction (e.g., R64), limited accuracy for rarer outcomes (e.g., Champions).
- **Conclusion**: Failed to reject the null hypothesis – defensive efficiency alone is not a strong predictor of postseason advancement.

### 🔹 Hypothesis 2: Regression Models
#### (1) Linear Regression
- **Goal**: Predict win percentage using Offp_3p and FTR.
- **Result**: Statistically significant predictors, R² ≈ 0.19.
- **Conclusion**: Higher 3-point and free throw accuracy are strongly associated with win percentage.

#### (2) Logistic Regression
- **Goal**: Predict postseason success using Offp_3p and FTR.
- **Result**: Offp_3p was a significant predictor; FTR was less impactful.
- **Conclusion**: Rejected null hypothesis – offensive metrics influence postseason performance.

## 📈 Visualizations
- Correlation heatmaps
- Confusion matrices and classification accuracy charts
- Regression scatter plots and residuals
- Precision-recall and ROC curves for model evaluation

## ✅ Key Takeaways
- Defensive efficiency correlates with success but isn't sufficient alone for postseason prediction.
- Offensive shooting metrics (3P%, FTR) are reliable predictors of both win percentage and postseason outcomes.
- Model performance can be enhanced by:
  - Expanding the dataset
  - Incorporating additional features (e.g., turnovers, rebounds, player injuries)
  - Addressing class imbalance in postseason categories

## 📌 Future Improvements
- Add contextual variables (e.g., home-court advantage)
- Explore temporal trends across a season
- Implement ensemble models or advanced classification algorithms for better accuracy
