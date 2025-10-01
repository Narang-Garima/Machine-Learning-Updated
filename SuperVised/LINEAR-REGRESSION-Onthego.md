# Regression Types & Concepts – Interview Perspective

Regression is about predicting a **continuous numerical outcome** based on input variables.  
Think of it as drawing a line (or curve) that best fits your data points.

---

## 1. Simple Regression (Linear Regression)
- **Definition:** Uses **one input variable** to predict one output.
- **Example:** Predict a student’s score based on hours studied.
- **Visual:** A straight line through a scatter of points.
- **Interview Tips:**
  - Can be represented as `Y = b0 + b1*X` where `b0` is the intercept and `b1` is the slope.
  - Assumes **linearity**, **homoscedasticity** (constant variance), and **independence** of errors.
  - Can be evaluated using **MAE, MSE, RMSE**, and **R²**.

---

## 2. Multiple Regression
- **Definition:** Uses **two or more input variables** to predict an output.
- **Example:** Predict a student’s score based on hours studied, hours slept, and attendance.
- **Visual:** Plane or hyperplane in higher dimensions.
- **Interview Tips:**
  - Formula: `Y = b0 + b1*X1 + b2*X2 + … + bn*Xn`
  - Helps capture **combined effects** of multiple factors.
  - Beware of **multicollinearity** (high correlation between inputs) – can inflate coefficients.
  - Use **Adjusted R²** to see if adding variables really improves the model.

---

## 3. Polynomial Regression
- **Definition:** Fits a **curve** instead of a straight line.
- **Example:** Predict plant growth where growth accelerates and then slows.
- **Visual:** Curve bending to fit the data.
- **Interview Tips:**
  - Captures **non-linear relationships**.
  - Overfitting risk is higher with high-degree polynomials.
  - Feature scaling or regularization may be needed.

---

## 4. Underfitting vs Overfitting
- **Underfitting:** Model too simple; fails on training & new data.  
  - Example: Straight line for very wiggly dataset.
  - **Interview angle:** Explain bias-variance tradeoff – underfit = high bias.
- **Overfitting:** Model too complex; memorizes training data, fails on new data.  
  - Example: Complex curve passing through every training point.
  - **Interview angle:** Overfit = high variance. Use **cross-validation** to detect.
- **Goal:** Balance complexity → good generalization.

---

## 5. Error Metrics
**How we measure model performance:**
- **MAE (Mean Absolute Error):** Average absolute difference between predicted & actual values.  
  - Easy to interpret.
- **MSE (Mean Squared Error):** Average squared differences; penalizes large errors more.
- **RMSE (Root Mean Squared Error):** Square root of MSE; same units as target.
- **Interview tip:** Always mention **context & units** when interpreting these metrics.

---

## 6. R² & Adjusted R²
- **R²:** Fraction of variance in target explained by model.  
  - 1 = perfect fit, 0 = explains nothing.
- **Adjusted R²:** Penalizes unnecessary variables in multiple regression.  
  - Useful in multiple regression to check if extra features help.
- **Interview tip:** Know when **Adjusted R² can decrease** if irrelevant variables are added.

---

## 7. Regularization (Bonus for Interviews)
- **Why needed:** Prevent overfitting in complex models.
- **Types:**
  - **Ridge Regression (L2):** Shrinks coefficients; keeps all variables.
  - **Lasso Regression (L1):** Shrinks and can zero-out coefficients (feature selection).
- **Interview angle:** “When would you use Ridge vs Lasso?” → Ridge = all features important, Lasso = select important ones.

---

## ✅ Summary – One Sentence
- **Regression Types:** Simple, multiple, polynomial → drawing line/curve through data.  
- **Underfitting vs Overfitting:** Too simple vs too complex.  
- **Error Metrics:** MAE/MSE/RMSE → measure prediction errors.  
- **Model Fit:** R² & Adjusted R² → measure how well model explains variance.  
- **Regularization:** Ridge/Lasso → control overfitting, improve generalization.
