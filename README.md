# Amazon Product Performance Analysis using Python & Power BI

## 📌 Project Overview

Amazon sells thousands of products across multiple categories. Understanding product performance, customer engagement, pricing, discounts, and ratings can help identify patterns that support better business decisions.

In this project, I analyzed Amazon product data using **Python for data cleaning and exploratory data analysis (EDA)** and **Power BI for interactive data visualization and dashboarding**.

The project focuses on exploring product categories, customer engagement, ratings, discounts, and pricing relationships to identify meaningful patterns and business insights.

---

## 🎯 Business Objectives

The main objectives of this project were to:

- Understand the structure and characteristics of the Amazon product dataset.
- Clean and prepare the data for analysis.
- Explore product categories, pricing, discounts, ratings, and review counts.
- Identify trends and patterns through exploratory data analysis.
- Investigate relationships between pricing, discounts, and customer ratings.
- Generate meaningful business insights from the analysis.
- Present the findings through an interactive Power BI dashboard.

---

## 📊 Dataset

The dataset was obtained from **Kaggle**.

**Dataset:** Amazon Sales Dataset  
**Dataset ID:** `karkavelrajaj/amazon-sales-dataset`

The dataset contains information related to Amazon products, including:

- Product ID
- Product Name
- Category
- Discounted Price
- Actual Price
- Discount Percentage
- Rating
- Rating Count
- Product and Review Information

The dataset was downloaded using `kagglehub` and loaded into Pandas for analysis.

---

## 🛠️ Tools & Technologies

- **Python**
- **Pandas** – Data manipulation and cleaning
- **NumPy** – Numerical operations
- **Matplotlib** – Data visualization
- **Seaborn** – Statistical visualization
- **Google Colab** – Analysis environment
- **Power BI** – Interactive dashboard and business visualization
- **Kaggle** – Dataset source

---

# 🔄 Project Workflow

## 1. Data Acquisition

The Amazon dataset was downloaded from Kaggle using the `kagglehub` library and loaded into a Pandas DataFrame for further analysis.

---

## 2. Data Understanding

Before performing the analysis, the dataset was explored to understand its structure and identify potential data quality issues.

The following checks were performed:

- Dataset preview using `head()`
- Dataset dimensions using `shape`
- Dataset information using `info()`
- Summary statistics using `describe()`
- Column names and data types
- Missing value detection
- Duplicate record detection
- Categorical value exploration

This helped identify formatting issues and missing values that needed to be handled during data cleaning.

---

## 3. Data Cleaning

Several columns contained values stored as text because of currency symbols, percentage signs, and comma formatting.

Examples included:

- `₹399`
- `₹1,099`
- `64%`
- `1,79,691`

These values were cleaned and converted into numerical formats.

### Price Cleaning

Currency symbols and commas were removed from:

- `discounted_price`
- `actual_price`

### Discount Cleaning

The `%` symbol was removed from:

- `discount_percentage`

### Rating Count Cleaning

Commas were removed from:

- `rating_count`

The cleaned columns were converted into appropriate numeric data types.

Missing values in relevant columns were also handled before continuing with the analysis.

---

## 4. Feature Engineering

The original `category` column contained multiple levels of product categories separated by `|`.

The category information was separated to create a clearer hierarchy:

- Main Category
- Sub Category
- Product Category

This made the category structure easier to analyze during EDA and was also useful when creating the Power BI dashboard.

---

# 📈 Exploratory Data Analysis

After cleaning and preparing the dataset, exploratory data analysis was performed to investigate important business questions.

### Business Questions

1. **Which main product categories contain the highest number of products?**

2. **Which products have received the highest number of customer ratings/reviews?**

3. **How are customer ratings distributed across the products?**

4. **What discount percentages are most commonly offered across products?**

5. **Is there a relationship between the discount offered on a product and its customer rating?**

6. **How are price, discount, rating, and rating count related to each other?**

Different visualizations and statistical analysis techniques were used to explore these questions.

---

# 🔍 Key Findings from EDA

- Technology-related categories, particularly **Electronics** and **Computers & Accessories**, have a strong presence in the dataset.
- Most products receive relatively high customer ratings, with ratings concentrated around **4.0–4.5**.
- Customer engagement is concentrated among a smaller number of highly reviewed products.
- Moderate discount percentages are commonly offered across products.
- There is **no strong relationship between discount percentage and customer ratings**.
- Actual price and discounted price show a strong positive relationship.
- Rating has relatively weak relationships with the pricing and discount variables analyzed.

---

# 📊 Power BI Dashboard

After completing the data cleaning and exploratory analysis in Python, the prepared data was used to create an interactive **Power BI dashboard**.

The dashboard provides a business-oriented view of Amazon product performance.

### Dashboard KPIs

- **Total Products:** 1,462
- **Average Rating:** 4.10
- **Average Discount:** 47.67%
- **Average Discounted Price:** 3.13K

### Dashboard Visualizations

The dashboard includes:

- Main Category and Sub Category analysis
- Discount % vs Rating
- Customer Rating Distribution
- Average Discounted Price by Rating
- Discount Distribution
- Interactive Main Category filtering

The dashboard allows users to explore product performance and identify patterns across different categories and metrics.

![Amazon Product Performance Dashboard](Screenshot%202026-08-19%20211517.png)

---

# 💡 Business Insights

Based on the analysis:

- Product performance varies across different categories and product groups.
- Technology-related categories represent a significant portion of the products analyzed.
- High customer ratings are common across the dataset.
- Customer engagement varies considerably across products.
- Discounts are widely used, but higher discounts do not necessarily correspond to higher customer ratings.
- Pricing, customer ratings, discounts, and review engagement should be considered together when evaluating product performance.

---

# 📌 Conclusion

This project analyzed Amazon product performance by examining product categories, pricing, discounts, customer ratings, and review counts.

Python was used for data cleaning, feature engineering, exploratory data analysis, and identifying relationships within the data. The prepared data was then used in Power BI to create an interactive dashboard for visual exploration and business-oriented reporting.

Overall, the analysis shows that technology-related categories have a strong presence in the dataset, most products receive relatively high ratings, and discount percentage does not show a strong relationship with customer ratings. These findings highlight the importance of considering multiple factors such as product category, customer engagement, pricing, and customer feedback when evaluating product performance.

---

# 📁 Project Files

- `Amazon_Product_Performance_Analysis.ipynb` – Python data cleaning and exploratory data analysis
- `amazon-product-performance-dashboard.png` – Power BI dashboard
- `README.md` – Project documentation

---

## 👩‍💻 Project Author

**Srushti Kirve**

B.Tech Artificial Intelligence & Data Science Student

---

⭐ If you found this project interesting, feel free to explore the notebook and dashboard.
