# Northwind Sales and Shipping Analysis (Power BI Case Study)

This Power BI project analyzes the sales and shipping performance of **Northwind Traders**, a fictional gourmet food supplier. The dashboard explores trends, customer value, product performance, and shipping cost efficiency using relational data.

## 📁 Dataset Overview

The project is based on 7 CSV files representing the business data of Northwind Traders:[link](https://www.kaggle.com/datasets/jeetahirwar/northwind-traders)

| Table          | Description |
|----------------|-------------|
| `orders`       | Orders placed by customers with dates, shipping info, and employee IDs |
| `order_details`| Products sold in each order, with unit price, quantity, and discount |
| `products`     | Product information such as name, price, and category |
| `customers`    | Details of customers including company name and location |
| `employees`    | Employee metadata including title and region |
| `shippers`     | Shipping companies and IDs |
| `categories`   | Product category information |

## 🎯 Objectives

- Identify overall sales trends and seasonality
- Discover best and worst-selling products
- Analyze top customers based on sales volume
- Compare freight cost across shippers
- Evaluate category-level profitability

---

## ❓ Business Questions

1. Are there any noticeable sales trends over time?
2. Which are the best and worst-selling products?
3. Can you identify any key customers?
4. Are shipping costs consistent across providers?
5. What are the most profitable product categories?

---

## 📊 Visuals and Analysis

### 📌 Q1. Are there any noticeable sales trends over time?

- **Goal**: Track sales trends month-by-month.
- **Visual**: Line Chart – Monthly Total Sales
- **Steps**: Created a `YearMonth` column, calculated Total Sales, plotted line chart.
- **Screenshot**:  
  ![Sales Trend](https://github.com/muhammed-saheer/CS_7_Northwind-Sales-and-Shipping-Analysis-P_BI-/blob/main/images/Sales%20Overview.png)

---

### 📌 Q2. Which are the best and worst-selling products?

- **Goal**: Identify top and bottom revenue-generating products.
- **Visual**: Bar Chart – Total Sales by Product Name
- **Steps**: Created `Total Sales` column in `order_details`, joined with `products`, sorted descending.
- **Screenshot**:  
  ![Top Products](https://github.com/muhammed-saheer/CS_7_Northwind-Sales-and-Shipping-Analysis-P_BI-/blob/main/images/Product%20Performance.png)

---

### 📌 Q3. Can you identify any key customers?

- **Goal**: Highlight high-value customers by revenue.
- **Visual**: Table with Customer ID, Name, Country, Total Sales, Orders, Segment
- **DAX**: Created `Customer Segment` using SWITCH logic.
- **Screenshot**:  
  ![Key Customers](https://github.com/muhammed-saheer/CS_7_Northwind-Sales-and-Shipping-Analysis-P_BI-/blob/main/images/Customer%20Insights.png)

---

### 📌 Q4. Are shipping costs consistent across providers?

- **Goal**: Compare average freight cost per shipping company.
- **Visual**: Column Chart – Average Freight by Shipper
- **DAX**: `Average Freight = AVERAGE(orders[freight])`
- **Screenshot**:  
  ![Shipping Cost](https://github.com/muhammed-saheer/CS_7_Northwind-Sales-and-Shipping-Analysis-P_BI-/blob/main/images/Shipping%20Analysis.png)

---

### 📌 Q5. What are the most profitable product categories?

- **Goal**: Analyze category-wise contribution to revenue.
- **Visual**: Pie/Bar Chart – Total Sales by Category
- **Steps**: Join `order_details` → `products` → `categories` and aggregate sales.
- **Screenshot**:  
  ![Category Profitability](https://github.com/muhammed-saheer/CS_7_Northwind-Sales-and-Shipping-Analysis-P_BI-/blob/main/images/Deep%20Dive%20%E2%80%93%20Category%20Profitability.png)

---

## 🧠 Key DAX Measures

```DAX
Total Sales = (order_details[unitPrice] * order_details[quantity]) * (1 - order_details[discount])

Average Freight = AVERAGE(orders[freight])
```

---

## 🏁 Conclusion

- **Sales Trends**: Clear seasonal peaks visible in Q4.
- **Product Insights**: 'Chai' and 'Chang' are top-performing; some products underperform.
- **Customer Insights**: A few key customers contribute a majority of sales.
- **Shipping**: Speedy Express offers the most affordable shipping.
- **Categories**: Beverages and Confections are the highest-revenue categories.

---

## 📂 Files in this Project

- `Northwind_Sales_and_Shipping_Analysis.pbix` – Final dashboard file
- `data/` – All source CSVs
- `images/` – Dashboard and visual screenshots

---

## 💼 Author

**Muhammed Saheer K**  
- [Portfolio Website](https://muhammed-saheer.github.io/muhammedsaheer.github.io/)  
- [LinkedIn](https://www.linkedin.com/in/muhammed-saheer-k-34a7372a8/)  
- [GitHub](https://github.com/muhammed-saheer)  
- 📧 saheershan77@gmail.com

---

> ⭐ *If you liked this project, consider giving it a star on GitHub!*
