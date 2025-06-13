# Market Basket Analysis for GiftEase Ltd.

## 📦 Project Overview

This project applies **Market Basket Analysis (MBA)** to transaction data from GiftEase Ltd., a fast-growing online gift retailer. The goal is to uncover hidden patterns in customer purchase behavior and to provide actionable recommendations for cross-selling, product placement, and targeted marketing.

By leveraging the **Apriori algorithm**, this project identifies frequently bought-together products and generates association rules that can directly inform business decisions.

---

## 🗂️ Dataset

- **Source:** [UCI Machine Learning Repository - Online Retail Dataset](https://archive.ics.uci.edu/ml/datasets/online+retail)
- **Description:**  
  The dataset contains over 50,000 transactions from a UK-based online retailer, with fields such as:
  - InvoiceNo
  - StockCode
  - Description (Product Name)
  - Quantity
  - InvoiceDate
  - UnitPrice
  - CustomerID
  - Country

---

## 🚦 Problem Statement

Despite having extensive transaction data, GiftEase Ltd. was not using it to understand which products customers buy together. This led to:
- Missed cross-selling and upselling opportunities
- Ineffective product recommendations
- Generic, non-personalized promotional bundles

**Objective:**  
Use Market Basket Analysis to extract actionable insights from transaction data and enable data-driven marketing and merchandising strategies.

---

## 🔬 Methodology

1. **Data Collection & Cleaning**
   - Removed canceled orders and incomplete records (e.g., missing CustomerID).
   - Filtered for UK-based customers to match GiftEase’s market.

2. **Data Transformation**
   - Reformatted transactions into a basket structure (rows = transactions, columns = products).

3. **Market Basket Analysis**
   - Applied the **Apriori algorithm** using Python’s `mlxtend` library.
   - Calculated key metrics:  
     - **Support:** Frequency of itemsets in transactions  
     - **Confidence:** Likelihood of buying item B if item A is bought  
     - **Lift:** Strength of the association compared to random chance

4. **Rule Generation & Interpretation**
   - Generated association rules (if-then statements) to identify strong product relationships.

5. **(Optional) RFM Analysis**
   - Segmented customers based on Recency, Frequency, and Monetary value to personalize marketing.

---

## 📊 Key Findings

- **Frequent Itemsets:**  
  Decorative home items like “White Metal Lantern”, “Hanging Heart T-Light Holder”, and “Cream Cupid Hearts Coat Hanger” are often bought together.
- **Strong Association Rules:**  
  Example:  
  - If a customer buys “White Metal Lantern”, there’s a 65% chance they’ll also buy “Hanging Heart T-Light Holder” (Lift: 3.2).
- **Seasonal Trends:**  
  Certain products see spikes during festive periods.
- **Customer Segmentation:**  
  RFM analysis highlights high-value customers who can be targeted for re-engagement.

---

## 💡 Recommendations

- **Cross-Selling:**  
  Display “Frequently Bought Together” suggestions (e.g., T-Light Holder with Lantern).
- **Product Placement:**  
  Arrange strongly associated items together on the website or in-store.
- **Targeted Promotions:**  
  Use RFM segments to send personalized offers (e.g., discounts for loyal but inactive customers).
- **Future Enhancements:**  
  - Implement faster algorithms (e.g., FP-Growth) for larger datasets.
  - Integrate real-time recommendation systems.
  - Analyze seasonal and regional trends for more targeted marketing.

---

## 🛠️ Requirements

- Python 3.x
- pandas
- mlxtend
- matplotlib
- seaborn
- jupyter (optional, for notebooks)

Install dependencies with:
