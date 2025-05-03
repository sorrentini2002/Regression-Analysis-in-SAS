# 📊 Regression Analysis in SAS

This repository presents four detailed regression analyses conducted using SAS. Each analysis follows a structured approach, focusing on model building, diagnostics, and refinement, with an emphasis on practical implementation and statistical concepts.

---

## 📝 Sommario

- [Analyses Included](#analyses-included)
  - [Forbes Data Analysis](#1-forbes-data-analysis)
  - [Gesell Data Analysis](#2-gesell-data-analysis)
  - [Fitness Data Analysis](#3-fitness-data-analysis)
  - [Pollution Mortality Analysis](#4-pollution-mortality-analysis)
- [Common Methodological Approach](#common-methodological-approach)
- [Technical Implementation](#technical-implementation)
- [Key Lessons](#key-lessons)
- [Conclusion](#conclusion)
- [License](#license)

---

## Analyses Included

### 1. Forbes Data Analysis

**Objective**: Investigates the relationship between boiling point (x) and pressure (y).  
**Key Steps**:
- Initial linear regression model.
- Addition of a quadratic term for model improvement.
- Detection and removal of outliers (observations 12, 1, 2).
- Residual diagnostics to assess model fit.

### 2. Gesell Data Analysis

**Objective**: Analyzes the relationship between age (x) and developmental score (y).  
**Key Steps**:
- Development of an initial linear model.
- Iterative outlier removal (observations 18, 2, 19).
- Normality assessment of residuals.
- Final model validation after adjustments.

### 3. Fitness Data Analysis

**Objective**: Predicts oxygen consumption (Oxy) based on various physiological measures.  
**Key Steps**:
- Evaluation of multicollinearity (e.g., high correlation between RunPulse and MaxPulse).
- Stepwise variable selection to optimize the model.
- Handling of outliers (observation 10).
- Model validation through various diagnostic checks.

### 4. Pollution Mortality Analysis

**Objective**: Models death counts (y) as a function of pollution measures (smog x, sulfur dioxide z).  
**Key Steps**:
- Detection of multicollinearity using VIF/TOL.
- Forward and backward selection for variable inclusion.
- Iterative outlier removal (observations 6, 5, 12, 9).
- Final model diagnostics to ensure the validity of results.

---

## Common Methodological Approach

All analyses follow a consistent methodological framework:

### Exploratory Data Analysis:
- Correlation assessment to identify potential relationships.
- Scatterplot generation to visualize initial data patterns.

### Model Building:
- Variable selection procedures to identify the most significant predictors.
- Transformation considerations for improving model fit (if necessary).

### Diagnostics:
- Residual analysis to assess model accuracy.
- Outlier detection using measures like Cook's distance and leverage.
- Influence measures to identify data points that unduly affect model results.

### Model Refinement:
- Iterative outlier handling to improve model robustness.
- Use of weighted regression when appropriate to mitigate the impact of influential observations.

### Validation:
- Normality tests to ensure residuals follow an appropriate distribution.
- Homoscedasticity checks to verify constant variance of residuals.
- Independence verification to confirm that residuals are uncorrelated.

---

## Technical Implementation

The analyses leverage standard SAS procedures to ensure a rigorous approach:

- `PROC REG`: Used for regression modeling.
- `PROC CORR`: For correlation analysis to explore relationships between variables.
- `PROC UNIVARIATE`: For normality testing of residuals.
- `PROC SGSCATTER`: For generating diagnostic scatterplots.
- `PROC GPLOT`: For bubble plots to visualize influence measures and leverage.

---

## Data Files

- Data for each analysis is included in SAS's `datalines` format.
- Ensure the data is properly loaded before running the analyses.

## Running the Analyses

- Open the appropriate SAS script in SAS Studio or your SAS environment.
- Run the code sequentially as presented in the repository.

## Diagnostic Plots

- Refer to the diagnostic plots generated during each step to guide model refinement and decision-making.

## Key Lessons

- **Iterative Diagnostics**: The importance of continuously refining models by addressing issues such as multicollinearity, outliers, and residual violations.
- **Outlier Handling**: Trade-offs involved in removing outliers versus retaining them, and their impact on model accuracy.
- **Multicollinearity**: Understanding the challenges posed by high correlations between predictors and the steps to mitigate them.
- **Model Selection**: Using stepwise selection methods and forward/backward procedures to optimize models based on the data and context.

## Conclusion

This repository serves as a comprehensive resource for performing regression analysis in SAS, providing both practical implementation and insight into statistical concepts such as multicollinearity, outlier detection, and model validation. The provided analyses are valuable for those seeking to understand and apply regression techniques in a variety of real-world scenarios.

## License

This project is licensed under the **MIT License**.  
See the `LICENSE` file for details.

