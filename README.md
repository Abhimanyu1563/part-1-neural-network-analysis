# Neural Network Fundamentals and Training Behavior Analysis

## Overview
This project builds and analyzes a neural network model to predict customer churn using a structured dataset. The workflow includes data exploration, preprocessing, model building, training, evaluation, and hyperparameter experimentation.

---

## Dataset Summary
- Total samples: 2000  
- Features: 17  
- Target variable: `churn` (binary: 0 = no churn, 1 = churn)  
- No missing values present  
- Dataset is highly imbalanced (very few churn cases)

---

## Task 1: Dataset Understanding
Basic exploration was performed including:
- Shape of dataset
- Data types of features
- Missing value check
- Statistical summary
- Target variable distribution

Observation: The dataset is highly imbalanced, which affects model performance.

---

## Task 2: Data Preprocessing
- Categorical variables encoded
- Numerical features scaled
- Dataset split into training and testing sets (80-20)

---

## Task 3: Model Building
A feed-forward neural network was implemented using Keras:
- Input layer
- Hidden layers with ReLU activation
- Output layer with Sigmoid activation (binary classification)
- Loss: Binary Crossentropy
- Optimizer: Adam

---

## Task 4: Training and Evaluation
- Model trained for 30 epochs
- Achieved high accuracy (~98%)

However:
- Model failed to detect churn cases due to class imbalance
- Confusion matrix showed all predictions as non-churn

---

## Task 5: Hyperparameter Experiments

Three experiments were conducted:

1. **Baseline Model**
   - High accuracy but no churn detection

2. **Class Weights**
   - Improved recall and F1-score for churn
   - Slight drop in accuracy

3. **Deeper Model**
   - Moderate improvement but less effective than class weighting

### Key Insight:
Class imbalance handling is more important than increasing model complexity.

Comparison table is available in the `results/` folder.

---

## Task 6: Final Reflection

- Weights and biases determine how input features influence predictions  
- Activation functions introduce non-linearity, enabling complex learning  
- Learning rate affects convergence speed and stability  
- Model initially failed due to class imbalance, not underfitting  

### Final Insight:
A model with high accuracy can still be ineffective if it ignores the minority class.

---

## Folder Structure
