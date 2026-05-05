# To What Extent Does Income Impact Hypertension? 
### *A Mediation Analysis of Lifestyle and Socioeconomic Factors*

## 📌 Project Overview
This research project investigates the "Socioeconomic Gradient of Health" using a dataset of **253,680 records** from the CDC's Behavioral Risk Factor Surveillance System (BRFSS). 

The primary goal was to answer: **To what extent do dietary habits and physical activity mediate the link between household income and high blood pressure?**

## 🕵️ The "Data Detective" Discovery
A critical milestone of this project was identifying and explaining a demographic anomaly during the Exploratory Data Analysis (EDA) phase:

*   **The Anomaly:** Initial visualizations showed a non-linear "spike" in hypertension at **Income Level 2**, making it appear unhealthier than Level 1.
*   **The Investigation:** By profiling the mean age across income brackets, I discovered that **Income Level 2 is significantly older** on average than Level 1.
*   **The Conclusion:** This proved that raw health outcomes were being **confounded by age**. This insight justified the use of Age and BMI as mathematical controls in the final model to isolate the "pure" impact of income-based lifestyle choices.

## 📊 Key Research Findings
The study utilized **Chi-Square Tests of Independence** and **Multivariate Logistic Regression** to quantify the "extent" of these relationships.

### 1. The Socioeconomic "Staircase"
While health outcomes were messy due to age, **behavioral mediators** followed a perfect linear staircase:
*   **Physical Activity:** Showed the strongest link to income ($\chi^2 = 10,442$), suggesting that financial status is the primary gatekeeper for exercise access.
*   **Dietary Habits:** Both Fruit and Vegetable consumption increased consistently with every step up the income scale.

### 2. Final Risk Model (Odds Ratios)
After mathematically controlling for **Age** and **BMI**, the model revealed exactly how much each factor protects against hypertension:
*   **Physical Activity:** Reduces risk by **18.4%** (OR: 0.816).
*   **Fruit Intake:** Reduces risk by **13.2%** (OR: 0.868).
*   **Vegetable Intake:** Reduces risk by **10.2%** (OR: 0.897).
*   **Independent Income Effect:** Every increase in income bracket provides a **9.7%** risk reduction, even after diet and exercise are accounted for.

## 🛠️ Tech Stack & Methodology
*   **Language:** Python (Pandas, NumPy, Scipy)
*   **Environment:** Google Colab
*   **Visualization:** Seaborn, Matplotlib (including Forest Plots and Heatmaps)
*   **Statistical Modeling:** Statsmodels (Multivariate Logistic Regression)

## 📁 Repository Structure
*   `Hypertension_Research.ipynb`: The complete Google Colab notebook.
*   `data/`: Processed subset of the CDC BRFSS dataset.
*   `images/`: Forest plots and EDA visualizations.

---
*This project demonstrates the transition from Descriptive Analytics (EDA) to Inferential Modeling, providing a transparent, evidence-based answer to a complex public health question.*
