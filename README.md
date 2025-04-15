NHANES-Based Observational Study: Impact of Depression on Obesity Outcomes Among U.S. Adults

Overview

This project analyzes the relationship between depression and obesity outcomes among U.S. adults using data from the National Health and Nutrition Examination Survey (NHANES) 2021–2023 dataset. The primary aim of the study is to evaluate how depression influences obesity (BMI ≥ 30) in adults, employing causal inference methods such as Propensity Score Matching (PSM), Inverse Probability of Treatment Weighting (IPTW), and covariate adjustment.

Objective

The main objectives of this project are:
	•	To assess the relationship between depression and obesity outcomes.
	•	To use real-world data from NHANES to investigate potential causal effects.
	•	To apply different statistical methods (PSM, IPTW, covariate adjustment, and causal forests) to estimate treatment effects and compare results.

Data

The study uses data from NHANES 2021–2023. The dataset includes variables such as:
	•	Demographics: Age, gender, race/ethnicity, education, and household size.
	•	Health Indicators: Depression screening scores (PHQ-9), obesity status (BMI), and other relevant health measures.
	•	Socioeconomic Status: Poverty ratio and related variables.

The data were pre-processed to clean missing values, encode categorical variables, and standardize numerical features. The analysis focuses on adults aged 18 and older.

Methodology

Propensity Score Matching (PSM)

PSM was used to match treated (depressed) and control (non-depressed) groups based on their propensity scores, which were estimated using logistic regression. This method helps balance the covariates between the two groups to reduce confounding biases.

Inverse Probability of Treatment Weighting (IPTW)

IPTW was used to weight the observations by the inverse of their propensity score. This method helps adjust for confounding by creating a pseudo-population where the treatment assignment is independent of the covariates.

Covariate Adjustment

An OLS regression model was fitted with covariate adjustment to estimate the effect of depression on obesity outcomes. Covariates such as age, gender, race/ethnicity, and socioeconomic status were included in the model.

Sensitivity Analysis

To assess the robustness of the findings, sensitivity analyses using different matching methods (e.g., IPTW) and model specifications were conducted.

Results

The results of the analysis provide insights into the potential relationship between depression and obesity outcomes in the U.S. adult population:
	•	ATT (Average Treatment Effect on the Treated): The treatment effect of depression on obesity was estimated using multiple causal inference methods.
	•	OLS Regression: The relationship between depression and obesity was explored with and without covariate adjustment.
	•	Statistical Significance: Sensitivity analyses were performed to test the robustness of the results.

Files in the Repository
	•	Data Cleaning and Pre-processing: Code to clean and preprocess the NHANES data.
	•	Matching Methods: Code for implementing Propensity Score Matching (PSM) and Inverse Probability of Treatment Weighting (IPTW).
	•	Causal Inference: Implementation of causal inference models such as covariate adjustment and causal forests.
	•	Results and Plots: Outputs, including statistical results, plots, and model diagnostics.

Requirements
	•	Python 3.x
	•	Libraries:
	•	pandas
	•	numpy
	•	matplotlib
	•	seaborn
	•	statsmodels
	•	scikit-learn
	•	causalml (for causal forests)
	•	Jupyter Notebook
