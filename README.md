
# Retail Customer Behavior Analysis  

## Overview  
This project analyzes **customer purchasing behavior** using the UCI Online Retail dataset.  
The goal is to understand sales trends, identify valuable customers, and segment them using **RFM analysis** and **clustering** to generate actionable business insights.  

---

## 📊 Dataset  
- **Source:** [UCI Machine Learning Repository – Online Retail](https://archive.ics.uci.edu/ml/datasets/online+retail)  
- **Period:** Dec 2010 – Dec 2011  
- **Size:** 541,909 transactions, ~4,300 customers  
- **Columns:** InvoiceNo, StockCode, Description, Quantity, InvoiceDate, UnitPrice, CustomerID, Country  

---

## 🛠️ Steps & Methods  

### 1. Data Cleaning & Preprocessing  
- Removed missing `CustomerID` values.  
- Filtered out negative/zero `Quantity` and `UnitPrice`.  
- Removed cancelled orders (Invoice numbers starting with 'C').  
- Added `TotalPrice = Quantity × UnitPrice`.  
- Final dataset: **392,692 rows, 9 columns**.  

### 2. Exploratory Data Analysis (EDA)  
- Identified **top products** by sales volume & revenue.  
- Analyzed **monthly revenue trends**.  
- Found **most valuable customers**.  
- Explored **country-level sales** and **weekday purchase patterns**.  

### 3. Visualizations  
- Line chart of **monthly revenue**.  
- Bar charts for **top products** and **top countries**.  
- Histogram of **order values** and **customer lifetime value**.  

### 4. Customer Segmentation – RFM Analysis  
- Calculated **Recency, Frequency, Monetary (RFM)** metrics per customer.  
- Assigned **RFM scores** (1–5 scale) for each metric.  
- Segmented customers into:  
  - Champions (933)  
  - Loyal Customers (1,346)  
  - Needs Attention (1,515)  
  - At Risk (544)  

### 5. Clustering (KMeans)  
- Applied log transformation & standardization to RFM metrics.  
- Used **Elbow Method** → optimal **K = 4**.  
- Profiles:  
  - **Cluster 0 (VIPs):** Recent, frequent, high spenders.  
  - **Cluster 1 (Lost):** Inactive, very low spend.  
  - **Cluster 2 (Moderates):** Active but low frequency/spend.  
  - **Cluster 3 (Potential Loyalists):** Medium activity, worth nurturing.  

---

##  Executive Insights  
- Revenue peaks toward **end of 2011** (seasonal demand).  
- UK dominates sales; international markets contribute less.  
- Small % of customers drive the majority of revenue (**Pareto principle**).  
- Marketing actions:  
  - Reward **Champions** with loyalty benefits.  
  - Upsell/cross-sell to **Loyal Customers**.  
  - Run **re-engagement campaigns** for “Needs Attention”.  
  - Send **win-back offers** to “At Risk” customers.  

---

## Repository Structure  
```
📦 retail-customer-analysis  
 ┣ 📜 Retail_Analysis_Notebook.ipynb   # Jupyter notebook  
 ┣ 📜 rfm_table.csv                    # RFM segmentation results  
 ┣ 📜 cluster_profile.csv              # KMeans cluster summaries  
 ┣ 📜 monthly_revenue.png              # Visualization example  
 ┣ 📜 top_products.png                 # Visualization example  
 ┗ 📜 README.md                        # Project overview (this file)  
```

---

##  Tech Stack  
- Python (Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn)  
- Jupyter Notebook  
- GitHub for version control & portfolio showcase  

---

## How to Run  
1. Clone repo and install dependencies:
   ```bash
   pip install pandas numpy scikit-learn matplotlib seaborn openpyxl
   ```
2. Open Jupyter Notebook and run `Retail_Analysis_Notebook.ipynb`.  

---

## Author  
👤 Kaustubh Gaikwad
📧 kaustubh01gaikwad@gmail.com 
🔗 LinkedIn: http://linkedin.com/in/kaustubhgaikwad-msba | GitHub: https://github.com/kaustubh-gaikwad 
