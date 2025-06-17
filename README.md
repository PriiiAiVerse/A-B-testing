#  A/B Testing Project — Do Ads Help Increase User Conversions?

##  Introduction

This project investigates whether displaying advertisements increases user conversions using **A/B testing**. The dataset is divided into two groups:

- **"ad" group**: Users who saw ads
- **"no_ad" group**: Users who did not see ads

The objective is to determine whether ad exposure had a statistically significant impact on user behavior — specifically, on **conversion rate**.

---

##  Proposed Solution
**A/B Testing** was chosen as the core method for comparing conversion performance between the two groups.

---

##  Prerequisites & Learning Goals

To understand or replicate this project, you should be familiar with:

- Basic statistics (mean, variance, distributions)
- Hypothesis testing, p-values
- A/B Testing concepts
- Python libraries: `pandas`, `matplotlib`, `seaborn`, `scipy`
- Data visualization and result interpretation

---

##  What is A/B Testing?

A/B Testing is a controlled experiment comparing two versions of something to evaluate which performs better.

In this project:
- **Group A (Control)**: Users who did **not** see ads
- **Group B (Treatment)**: Users who **did** see ads

The goal is to assess whether **Group B** converted at a significantly higher rate than **Group A**.

---

##  A/B Testing Workflow

### 1. Define the Hypotheses:
- **Null Hypothesis (H₀):** Ads do not affect conversion rates.
- **Alternative Hypothesis (H₁):** Ads increase conversion rates.

### 2. Experiment Design
- Users were randomly assigned to one of the two groups.
- Only Group B was exposed to advertisements.

### 3. Measure Outcomes
- Did users convert (True/False)?

### 4. Statistical Testing
- Mann-Whitney U Test was used due to non-normal data.
- p-value interpretation guided our conclusion.

---

##  Statistical Concepts Applied

### 🔹 Hypothesis Testing
A formal process for making decisions using data. We test a null hypothesis and seek statistical evidence to reject it.

### 🔹 P-Value
Probability that the observed effect is due to chance. A **p-value < 0.05** typically means results are statistically significant.

### 🔹 T-Test (Not used here)
Compares means of two groups assuming normal distribution. In this case, the data **was not normal**, so an alternative was used.

### 🔹 Mann-Whitney U Test
A non-parametric test comparing medians of two groups. Used here as a robust alternative to the t-test.

---

##  Dataset Overview

| Column Name      | Description                                             |
|------------------|---------------------------------------------------------|
| `user_id`        | Unique identifier for each user                         |
| `test_group`     | Indicates if the user saw ads (`ad`) or not (`no_ad`)  |
| `converted`      | Whether the user converted (True/False)                 |
| `total_ads`      | Number of ads the user saw                              |
| `most_ads_day`   | Day of the week the user saw the most ads               |
| `most_ads_hour`  | Hour of the day the user saw the most ads               |


##  Statistical Test Result
Test Used: Mann-Whitney U Test
P-Value: 1.0

##  Interpretation:
The p-value is very high (≫ 0.05), so we fail to reject the null hypothesis.

No statistically significant difference in conversion between groups.

##  Summary of Findings
# Analysis Element	Result
  - Group Balance	Fairly equal "ad" vs. "no_ad" user count
  - Conversion Outcome	More users did not convert
  - Ads by Day/Hour	Most ads shown on Monday/Tuesday, around 8 PM–10 PM
  - Conversion Impact	Ads did not significantly influence conversion
  - Statistical Test	Mann-Whitney U → No significant difference
  - Visual + Statistical	Both confirm the same story: ads had no measurable effect

## Final Conclusion
-  Both visual analysis and statistical testing clearly indicate that showing ads did not lead to higher conversions in this dataset.

Result: No measurable uplift from ad exposure.
This highlights the importance of A/B testing in validating marketing strategies before scaling.

## Tech Stack
  - Python 3.x

  - pandas

  - numpy

  - matplotlib / seaborn

  - scipy.stats

## Folder Structure
```markdown

├── ab_ads_analysis.ipynb
├── ads_dataset.csv
├── README.md
└── plots/summaryPDF
```
  
##  Future Work

- Perform power analysis for sample size calculation

- Try other metrics like time-on-site or click-through rate

- Test multi-variate changes (A/B/n testing)

👤 Author
Priti Kumari



