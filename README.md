# Predicting-Nominal-Power-of-Charging-Stations-in-Germany

## Introduction
This project predicts the nominal power of EV charging stations using factors like operator, number of charging points, plug types, and location. The insights aim to support policymakers, urban planners, and resource allocation for sustainable EV infrastructure development.

## Dataset
- **Size:** 54,162 rows, 15 columns  
- **Key Features:** Operator, operator type, charging points, plug types, power ratings (p1_kw, p2_kw, p3_kw), location details.  
- **Missing Values:** Addressed with probabilistic imputation, median filling, or removal.  

## Preprocessing
- **Dropped Columns:** Irrelevant (e.g., pincode, street).  
- **Handling Missing Values:** Imputed or removed based on feature importance.  
- **Encoding:** Frequency, label, and target encoding for categorical features.  
- **Scaling:** Standardization (numerical) and MinMax scaling (target).  
- **Outlier Handling:** Rare occurrences grouped or dropped.

## Model
- **Architecture:** Fully connected neural network  
  - Input layer: Features as input  
  - Hidden layers: 64-128-64 neurons, ReLU activation, Dropout for regularization  
  - Output layer: Single neuron (regression task)  
- **Loss Function:** Mean Squared Error (MSE)  
- **Optimizer:** Adam  

## Training
1. **Workflow:**  
   - Forward pass → Loss calculation → Backward pass → Weight updates  
2. **Phases:**  
   - Training: Batch updates  
   - Validation: Performance monitoring  
3. **Stopping Criteria:** Fixed epochs or early stopping based on validation performance.  

## Objectives
- Optimize charging infrastructure deployment.  
- Identify key drivers for charging station capacity.  
- Enable data-driven decisions for EV infrastructure growth.  
