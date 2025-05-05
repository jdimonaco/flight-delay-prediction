
🚀**Project Overview**
The objective of this project is to predict whether a flight will be delayed using classification models trained on historical flight data. Delays can significantly impact both passenger experience and cargo logistics, leading to financial losses and disrupted operations. Early prediction enables airlines and logistics providers to make proactive, data-driven decisions.

🧠 ** Models Used **

A progressive modelling approach was adopted:

**Decision Tree:** Used as a baseline for initial feature analysis and interpretability.

**Random Forest:** Selected as the final model due to its strong performance, interpretability, and operational practicality.

**XGBoost:** Achieved the highest accuracy and ROC-AUC but was not selected due to its complexity and lower interpretability.

✅ **Final Model:** Random Forest

Although XGBoost slightly outperformed other models in metrics, the Random Forest model was selected for the following reasons:

High predictive performance (Accuracy: 99.44%, ROC-AUC: 0.999)

Clear feature importance output, aiding stakeholder understanding and decision-making

Lower computational cost and faster training time

Easier hyperparameter tuning, reducing risk in production environments

Improved stakeholder trust through explainability and transparency

📊 **Key Features Engineered**

Flight Duration (including ground time)

Cargo Density

Departure Time Categories (e.g., Morning, Afternoon)

Delay Severity Classification

These features enhance the model’s ability to capture operational complexity and real-world factors contributing to delays.

📈 **Evaluation Metrics**
Accuracy

Precision / Recall / F1-Score

ROC-AUC

Confusion Matrix

Learning Curves

Cross-Validation Accuracy Distribution

🔍 **Key Takeaways**

All three models showed exceptional predictive performance.

Random Forest was selected for its balance between accuracy, interpretability, and efficiency.

Feature importance enabled insights into key drivers of delays, such as cargo weight, flight duration, and departure time.

XGBoost achieved the highest metrics but required more complex tuning and lacked interpretability for business users.

⚠️ **Considerations**

While model performance was strong, it is important to consider:

The high accuracy may be partially due to the dataset structure, which could oversimplify real-world complexity.

External validation is recommended for future work to assess generalisability.

Continuous model monitoring and retraining should be implemented in live environments.
