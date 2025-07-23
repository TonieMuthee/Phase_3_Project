# SyriaTel Customer Churn Prediction

## Overview
This project applies machine learning to predict customer churn for SyriaTel, a telecom provider. Churn refers to customers who stop using the service, and reducing it is vital for retaining revenue.

## Business and Data Understanding
**Stakeholder**: SyriaTel’s marketing and customer success teams.

**Business Problem**: High customer churn reduces revenue. The company needs to identify at-risk customers early and take proactive steps to retain them.

**Dataset**:
- 3,333 customer records
- Features: usage statistics, support calls, service plans
- Target: `churn` (0 = stayed, 1 = churned)

## Modeling
We tested multiple models:
1. **Logistic Regression** – baseline model; failed to converge effectively.
2. **Decision Tree** – improved churn recall to 64%.
3. **Random Forest** – final model with best performance:
   - Accuracy: 93%
   - Churn Recall: 60%
   - Churn Precision: 89%

## Evaluation
We prioritized **recall** for churners to ensure fewer at-risk customers are missed. Random Forest provided the best balance of accuracy and recall.

## Conclusion
Tree-based models like Random Forest outperform simpler models in predicting churn. The model is suitable for real-time alerts in CRM systems and proactive retention strategies.

## Recommendations
- Use the final model to flag likely churners.
- Focus on customers with frequent support calls.
- Periodically retrain the model and enhance features with customer feedback.

## Repository Structure
```
.
├── data/                   # (Optional) Raw or processed dataset
├── syriatel_churn_analysis_final.ipynb
├── SyriaTel_Churn_Prediction_Presentation.pptx
├── README.md
```

## Author
**CPA Anthony Njiru**