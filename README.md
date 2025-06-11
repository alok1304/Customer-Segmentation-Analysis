# 🧠 Customer Segmentation Analysis Using RFM and KMeans Clustering

## 🔍 Overview
This project performs customer segmentation using **RFM (Recency, Frequency, Monetary)** analysis combined with **KMeans Clustering** to identify key customer groups for targeted marketing strategies.

---

## 📁 Dataset
- [Online Retail Dataset](https://www.kaggle.com/datasets/carrie1/ecommerce-data)
- Format: `.csv` file containing transactions including InvoiceNo, CustomerID, InvoiceDate, Quantity, UnitPrice, etc.

---

## 🛠️ Tools & Libraries
- Python 🐍
- Pandas, NumPy
- Scikit-learn
- Seaborn, Matplotlib
- Jupyter Notebook / Google Colab

---

## 🚀 Workflow

### 1️⃣ Load Dataset
- Load and inspect the dataset using Pandas.
- Handle encoding using `ISO-8859-1`.

### 2️⃣ Data Cleaning
- Drop rows with missing `CustomerID`.
- Remove canceled orders (InvoiceNo starting with 'C').
- Convert `InvoiceDate` to datetime format.
- Create new feature: `TotalPrice = Quantity × UnitPrice`.

### 3️⃣ RFM Analysis
- Define:
  - **Recency**: Days since last purchase
  - **Frequency**: Number of purchases
  - **Monetary**: Total money spent
- Group data by `CustomerID` to compute RFM values.

### 4️⃣ Feature Engineering
- Log-transform `Monetary` to reduce skew.
- Normalize RFM features using `StandardScaler`.

### 5️⃣ KMeans Clustering
- Use the **Elbow Method** to find the optimal number of clusters (k).
- Apply KMeans with chosen k (e.g., 4).
- Assign cluster labels to each customer.

### 6️⃣ Data Visualization
- Use `scatterplot`, `pairplot` to visualize customer segments.
- Optionally use radar charts for advanced comparison.

---

## 📈 Sample Output: Cluster Interpretation

| Cluster Type      | Description                | Strategy                          |
|------------------|----------------------------|-----------------------------------|
| **Loyal Customers** | Frequent, high spenders     | Send early-access promotions      |
| **At-Risk**         | Not purchased recently      | Re-engagement offers              |
| **New Customers**   | Recent but low frequency    | Welcome offers, loyalty program   |
| **Low Value**       | Rare & low spenders         | Upsell or cross-sell              |

---

## ✅ Conclusion
This analysis enables businesses to **tailor marketing efforts** for different customer groups by understanding their buying behavior. It is a practical use-case of unsupervised learning applied to customer data.

---

## 📌 How to Run
1. Upload the dataset `data.csv` to your notebook or environment.
2. Run each cell in the notebook `CustomerSegmentationAnalysis.ipynb`.
3. Explore the RFM features, clustering results, and insights.
