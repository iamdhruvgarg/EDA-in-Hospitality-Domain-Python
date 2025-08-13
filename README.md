# 🏨 AtliQ Grands – Exploratory Data Analysis (EDA)  

This project presents an **Exploratory Data Analysis** for **AtliQ Grands**, a hotel chain with multiple branches across India offering various categories of rooms: **Business, Premium, Luxury, and Presidential**.  

The dataset contains **3 months** of booking records, revenue earned, and revenue realized for all branches.  
The dataset was made available by **Codebasics**.  

---

## 📂 Project Overview
This EDA project aims to:
- Understand and analyze booking patterns.
- Identify trends in revenue and occupancy.
- Clean and transform the dataset for deeper insights.
- Answer business-related questions using Python libraries.

---

## 🛠 Tools & Libraries Used
- **Python**
- **Pandas** – data manipulation
- **NumPy** – numerical operations
- **Jupyter Notebook** – interactive analysis

---

## 📊 Project Workflow

### **1. Data Exploration**
- Loaded the dataset into Jupyter Notebook.
- Understood each column’s meaning and relevance.
- Verified data against project requirements.
- Used commands such as:
```python
df.describe()
df.info()
df.mean()
```

---

### **2. Data Cleaning**
- Handled improper values (e.g., negative values, missing values, outliers).
- Used `fillna()` to replace missing data.
- Applied **3-point standard deviation method** to detect and remove outliers:
```python
upper_limit = df['column'].mean() + 3 * df['column'].std()
lower_limit = df['column'].mean() - 3 * df['column'].std()
df = df[(df['column'] >= lower_limit) & (df['column'] <= upper_limit)]
```
- Filtered and replaced incorrect entries.

---

### **3. Data Transformation**
- Added new calculated fields such as **Occupancy Percentage**:
```python
df['occupancy_percentage'] = (df['rooms_booked'] / df['total_rooms']) * 100
```
- Reformatted date columns for time-based analysis.

---

### **4. Insight Generation**
- Addressed key business questions, such as:
  - **Monthly revenue trends**.
  - **Revenue realized per city**.
  - **Average occupancy rate per room category**.
  - **Top-performing branches**.
- Used Pandas operations to group, aggregate, and visualize data:
```python
monthly_revenue = df.groupby('month')['revenue_realized'].sum()
```

---

## 📈 Key Insights
- Month-by-month revenue trends helped identify peak seasons.
- Certain cities showed consistently higher occupancy and revenue.
- Presidential and Luxury rooms had lower occupancy but higher per-room revenue.
- Occupancy percentage varied significantly across room categories and months.

---

## 📚 Learning Outcomes
- Improved understanding of **data cleaning techniques** in Pandas.
- Hands-on experience with **outlier detection** using standard deviation.
- Learned how to **transform datasets** to answer real-world business questions.
- Gained insight into **how Python is used in the hospitality domain** for decision-making.

---

## 📜 Credits
- **Dataset Source:** [Codebasics](https://codebasics.io)
- **Author:** *Dhruv Garg*
