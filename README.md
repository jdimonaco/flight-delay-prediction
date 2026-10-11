🚀 **Project Overview**

The objective of this project is to predict whether a flight will be delayed using classification models trained on historical flight data. Delays can significantly impact both passenger experience and cargo logistics, leading to financial losses and disrupted operations. Early prediction enables airlines and logistics providers to make proactive, data-driven decisions.

🧠 **Models Used**

A progressive modelling approach was adopted:

**Decision Tree:** Used as a baseline for initial feature analysis and interpretability.

**Random Forest:** Selected as the final model due to its strong performance, interpretability, and operational practicality.

**XGBoost:** Achieved the highest accuracy and ROC-AUC but was not selected due to its complexity and lower interpretability.

✅ **Final Model: Random Forest**

Although XGBoost slightly outperformed other models in metrics, the Random Forest model was selected for the following reasons:

- Strong predictive performance (Accuracy: 73.8%, ROC-AUC: 0.84), with the highest precision of the three models (93.6%), so flagged flights are almost always genuinely at risk
- Clear feature importance output, aiding stakeholder understanding and decision-making
- Proportionate to a small dataset: robust with modest tuning, and simple to retrain and maintain
- Easier hyperparameter tuning, reducing risk in production environments
- Improved stakeholder trust through explainability and transparency

📊 **Key Features Engineered**

- Flight Duration (planned, including ground time)
- Cargo Density
- Departure Time Categories (e.g., Morning, Afternoon), based on the planned departure time

These features enhance the model's ability to capture operational complexity and real-world factors contributing to delays.

📈 **Evaluation Metrics**

- Accuracy
- Precision / Recall / F1-Score
- ROC-AUC
- Confusion Matrix
- Learning Curves
- Cross-Validation Accuracy Distribution

🔍 **Key Takeaways**

All three models achieved realistic performance (74–76% accuracy) using only information available before departure.

Random Forest was selected for its balance between accuracy, interpretability, and efficiency.

Feature importance enabled insights into key drivers of delays, such as flight duration, distance, and cargo weight.

XGBoost achieved the highest metrics but required more complex tuning and lacked interpretability for business users.

⚠️ **Considerations**

While the results are encouraging, it is important to consider:

- An earlier version of this project reported over 99% accuracy due to data leakage (features that are only known after a delay has occurred). These were removed and all results re-run; see the version note at the top of the notebook.
- At the default threshold, Random Forest catches around half of delayed flights. The threshold can be adjusted if missing a delay is more costly than a false alarm.
- External validation is recommended for future work to assess generalisability.
- Continuous model monitoring and retraining should be implemented in live environments.

📌 **Disclaimer**

This project was adapted for research purposes only, using synthetic data to simulate real-world flight and cargo scenarios. Airline and airport codes have been anonymised. The model and its predictions are not intended for operational use without further validation. Accuracy and outcomes depend on the structure and assumptions within the dataset, and may not reflect real-world conditions.
