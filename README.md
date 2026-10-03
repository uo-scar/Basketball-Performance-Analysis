# Basketball-Performance-Analysis
Statistical investigation of factors associated with basketball scoring using Rivers Hoopers match data.

# 🏀 Statistical Investigation of Basketball Scoring

### Rivers Hoopers Basketball Club Case Study

An applied statistical analysis investigating the relationship between selected team performance indicators and points scored across recorded Rivers Hoopers matches.

**Focus:** Statistical Analysis · Correlation · Multiple Linear Regression · Model Diagnostics

---

## The Question

Basketball scoring is influenced by multiple aspects of team performance, but it is easy to assume that a statistic matters simply because it appears intuitively important.

I wanted to test that assumption.

> **To what extent can selected team performance indicators explain variation in points scored?**

---

## Data

The analysis used **28 recorded match observations** from Rivers Hoopers.

| Variable      | Role      |
| ------------- | --------- |
| Points Scored | Outcome   |
| FG%           | Predictor |
| FT%           | Predictor |
| 3P%           | Predictor |
| Rebounds      | Predictor |
| Assists       | Predictor |
| Turnovers     | Predictor |

The predictors represent different aspects of shooting efficiency, possession, playmaking and ball control.

---

## Analytical Approach

I approached the question in stages:

**1. Descriptive statistics**
To understand the typical performance and variation in the recorded matches.

**2. Pearson correlation**
To examine the direction and strength of the individual linear relationships with points scored.

**3. Multiple linear regression**
To examine the predictors simultaneously and determine how much variation in points scored the model could account for.

**4. Model diagnostics**
To assess residual independence, multicollinearity and potentially influential observations before interpreting the regression model.

---

## What Did the Data Show?

The team averaged **75.57 points per match**, with scores ranging from **56 to 93**.

### Correlation with Points Scored

| Predictor |         r | p-value |
| --------- | --------: | ------: |
| FG%       |     0.112 |   0.571 |
| FT%       |     0.218 |   0.264 |
| 3P%       | **0.354** |   0.065 |
| Rebounds  |     0.142 |   0.472 |
| Assists   | **0.322** |   0.095 |
| Turnovers |    -0.212 |   0.279 |

The strongest individual positive relationship was between **3P% and Points Scored (r = 0.354)**, followed by assists (**r = 0.322**).

However, **none of the individual correlations reached the 5% significance level**.

This distinction mattered: an observed relationship is not automatically statistically supported.

---

## What Happened in the Regression Model?

When the six predictors were considered simultaneously:

| Measure       |    Result |
| ------------- | --------: |
| R             |     0.655 |
| R²            |     0.428 |
| Adjusted R²   |     0.265 |
| F-statistic   |     2.624 |
| Model p-value | **0.047** |

The model accounted for approximately **42.8% of the observed variation in points scored**.

The overall regression model was statistically significant at the 5% level.

Within the fitted model:

* **FT%:** B = 0.471, p = 0.024
* **Rebounds:** B = 0.689, p = 0.021

These two predictors were statistically significant at the 5% level after the other variables were considered simultaneously.

Interestingly, **3P% had the strongest simple correlation with scoring but was not statistically significant in the multiple regression model**.

This difference illustrates why examining variables individually can provide only part of the picture.

---

## Model Checks

I did not interpret the regression results based on significance alone.

The analysis also examined:

* **Durbin–Watson = 2.338** for residual independence
* **VIF = 1.482–3.508** for potential multicollinearity
* **Maximum Cook's Distance = 1.792** for potentially influential observations
* Residual normality using **Kolmogorov–Smirnov and Shapiro–Wilk tests**

These checks provided additional context for interpreting the fitted model.

---

## What I Learned

The main lesson from this analysis was **not simply which basketball statistic was significant**.

It was learning to distinguish between:

**What the data suggests**
and
**what the statistical evidence supports.**

A positive correlation does not automatically establish significance or causation. Likewise, a predictor's relationship with scoring can change when other variables are considered simultaneously.

The project therefore became an exercise in **statistical reasoning rather than simply producing numbers**.

---

## Limitations

The analysis was based on only **28 recorded matches**, so the findings should be interpreted within the available data.

The study was observational and therefore identifies **statistical associations, not causal effects**.

The results should also not automatically be generalized to other teams, competitions or populations.

---

## Conclusion

This project applied statistical thinking to a real basketball performance question using descriptive statistics, correlation, multiple linear regression and diagnostic checks.

Rather than assuming which performance indicators mattered, I used the available data to investigate the relationships and then interpreted the evidence within its limitations.

> **The most valuable outcome was learning to ask not only “What does the data show?” but also “How strongly does the evidence support that conclusion?”**

---

### Tools

**SPSS · Microsoft Excel · Statistical Analysis · Multiple Linear Regression**

### Project Context

Final-year undergraduate statistical research project
**Federal University of Technology, Owerri**
