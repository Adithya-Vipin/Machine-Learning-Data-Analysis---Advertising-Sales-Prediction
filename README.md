# Advertising Sales Prediction — ML Data Analysis

> Python · Linear Regression · EDA · Clustering · scikit-learn · Finlatics

An end-to-end machine learning analysis of an advertising sales dataset covering 200 campaigns across TV, Radio, and Newspaper channels. Includes exploratory data analysis, multiple linear regression modeling, feature importance analysis, and clustering — identifying TV advertising as the dominant sales driver and building a regression model for ad budget forecasting.

---

## Project Overview

**Dataset:** 200 advertising campaigns — TV spend, Radio spend, Newspaper spend → Sales units

**Goal:** Identify which advertising channels drive sales, build a predictive regression model, and provide data-driven budget allocation recommendations.

**Key finding:** TV advertising is the single strongest predictor of sales by a large margin. Newspaper spend has negligible ROI.

---

## Key Insights

| Finding | Detail |
|---|---|
| Strongest sales driver | **TV advertising** — highest correlation with sales |
| Moderate contributor | **Radio** — positive effect, useful as supporting channel |
| Weakest channel | **Newspaper** — negligible influence, very low ROI |
| Model fit (all variables) | Strong — all three predictors together give reliable predictions |
| Normalization impact | Does not change accuracy; improves coefficient interpretability |
| TV-excluded model | Performance drops significantly — confirms TV is essential |

---

## Analysis Pipeline

```
1. Data Loading & Cleaning
   └── 200 records, 4 features (TV, Radio, Newspaper, Sales)
   └── 2 missing values in Radio column → imputed with mean
   └── No duplicates after cleaning

2. Exploratory Data Analysis (EDA)
   └── Distribution plots for each channel
   └── Correlation matrix — TV vs Sales, Radio vs Sales, Newspaper vs Sales
   └── Average spend per channel
   └── Identified TV as dominant predictor

3. Regression Modeling
   └── Multiple Linear Regression (all 3 predictors)
   └── Radio + Newspaper only (TV excluded) — performance comparison
   └── Normalization experiment — standardized coefficients
   └── Prediction: TV=200, Radio=40, Newspaper=50 → forecasted sales

4. Clustering
   └── K-Means clustering on campaign data
   └── Segment campaigns by spend patterns and sales outcomes

5. Recommendations
   └── Budget allocation strategy based on model findings
```

---

## Regression Results

**Multiple Linear Regression (all predictors):**
- Strong model fit across all 200 campaigns
- TV coefficient dominates — largest effect on predicted sales
- Radio adds moderate positive contribution
- Newspaper coefficient near zero — statistically insignificant

**Feature importance ranking:** TV > Radio >> Newspaper

**Sample prediction:** TV=200, Radio=40, Newspaper=50 → model forecasts sales accurately within confidence interval

---

## Recommendations

Based on analysis findings:

1. **Prioritize TV** — allocate majority of ad budget to TV for maximum sales impact
2. **Maintain Radio** — useful as a supporting channel, especially for targeted/local markets
3. **Reduce Newspaper** — reallocate newspaper budget to TV or Radio for better ROI
4. **Use regression for planning** — model can be used to forecast sales under new budget scenarios before committing spend
5. **Apply normalization** when comparing feature importance or adding new variables

---

## Files

```
├── Sales Prediction - Analysis/
│   ├── Sales_Prediction_Code.pdf         # Full analysis code (PDF)
│   ├── Sales Prediction Data Analysis.pptx  # Presentation slides
│   ├── Sales Prediction Data Analysis PPT.pdf  # Slides (PDF)
│   └── advertising_sales_data.xlsx       # Dataset
└── README.md
```

---

## Tech Stack

![Python](https://img.shields.io/badge/Python-3.8+-3776AB?style=flat&logo=python&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-F7931E?style=flat&logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-EDA-150458?style=flat&logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Plots-11557C?style=flat)

| Task | Tool |
|---|---|
| Data manipulation | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| Regression modeling | scikit-learn (LinearRegression) |
| Clustering | scikit-learn (KMeans) |
| Preprocessing | StandardScaler, SimpleImputer |

---

## Author

**Adithya Vipin** — [GitHub](https://github.com/Adithya-Vipin) · [LinkedIn](https://linkedin.com/in/adithya-vipin-7b6a44281)

B.M.S College of Engineering, Bengaluru — AI & ML (B.E.) | Finlatics Data Science Program, Aug 2025
