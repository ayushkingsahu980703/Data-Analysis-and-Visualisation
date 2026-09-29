# 🍽️ Zomato Restaurant Data Analysis & Visualization

An exploratory data analysis project using Python to understand restaurant categories, ratings, pricing, online ordering, customer engagement, and relationships between key numerical variables.

## 📌 Project Overview

This project analyzes a dataset containing **148 restaurant records** and demonstrates an end-to-end data analysis workflow:

**Data Loading → Data Cleaning → Validation → Exploratory Data Analysis → Visualization → Correlation Analysis → Insights**

The project focuses on answering practical questions about restaurant characteristics and customer engagement.

> **Note:** All findings in this project describe the provided dataset and should not be generalized to the entire Zomato restaurant market.

---

## 🎯 Business Questions

The analysis attempts to answer the following questions:

1. Which restaurant types are most common?
2. How are restaurant ratings distributed?
3. How does cost vary across restaurant types?
4. Is restaurant cost associated with restaurant rating?
5. How common is online ordering?
6. Which restaurants receive the most customer votes?
7. What relationships exist between rating, votes, and cost?

---

## 🛠️ Technologies & Libraries

* **Python**
* **Pandas** — Data cleaning, transformation, grouping and aggregation
* **Matplotlib** — Static visualizations
* **Seaborn** — Statistical and categorical visualizations
* **Plotly** — Interactive visualizations

---

## 📂 Dataset

The dataset contains **148 restaurant records** with information related to:

* Restaurant name
* Restaurant type
* Rating
* Approximate cost for two
* Online ordering
* Table booking
* Customer votes

The dataset is used specifically for exploratory analysis and visualization.

---

## 🧹 Data Cleaning & Preparation

The project includes several data-quality and preparation steps:

* Simplifying column names
* Converting restaurant ratings such as `4.1/5` into numerical values
* Checking missing values
* Examining unique values and value counts
* Checking duplicate records
* Identifying repeated restaurant names
* Aggregating repeated restaurant names for the customer-vote analysis

For the **Top 10 restaurants by votes**, repeated restaurant names are grouped together and the maximum vote count is retained. This avoids incorrectly inflating votes by summing repeated rows.

---

## 📊 Exploratory Data Analysis

### Restaurant Type Distribution

Restaurant categories were analyzed using three visualization libraries:

* Matplotlib
* Seaborn
* Plotly

The analysis shows that **Dining** is the dominant restaurant category in the dataset, followed by **Cafes**.

---

### ⭐ Rating Analysis

The dataset contains ratings ranging from:

**2.6 → 4.6**

Key statistics:

* **Average rating:** approximately 3.63
* **Most frequent rating:** 3.8

Average ratings were also compared across different restaurant types.

---

### 💰 Cost Analysis

The project examines:

* Distribution of approximate cost for two
* Cost across restaurant categories
* Relationship between cost and rating

A regression plot is used to examine the overall linear association between cost and rating.

> Correlation or regression in this project represents association and does not establish causation.

---

### 📱 Online Ordering

Online-ordering availability was analyzed using the values recorded in the dataset.

| Online Ordering | Restaurants |
| --------------- | ----------: |
| No              |          90 |
| Yes             |          58 |

Online ordering was also compared across different restaurant categories using interactive Plotly visualizations.

---

### 🪑 Table Booking

Table-booking availability is relatively uncommon in this dataset:

| Table Booking | Restaurants |
| ------------- | ----------: |
| No            |         140 |
| Yes           |           8 |

---

### 🏆 Customer Engagement

Customer engagement was explored using the **votes** variable.

Because some restaurant names occur multiple times in the raw dataset, the Top 10 analysis groups records by restaurant name before ranking them.

The analysis identifies **Empire Restaurant** and **Meghana Foods** among the restaurants with the highest customer vote counts in the dataset.

---

## 📈 Correlation Analysis

The project examines relationships between:

* Rating
* Customer votes
* Approximate cost

Approximate correlations in the dataset:

| Variables      | Correlation |
| -------------- | ----------: |
| Rating ↔ Votes |    **0.49** |
| Rating ↔ Cost  |    **0.28** |
| Votes ↔ Cost   |    **0.32** |

All three relationships are positive in this sample.

The strongest relationship among these variables is between **rating and customer votes**.

> Correlation indicates association between variables. It does not prove that one variable causes another.

---

## 🔍 Key Findings

### Restaurant Composition

Dining restaurants account for the largest share of observations in the dataset.

### Ratings

Restaurant ratings range from **2.6 to 4.6**, with an average of approximately **3.63**.

### Online Ordering

**58 restaurants** have online ordering recorded as available, while **90** do not.

### Table Booking

Only **8 restaurants** have table booking recorded as available compared with **140** without it.

### Customer Engagement

Customer votes vary substantially between restaurants, with Empire Restaurant and Meghana Foods among the highest-voted restaurants.

### Relationships

Rating and votes show a moderate positive correlation, while cost has weaker positive relationships with both rating and votes.

---

## 📸 Visualizations

The project uses multiple visualization approaches to demonstrate different Python visualization workflows.

### Matplotlib

Used for foundational static charts such as restaurant-type distribution and online-ordering analysis.

### Seaborn

Used for categorical distributions, rating analysis, scatter plots, regression plots, and correlation analysis.

### Plotly

Used for interactive visualizations, including:

* Restaurant type distribution
* Rating vs cost
* Online ordering by restaurant type
* Cost distribution by restaurant type
* Multivariate restaurant analysis

---

## 📁 Project Structure

```text
Zomato-Data-Analysis/
│
├── Zomato_Portfolio.ipynb
├── Zomato-data-.csv
└── README.md
```

---

## 🚀 How to Run the Project

### 1. Clone the repository

```bash
git clone <your-repository-url>
```

### 2. Navigate to the project directory

```bash
cd Zomato-Data-Analysis
```

### 3. Install the required libraries

```bash
pip install pandas matplotlib seaborn plotly jupyter
```

### 4. Launch Jupyter Notebook

```bash
jupyter notebook
```

Open:

```text
Zomato_Portfolio_Polished.ipynb
```

Make sure the dataset file is present in the same directory as the notebook.

---

## 💡 What I Learned

Through this project, I practiced:

* Loading and inspecting real-world datasets
* Data cleaning and preparation
* Handling duplicate and repeated records
* Feature transformation
* Using `groupby()` and aggregation
* Value-count analysis
* Exploratory Data Analysis
* Data visualization with Matplotlib and Seaborn
* Interactive visualization with Plotly
* Correlation analysis
* Interpreting relationships between variables
* Communicating data-driven findings

---

## 📌 Portfolio Takeaway

This project demonstrates an end-to-end exploratory data analysis workflow while focusing on an important part of data science: **connecting visualizations to meaningful questions and interpreting results without making claims that the data cannot support.**

---

## 👤 Author

**Ayush King Sahu**

Aspiring Data Scientist | Python | Pandas | SQL | Data Visualization | Machine Learning

---
