# Neural Networks — Business Applications

This project applies neural networks to real business problems, combining a manual neural-network illustration with classification and regression models. The focus is on how neural networks learn, how architecture choices affect generalization, and how results translate into business decisions.

Two core use cases are covered:
1. Credit card usage (manual neural network forward pass)
2. Customer response prediction using neural networks

---

## Credit Card Usage — Neural Network Illustration

An Excel worksheet demonstrates **one complete forward pass** through a simple neural network for predicting credit card usage.

Inputs:
- **Years**: number of years the customer has been with the bank  
- **Salary**: customer salary (in thousands)

Target:
- **UsedCredit**  
  - 1 = customer carried a credit card balance  
  - 0 = customer paid balances in full  

The worksheet shows:
- Randomly initialized weights and bias
- Weighted sum (z)
- Output using **logistic activation**
- Output using **ReLU activation**
- Final prediction and correctness

This illustration highlights how:
- Activation functions change network output
- The same weights can lead to different predictions depending on activation choice
- Neural networks begin with random behavior before learning from error feedback

---

## Neural Network Learning

Neural networks improve through **error feedback**:
- Predictions are compared to actual outcomes
- Errors are propagated backward
- Weights are updated using gradient-based optimization
- Repeated passes reduce prediction error

This process explains how neural networks evolve from random predictions to meaningful models.

---

## Direct Mail Response — Classification Model

A neural network classifier is built to predict whether airline customers will respond to a direct-mail offer.

Key steps:
- Categorical variables converted to dummy variables
- Numeric predictors scaled to [0, 1] using MinMaxScaler (`clip=True`)
- Binary dummy variables left unscaled
- Data split into training (60%) and validation (40%)

Models evaluated:
- One hidden layer with **5 nodes**
- One hidden layer with **1 node**

Findings:
- The 5-node network captured meaningful patterns while generalizing well
- The 1-node network was too simple and underfit the data
- Training and validation lift charts were similar, indicating good generalization

**Business interpretation of lift:**  
The top decile of scored customers contains a much higher proportion of responders than random targeting, making the model useful for focused marketing.

---

## Regression Model — Price Prediction

A neural network regressor predicts a continuous outcome using structured inputs.

Approach:
- Separate scaling for inputs and output variables
- Predictions inverse-transformed back to original units
- Architectures compared:
  - Single hidden layer with 2 nodes
  - Single hidden layer with 5 nodes
  - Two hidden layers with 5 nodes each

Results:
- Increasing complexity reduced training error
- Validation error increased with larger networks
- The simplest network generalized best

This shows how overfitting can occur when neural networks become unnecessarily complex.

---

## Model Selection & Generalization

Key lessons:
- Validation performance matters more than training accuracy
- Simpler neural networks often generalize better
- Neural networks require careful scaling and tuning
- More layers and nodes do not guarantee better results

---

## Files Included

- **Credit Card Use.xlsx** — Manual neural network forward-pass illustration  
- **Jupyter Notebook** — Neural network classification and regression models  

---

## Tools Used

- Python
- scikit-learn (`MLPClassifier`, `MLPRegressor`)
- MinMaxScaler
- pandas, numpy
- dmba utilities
- Excel (manual neural network illustration)

---

## Key Takeaways

- Neural networks learn through error correction
- Activation functions matter
- Overfitting is a real risk with complex architectures
- Validation data is essential for trustworthy models
- Neural networks can support real business decisions when used carefully

---

## Contact

- **Portfolio:** https://hashimgilani.github.io  
- **LinkedIn:** https://linkedin.com/in/syedhashimgilani  
- **Email:** hashimgilani331@gmail.com  

⭐ Thanks for checking out this neural networks project.
