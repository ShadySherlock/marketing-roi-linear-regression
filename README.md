# marketing-roi-linear-regression
A Machine Learning model predicting marketing ROI and optimizing advertising budgets using Multiple Linear Regression
# 📈 Marketing Mix Modeling & ROI Analyzer

## 🎯 The Business Problem
A retail company is spending heavily across three different advertising channels: **TV, Radio, and Newspaper**. However, the executive team is operating blindly—they do not know which platforms are actually driving consumer purchases, and which are simply draining the budget. 

The goal of this project is to build a Machine Learning model that answers two critical questions for the business:
1. Which advertising platform generates the highest return on investment?
2. If we allocate $X to a specific platform, exactly how many sales will that generate?

---

## 🛠️ Methodology & Tech Stack
To solve this, I applied **Multiple Linear Regression** to analyze the company's historical marketing data and determine the exact statistical impact of each channel on overall sales volume.
* **Language:** Python 3.x
* **Libraries:** Pandas, NumPy, Scikit-Learn, Matplotlib, Seaborn
* **Validation:** 80/20 Train-Test Split to ensure the model generalizes to unseen future data without overfitting.

---

## 📐 The Mathematical Model & Evaluation
The algorithm solved for the optimal coefficients in the following multivariate equation: 
`Sales = β0 + (β1 × TV) + (β2 × Radio) + (β3 × Newspaper)`

**Learned Parameters:**
* **Intercept (Base Sales):** 2.97
* **TV Coefficient:** 0.044
* **Radio Coefficient:** 0.189
* **Newspaper Coefficient:** -0.001

**Model Accuracy:**
Tested against 20% of the dataset withheld during training, the model achieved an **R-Squared (R²) score of 0.899**. This means the model successfully explains ~90% of the variance in sales purely based on the ad spend features, proving it is highly accurate for future forecasting.

---

## 💡 Key Business Insights & Actionable Recommendations

By translating the mathematical coefficients back into business metrics, I uncovered the exact ROI (units sold per `$1,000` spent) for each platform. 

### 1. Radio is the Most Efficient Channel 🟢
With a coefficient of 0.189, every `$1,000` invested in Radio yields roughly **189 extra units sold**. This is the highest ROI of any platform.

### 2. TV Drives Volume, But at a Lower ROI 🔵
TV advertising has a reliable, positive correlation with sales (**45 extra units per `$1,000`**). While the ROI is lower than Radio, it is highly scalable for generating bulk volume.

### 3. Newspaper Spend Should Be Halted 🔴
The coefficient for Newspaper advertising is virtually zero. Visually and mathematically, it provides no measurable lift in sales. 

**🚨 Final Executive Recommendation:** 
The company should immediately halt all spending on Newspaper advertising. Those funds should be reallocated into Radio to maximize quarterly revenue and overall sales.
