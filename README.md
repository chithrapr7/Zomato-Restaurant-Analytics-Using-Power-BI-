# 🍽️ Zomato Restaurant Analytics Dashboard (Power BI)

## 📌 Problem Statement

Zomato collects massive amounts of restaurant data across multiple countries. However, this data exists in a **raw, unstructured format**, making it difficult for stakeholders to extract meaningful insights.

### Key Challenges:

* No clear way to identify **high-performing restaurants**
* Inability to compare **delivery vs non-delivery performance**
* Lack of visibility into **pricing, ratings, and cuisine trends**
* Presence of **missing values and outliers**
* Flat dataset with **no relational structure**

### Goal:

Transform raw data into a **structured analytical model** and build an **interactive dashboard** to enable data-driven decision making.

---

## 🎯 Project Objective

To design and develop a **Power BI dashboard** that analyzes:

* Restaurant performance
* Customer ratings
* Pricing trends
* Delivery impact

Across **15 countries and 6 continents**

---

## 📂 Dataset Information

* **Source:** Zomato Public Dataset
* **Records:** 9,551 restaurants
* **Columns:** 21
* **Countries:** 15
* **Continents:** 6

### Key Data Fields:

* Restaurant Name, City, Country
* Cuisines
* Average Cost for Two
* Ratings & Votes
* Online Delivery & Table Booking

---

## 🔍 Exploratory Data Analysis (EDA)

### Key Findings:

* 🇮🇳 India contributes **90.6%** of total data
* ⭐ Average rating: **3.44** (after cleaning)
* 🍽️ Most common cuisine: **North Indian**
* 🛵 Only **25.7%** offer online delivery
* 📋 Only **12.1%** support table booking
* ⚠️ **22.5% restaurants are unrated**
* 💰 Majority fall under **budget category**

👉 Insight: Raw data was heavily **skewed and imbalanced**, requiring careful cleaning.

---

## 🏗️ Data Architecture

A **3-table Star Schema** was implemented:

### 🔹 Fact Table:

* `Performance_Fact`

  * Ratings, Votes, Cost, Delivery, Booking

### 🔹 Dimension Tables:

* `Restaurant_Dim`

  * Restaurant details, cuisine, location
* `Country_Dim`

  * Country & continent mapping

### ⚙️ Key Design Decision:

* Enabled **bi-directional filtering** to ensure correct dashboard interactions

---

## 🧹 Data Cleaning & Transformation

Performed using **Power Query**

### Steps:

* Removed **outliers** (₹8,00,000 cost entry)
* Handled **missing ratings (0 values)**
* Standardized columns
* Created **derived fields for analysis**

👉 Without this step, your results would be garbage. This is where most people mess up — you didn’t.

---

## 📊 DAX Measures (20 Total)

Key measures include:

* Total Restaurants
* Total Votes
* Weighted Average Rating
* Online Delivery %
* Table Booking %
* Rating Completion %
* Delivery Rating Uplift (+0.78)
* Avg Cost (Cleaned)

### ⚡ Advanced Logic:

* Used `CALCULATE`, `FILTER`, `DIVIDE`, `VAR`
* Avoided divide-by-zero errors
* Excluded invalid ratings

👉 This is what separates dashboards from *actual analytics work*

---

## 📈 Dashboard Overview

### 🔹 Page 1: Restaurant Performance

* 6 KPI Cards
* 8 Interactive Charts
* Filters: Continent, Country, Price, Rating

### 🔹 Page 2: Deep Dive Analysis

* Continent-wise comparison
* Country-level insights
* Cost vs Rating analysis

---

## 📌 Key Insights

1. 🇮🇳 **India dominates dataset (90.6%)**
2. 🛵 **Delivery increases ratings (+0.78)**
3. 💰 **Luxury restaurants perform better than budget**
4. ⭐ **Top-rated restaurants get 18x more votes**
5. ⚠️ **22.5% restaurants have no ratings**
6. 🌍 **Africa has highest average rating (4.21)**

👉 Important: Your dataset is India-heavy — so global conclusions are biased. A good interviewer *will* challenge you on this.

---

## 💡 Business Recommendations

* Promote **online delivery adoption**
* Launch **first-review campaigns**
* Introduce **premium restaurant badges**
* Expand into **high-performing regions (Africa, Europe)**

---

## 🚀 Tools & Technologies

* **Power BI Desktop**
* **DAX (Data Analysis Expressions)**
* **Power Query**
* **CSV Dataset**

---

## 📁 Project Files

* `zomato cp1.pbix` — Power BI Dashboard
* `Restaurant_Dim.csv`
* `Country_Dim.csv`
* `Performance_Fact.csv`
* Presentation File 

---

## 🧠 What This Project Demonstrates

* End-to-end **Data Analytics Workflow**
* Data Cleaning & Transformation
* Data Modeling (Star Schema)
* Advanced DAX Calculations
* Business Insight Generation

---

## 🏁 Conclusion

This project converts a **raw, unstructured dataset** into a **fully interactive business intelligence solution**.

By applying:

* Structured data modeling
* Robust DAX calculations
* Insight-driven dashboard design

It uncovers meaningful patterns in:

* Restaurant performance
* Customer behavior
* Pricing strategy

👉 This is not just a dashboard — it’s a **decision-making tool**

---
