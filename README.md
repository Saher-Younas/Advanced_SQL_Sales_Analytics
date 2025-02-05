# 📊 Advanced_SQL_Sales_Analytics


## 🔍 Overview
This project presents an in-depth analysis of an e-commerce dataset (`df_orders`) using SQL. The queries extract crucial business insights, including top-selling products, regional sales distribution, revenue trends, and customer segmentation. The analysis aids in strategic decision-making for inventory management, pricing, and marketing.

---

## 🏆 Key Analyses & Insights

### 1️⃣ Top 10 Revenue-Generating Products
- **Objective:** Identify products generating the highest revenue.
- **Query Highlights:**
  - Aggregates total `sale_price` for each `product_id`.
  - Sorts in descending order to find the top 10 revenue contributors.
- **Business Impact:** Helps businesses focus on best-selling products for marketing and inventory optimization.

---

### 2️⃣ Top 5 Best-Selling Products in Each Region
- **Objective:** Determine the highest-selling products in different regions.
- **Query Highlights:**
  - Uses `ROW_NUMBER()` to rank products within each region.
  - Filters to display only the top 5 in each region.
- **Business Impact:** Assists in region-specific inventory management and marketing campaigns.

---

### 3️⃣ Month-over-Month Sales Growth (2022 vs. 2023)
- **Objective:** Compare monthly revenue across two years to identify growth trends.
- **Query Highlights:**
  - Extracts `year(order_date)` and `month(order_date)`.
  - Uses `CASE WHEN` logic to separate sales for 2022 and 2023.
- **Business Impact:** Helps in forecasting trends and planning seasonal promotions.

---

### 4️⃣ Best-Selling Month for Each Product Category
- **Objective:** Identify which month saw the highest sales for each category.
- **Query Highlights:**
  - Uses `FORMAT(order_date, 'yyyyMM')` to group by month.
  - Applies `ROW_NUMBER()` to rank the highest sales month per category.
- **Business Impact:** Helps with seasonal marketing strategies and demand planning.

---

### 5️⃣ Sub-Category with the Highest Profit Growth (2023 vs. 2022)
- **Objective:** Identify the sub-category with the highest revenue increase.
- **Query Highlights:**
  - Aggregates `sale_price` for each `sub_category` per year.
  - Calculates the difference between 2023 and 2022.
  - Orders results in descending order to highlight the highest growth.
- **Business Impact:** Helps businesses double down on high-growth product categories.

---

### 6️⃣ Best-Selling Products by Quantity Sold
- **Objective:** Identify the top 10 products by units sold.
- **Query Highlights:**
  - Aggregates total `quantity` sold per `product_id`.
  - Orders by highest units sold.
- **Business Impact:** Ensures stock availability for high-demand products.

---

### 7️⃣ Region-Wise Revenue Contribution
- **Objective:** Analyze revenue distribution across different regions.
- **Query Highlights:**
  - Calculates total revenue per `region` by summing `(sale_price * quantity)`.
  - Orders results in descending order.
- **Business Impact:** Helps businesses prioritize high-revenue regions and optimize logistics.

---

### 8️⃣ Effect of Discounts on Sales Volume
- **Objective:** Examine how discounts impact order volume.
- **Query Highlights:**
  - Groups data by `discount` and calculates total `order_id` count and `quantity` sold.
  - Orders by discount percentage.
- **Business Impact:** Provides insights into discount effectiveness and pricing strategy.

---

### 9️⃣ Fastest & Slowest Shipping Modes
- **Objective:** Determine the shipping modes with the quickest and slowest delivery times.
- **Query Highlights:**
  - Calculates `DATEDIFF(CURDATE(), order_date)` for each `ship_mode`.
  - Computes the average shipping time and ranks modes accordingly.
- **Business Impact:** Helps optimize logistics and improve customer experience.

---

### 🔟 Customer Segmentation by Spending Behavior
- **Objective:** Categorize customers based on their total spending.
- **Query Highlights:**
  - Groups orders by `segment` and calculates total spending per order.
  - Classifies customers into:
    - **High-Value Customers:** Spent > $5000
    - **Mid-Tier Customers:** Spent between $2000-$5000
    - **Low-Value Customers:** Spent < $2000
- **Business Impact:** Enables personalized marketing campaigns and loyalty programs.

---

## 🚀 Conclusion
This SQL-powered analysis provides valuable insights into sales performance, customer behavior, and business growth opportunities. The queries can be used to:
✔ Optimize **inventory management**  
✔ Enhance **regional sales strategies**  
✔ Improve **customer retention and segmentation**  
✔ Fine-tune **pricing and discount policies**  

By leveraging these insights, businesses can make **data-driven decisions** to maximize profitability and customer satisfaction.

