# English Premier League (EPL) Match Data Analysis (2000–2025)

## 1. Introduction

**Context:**
The English Premier League (EPL) is one of the most popular and competitive football leagues in the world. Understanding trends in match outcomes and scoring can inform strategic decisions for clubs, analysts, and enthusiasts.

**Dataset Overview:**
- Source: Kaggle EPL Match Data (2000–2025)
- Records: Individual match details, including goals, results, and seasonal data.
- Key Variables:
  - Date of match
  - Home and away teams
  - Full-time goals for home (`FTHG`) and away (`FTAG`) teams
  - Full-time result (`FTR`: H=Home Win, D=Draw, A=Away Win)
  - Season

## 2. Research Questions

1. **What trends in match outcomes (home wins, draws, away wins) can be observed over time?**
2. **How have total goals per season evolved across the observed period?**
3. *(Optional)* Can we build a simple predictive model to estimate match results using available numeric features?

## 3. Data Cleaning and Preparation

**Steps Taken:**
- Converted date fields to standard datetime format.
- Filled missing numeric values with zeros to maintain data consistency.
- Trimmed whitespace in categorical columns.
- Verified dataset integrity (e.g., checking data types, missing values).

This cleaning ensured reproducibility and avoided errors during analysis.

## 4. Exploratory Data Analysis (EDA)

**Descriptive Statistics:**
- Computed summary statistics for goals and match counts.
- Verified the distribution of match results.

**Visualizations:**
- **Total Goals per Season:**
  - A line plot illustrating fluctuations in total goals scored each season.
- **Outcome Distribution:**
  - A count plot of match results showing home wins as the most frequent outcome.

**Insights:**
- While home wins remain dominant, there are observable shifts in draws and away victories over time.
- Seasonal goal totals vary but remain within a comparable range.

## 5. Modeling Approach

**Objective:**
Explore whether match results can be predicted from numeric features (goals scored).

**Methodology:**
- Multinomial Logistic Regression using `FTHG` and `FTAG` as predictors.
- Encoded categorical target variable (`FTR`).

**Results:**
- Model achieved modest predictive accuracy.
- Confusion matrix indicates frequent misclassification between draws and away wins.

**Interpretation:**
While simple numeric features alone are insufficient for high-accuracy prediction, this serves as a baseline illustrating potential for richer modeling.

## 6. Conclusions and Recommendations

**Key Findings:**
- Home advantage is a persistent factor in EPL matches.
- Goal scoring trends exhibit season-to-season variability but no drastic long-term changes.
- Simple models can partially predict match outcomes but require additional contextual features (e.g., team strength, historical performance) for practical use.

**Future Directions:**
- Incorporate advanced features such as betting odds, team form, and player statistics.
- Develop time-series models to forecast future trends.
- Build interactive dashboards to visual

