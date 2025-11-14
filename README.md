# Marketing-A-B-Testing
A/B test analysis of a marketing campaign to determine statistical significance and provide a data-driven business recommendation.

**Overview
This project is a complete analysis of a sample A/B test for a marketing campaign. The primary goal was to determine whether a new "ad" (treatment) provided a statistically significant improvement in user conversion rate compared to the existing "psa" (control).

This analysis demonstrates a practical application of data-driven decision-making, translating raw data from a marketing_AB.csv file into an actionable business recommendation.

**Project Goals
Clean and prepare the raw test data, ensuring data integrity.

Define the null and alternative hypotheses.

Perform a two-proportion z-test to determine statistical significance.

Provide a clear, data-driven recommendation for non-technical stakeholders.

**Tech Stack
Python: The core language for the analysis.

Jupyter Notebook: For iterative analysis and documentation.

Pandas: Used for data loading, cleaning, and manipulation.

Statsmodels: Used to perform the statistical (two-proportion z-test).

**The Dataset
The dataset used is a public A/B testing dataset from Kaggle. It contains user IDs and information on which test group they were in (ad or psa) and whether they converted.

[Link to Dataset] (e.g., https://www.kaggle.com/datasets/faviovila/marketing-ab-testing)

Analysis Workflow
My process for this analysis followed these key steps:
1. Data Cleaning & PreparationI first loaded the marketing_AB.csv file into a Pandas DataFrame. The key cleaning step was to check for and remove any users who may have been exposed to both the ad and psa versions, as this would contaminate the results.
2. Defining the HypothesisBefore running the test, I established a clear hypothesis.Null Hypothesis ($H_0$): There is no difference in conversion rate between the 'psa' (control) and 'ad' (treatment) groups.Alternative Hypothesis ($H_A$): There is a significant difference in conversion rate between the two groups.
3. Statistical TestI separated the data into control and treatment groups and calculated their respective conversion rates. I then used the proportions_ztest function from the statsmodels library to compare the two proportions. This test yielded a z-statistic and, most importantly, a p-value.

Final Analysis & Recommendation
The final step was to translate the statistical findings into a clear, non-technical recommendation.

Executive Summary: A/B Test for 'Ad' Campaign
  Goal: We tested a new 'ad' (Treatment) against the current 'psa' (Control) to see if it improved user      conversion.

Findings
Control Rate (psa): 1.75%
Treatment Rate (ad): 2.55%
Statistical Significance: The test was statistically significant (p = 0.0001). This means the 0.8% absolute lift in conversion is not due to random chance.

Recommendation
Launch the 'ad' version.The test provides strong evidence that the 'ad' campaign is more effective at converting users than the 'psa'. This change is projected to increase our overall conversions.
