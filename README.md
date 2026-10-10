# Deep Learning-Based Predictive Maintenance and Anomaly Detection for Industrial Robotic Systems Using Sensor Data using AI4I 2020

## M.Tech Data Science and Artificial Intelligence Project

This project develops an explainable machine-learning framework for predictive maintenance using the AI4I 2020 Predictive Maintenance Dataset.

The objective is to predict machine failure from operational sensor parameters and provide interpretable explanations for the predictions.

---

## Project Workflow

The project was implemented in two phases.

### Phase 1 – Model Development

Phase 1 includes:

- Exploratory Data Analysis (EDA)
- Data preprocessing
- Feature preparation
- Random Forest model
- XGBoost model
- LSTM model
- Model performance comparison
- Selection of XGBoost as the final predictive model

The failure-mode indicator columns (TWF, HDF, PWF, OSF and RNF) were not used as model input features in order to avoid target leakage.

The operational features used for prediction include:

- Product Type
- Air Temperature
- Process Temperature
- Rotational Speed
- Torque
- Tool Wear

### Phase 2 – Model Optimization, Explainability and Demo

Phase 2 extends the selected XGBoost model with:

- Hyperparameter and class-imbalance experiments
- Decision-threshold optimization
- SHAP explainability
- Global feature interpretation
- Individual prediction explanations
- Risk-based maintenance recommendations
- Interactive prediction demonstration

The decision threshold was optimized from 0.50 to 0.45, improving the observed F1-score from approximately 82.93% to 83.87%.

SHAP is used to explain how individual operational features contribute to model predictions.

---

## Implementation Environment

Phase 1 model development was performed using Jupyter Notebook.

The trained XGBoost model was serialized as:

`phase1_xgb.pkl`

For Phase 2, the saved XGBoost model was loaded in Google Colab for SHAP explainability and demonstration. Colab was used to avoid local dependency/environment compatibility issues encountered with SHAP.

This separation also demonstrates a typical machine-learning workflow in which a trained model is saved and subsequently loaded in another environment for explainability and inference.

---

## Repository Files

### `01_EDA_AI4I_Phase1_Model_Development.ipynb`

Contains EDA, preprocessing, model development and comparison of Random Forest, XGBoost and LSTM.

### `01_EDA_AI4I_Phase2_SHAP with demo.ipynb`

Contains Phase 2 analysis, SHAP explainability and the prediction demonstration.

### `phase1_xgb.pkl`

Serialized trained XGBoost model used by the Phase 2 notebook.

### `ai4i2020.csv`

AI4I 2020 Predictive Maintenance Dataset used for model development and evaluation.

---

## Key Result

XGBoost was selected as the primary predictive model based on the experimental comparison.

Threshold optimization improved the F1-score:

- Default threshold (0.50): approximately 82.93%
- Optimized threshold (0.45): approximately 83.87%

The final system combines failure prediction with SHAP-based model explanations to support maintenance decision-making.

---

## Author

**Sanooj Kumar V R**  
M.Tech – Data Science and Artificial Intelligence
PES University
