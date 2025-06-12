# King County Housing Price Prediction

This project implements a deep learning regression model using TensorFlow/Keras to predict housing prices in King County, WA.

---

## Overview

- **Framework**: TensorFlow / Keras  
- **Model Type**: Fully connected feedforward neural network  
- **Task**: Supervised regression  
- **Dataset**: `kc_house_data.csv`  
- **Input Features**: 19 normalized numerical features  
- **Target**: House price (USD)

---

## Workflow

1. Data ingestion and validation using `pandas`
2. Exploratory data analysis (EDA) using `seaborn` and `matplotlib`
3. Feature engineering: dropped irrelevant columns, added `year`, `month`
4. Data normalization with `MinMaxScaler`
5. Train/test split: 70/30
6. Model definition and training
7. Evaluation: MAE, RMSE, explained variance
8. Inference on single sample

---

## Model Details

- **Input**: 19 normalized features  
- **Architecture**:  
  - Dense(19) + ReLU  
  - Dense(19) + ReLU  
  - Dense(19) + ReLU  
  - Dense(19) + ReLU  
  - Dense(1) + ReLU  
- **Optimizer**: Adam  
- **Loss**: Mean Squared Error  
- **Epochs**: 400  
- **Batch Size**: 128  

---

## Performance (on Test Set)

- RMSE ≈ 163,452  
- MAE ≈ 101,088  
- Explained Variance Score ≈ 0.799

---

## Example Inference

```python
# Single House Prediction
Input: 19 normalized values
Output: Predicted price ≈ $289,450  
Actual: $221,900
