# Developers_Hub-Loan_default_Risk-Internship-task-
Data Science &amp;amp; Analytics internship tasks completed for the DevelopersHub Corporation internship program (June-15 July ,2026).

# Loan Default Risk & Decision Cost Optimization

This repository contains the end-to-end Python implementation for **Task 4: Loan Default Risk Classification and Cost Optimization**, completed as a core submission for the Advanced Data Science Internship at DevelopersHub Corporation.

##  Project Objective
The primary business goal is to build a high-accuracy classification pipeline capable of identifying high-risk loan applicants. Unlike standard machine learning pipelines that optimize solely for general metrics (like accuracy), this project applies **Cost Optimization** analysis to align classification outputs with realistic bank default balance sheets, finding a threshold that minimizes total business losses.

##  Business Loss Logic
Standard models use a default threshold of $0.50$, which assumes all error types are identical. In banking:
- **False Positive Cost ($5,000):** Declining a reliable applicant results in loss of potential interest revenue.
- **False Negative Cost ($50,000):** Approving an applicant who defaults causes a high balance sheet loss.
- This model optimizes prediction thresholds to reduce total operational loss.

## 🛠️ Technology Stack
- **Languages:** Python 3.10+
- **Machine Learning Frame:** Scikit-Learn, Pandas, NumPy
- **Visualizations:** Matplotlib, Seaborn
- **Development Tool:** Google Colab / Jupyter Notebooks

## Workflow Steps

1. **Exploratory Data Analysis (EDA):**
   - Assessed massive balance-sheet imbalance rates where defaults occupy a minor portion of the overall applicant pool.
2. **Preprocessing & Encoding:**
   - Cleaned demographic and contractual features.
   - Encoded string categorical variables using `LabelEncoder`.
   - Scaled structural distributions using `StandardScaler`.
3. **ML Pipeline Training:**
   - Evaluated a **Logistic Regression** baseline.
   - Built a high-capacity **Random Forest Classifier** with specialized class weights.
4. **Cost-Curve Optimization Optimization:**
   - Swept classifier prediction probability bounds across a spectrum of $[0.01, 0.99]$ to isolate the exact point minimizing financial loss.

##  Key Results & Strategic Insights

- **Operational Impact:** By shifting the classification threshold to its optimal value, the system reduces bank financial risk and limits write-offs from missed default alerts.
- **Visual Analysis:** Included interactive cost-curve visualizations showing how extreme model bounds ($p \approx 0$ or $p \approx 1$) impact standard operational efficiency.

##  How to Run
1. Clone this repository:
   ```bash
   git clone [https://github.com/your-username/loan-default-cost-optimization.git](https://github.com/your-username/loan-default-cost-optimization.git)
   
