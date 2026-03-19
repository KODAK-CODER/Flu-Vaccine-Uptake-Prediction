# Flu Vaccine Uptake Prediction
**Predicting H1N1 and Seasonal Flu Vaccination Status**

## Overview
This project uses Machine Learning to predict whether individuals received the H1N1 and seasonal flu vaccines based on data from the 2009 National H1N1 Flu Survey.

## Business and Data Understanding
**Stakeholder:** Public Health Departments.
**Objective:** To identify key drivers of vaccination behavior to optimize outreach and communication strategies. 
**The Data:** 26,707 survey responses including demographics, health behaviors, and personal opinions.

## Modeling
We followed an iterative approach:
1. **Baseline Model:** A Logistic Regression model provided an interpretable starting point.
2. **Final Model:** A Random Forest Ensemble model was used to capture complex interactions between features like health insurance and doctor recommendations.
*Key Technique:* We used a Scikit-Learn Pipeline to handle missing data and scaling, ensuring no data leakage.

## Evaluation
We used **ROC-AUC** as our primary metric.
- **Baseline AUC:** 0.844
- **Final Model AUC:** 0.845
The model is 84.5% effective at correctly ranking a vaccinated individual higher than a non-vaccinated one.

## Conclusion & Recommendations
- **Doctor Recommendations:** This is the most significant predictor. Public health campaigns should empower physicians with more vaccine resources.
- **Perceived Risk:** High concern correlates strongly with uptake. Educational campaigns should focus on the risks of *not* vaccinating.

## Repository Structure
- `notebook.ipynb`: Data analysis and model building.
- `data/`: Folder containing survey features and labels.
- `presentation.pdf`: Non-technical slide deck.