# AI Autoscaler

## 📌 Project Overview
**AI Autoscaler** is an AI-powered predictive Kubernetes pod scaling solution. It anticipates fluctuating workloads for events such as IPL matches and Amazon sales and preemptively scales the required number of pods 30 minutes in advance. This reduces dropped requests and ensures smooth application performance.

## 🎯 Objectives
- Predict the optimal number of Kubernetes pods needed before an event.
- Minimize response time and prevent over/under-provisioning.
- Utilize AutoML to automate model selection and tuning.
- Evaluate model performance with R² score and RMSE.

## 🚀 Features
- **AI-Based Predictions**: Uses historical traffic patterns to forecast scaling needs.
- **AutoML Integration**: Leverages `H2O AutoML` for model selection and hyperparameter tuning.
- **Error Analysis**: Provides RMSE, MSE, and R² for performance evaluation.
- **Scalability**: Adapts to different event types with fluctuating workloads.

## 🛠️ Tech Stack
- **Programming Language**: Python (Jupyter Notebook)
- **Machine Learning Library**: H2O.ai AutoML
- **Data Processing**: Pandas, NumPy
- **Deployment**: Kubernetes (future scope)

## 📊 Model Training Process
1. **Data Collection**: Use historical event traffic data (e.g., IPL matches from 2021-2024).
2. **Preprocessing**: Clean and format data, ensuring features like date, time, and team popularity are included.
3. **Feature Engineering**: Selecting independent variables (X) and target variable (Y - `pods_required`).
4. **Model Training**: Utilize `H2OAutoML` while excluding undesired algorithms (e.g., Deep Learning, Stacked Ensemble, GLM).
5. **Evaluation**:
   - RMSE (Root Mean Squared Error)
   - R² Score
   - Adjusted R² Score (calculated manually)
6. **Prediction**: Predict pod scaling needs on test data (IPL 2025 data).

## 📈 Results
- **Train Data R² Score**: 92.19%
- **Test Data R² Score**: 75%
- **Test RMSE**: 2.59

## 📂 Project Structure
```
AIAutoScaler/
│-- ipl_train_data.csv
│-- ipl_test_data.csv
│── predictions.ipynb
│-- README.md
```

## 🏗️ Future Enhancements
- Deploy as a **Kubernetes Operator** for real-time scaling.
- Incorporate **real-time traffic data** for continuous learning.
- Optimize feature engineering for better accuracy.
- Compare with other ML frameworks like `AutoGluon`.

## 🏁 Conclusion
AIAutoScaler leverages AI to **intelligently predict and optimize Kubernetes pod scaling**, ensuring high availability and cost efficiency during high-traffic events. 🚀

