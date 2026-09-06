# 🍽️ Zomato Bangalore Restaurant EDA

An exploratory data analysis (EDA) project in Python exploring over 50,000 restaurant listings across Bengaluru from Zomato. This project focuses on data cleaning, feature engineering, geographical analysis, and identifying business insights for restaurant owners, platforms, and food industry investors.

---

## 📌 Links & References

* **Source Code Notebook:** [GitHub Repository Code](https://github.com/Kirubakaran05/Zomato-Bangalore-Restaurant-EDA/blob/main/zomato-data-set-analysis-visualization.ipynb)
* **Original Dataset:** [Kaggle Dataset Source](https://www.kaggle.com/code/akshitmadan/zomato-data-set-analysis-visualization/input)

---

## 📊 Business Problem & Project Overview

Bengaluru is known as the restaurant capital of India, with thousands of eateries spanning various cuisines, service types, and price points. The objective of this project is to analyze the operational dynamics of restaurants in Bangalore to answer key strategic questions:

1. How do online order availability and table booking services impact customer ratings?
2. Which locations exhibit the highest restaurant density and customer engagement?
3. What are the dominant cuisines, and where do potential market gaps exist?
4. What pricing structures align best with high-rated dining experiences?

---

## 🛠️ Tech Stack & Dependencies

* **Language:** Python 3.x
* **Environment:** Jupyter Notebook / Google Colab
* **Data Manipulation:** `pandas`, `numpy`
* **Data Visualization:** `matplotlib`, `seaborn`

---

## 📁 Dataset Schema & Preprocessing

The original Kaggle dataset consists of 17 attributes and over 51,000 records (`zomato.csv`).

### Data Cleaning Workflow
1. **Feature Dropping:** Removed redundant or uninformative columns (`url`, `address`, `phone`, `dish_liked`, `reviews_list`, `menu_item`).
2. **Missing & Duplicate Handling:** Dropped duplicate records and missing data rows (`dropna()`).
3. **Rating Transformation:** Cleaned the `rate` column (e.g., `'4.1/5'` $\rightarrow$ `4.1`), removed non-numeric values like `'NEW'` and `'-'`, and converted the column to floating-point values.
4. **Cost Transformation:** Stripped commas from `approx_cost(for two people)` (e.g., `'1,200'` $\rightarrow$ `1200`) and cast to numeric type.
5. **Rare Category Grouping:** Handled high cardinality in features such as `location` and `cuisines` by binning low-frequency entries into an **"Others"** category.

---

## 💡 Key Analysis & Insights

### 1. Impact of Table Booking & Online Ordering
* **Higher Ratings for Table Bookings:** Restaurants offering table reservation facilities consistently achieve higher median ratings (~4.0–4.3) compared to walk-in/delivery-only places.
* **Online Orders Drive Volume:** The vast majority of listed restaurants enable online ordering, driving the bulk of transaction volume on Zomato.

### 2. Location & Density Mapping
* **Top Dining Hubs:** BTM Layout, Koramangala, and Indiranagar have the highest concentration of listed restaurants.
* **Market Opportunity:** BTM Layout features a high density of delivery-first outlets but relatively few dine-in table reservation options, representing a key market entry opportunity for new dine-in establishments.

### 3. Customer Engagement (Votes)
* **Koramangala (5th Block)** and **Indiranagar** generate the highest total review vote counts, indicating strong consumer engagement and active feedback loops.

### 4. Cuisine Market Share
* The top 3 dominant cuisines by menu distribution and consumer demand are:
  1. **North Indian**
  2. **Chinese**
  3. **South Indian**

---

## 🚀 How to Run Locally

### 1. Clone the Repository
```bash
git clone [https://github.com/Kirubakaran05/Zomato-Bangalore-Restaurant-EDA.git](https://github.com/Kirubakaran05/Zomato-Bangalore-Restaurant-EDA.git)
cd Zomato-Bangalore-Restaurant-EDA
