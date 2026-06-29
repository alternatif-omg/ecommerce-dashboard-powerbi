# 🛒 E-Commerce Revenue & Logistics Dashboard

An end-to-end data analysis project using SQL and Power BI on the Brazilian E-Commerce (Olist) dataset containing 100,000+ orders across multiple business dimensions.

---

## 📊 Dashboard Preview

### Page 1 — Revenue Overview
![Revenue Overview](screenshots/halaman1.png)

### Page 2 — Logistics Performance
![Logistics Performance](screenshots/halaman2.png)

### Page 3 — Customer Analysis
![Customer Analysis](screenshots/halaman3.png)

---

## 🛠️ Tools & Technologies
| Tool | Purpose |
|---|---|
| SQL (SQLite) | Data extraction, transformation, and aggregation |
| Power BI Desktop | Dashboard development and visualization |
| DAX | Custom measures and KPI calculations |
| Power Query | Data modeling and relationship management |

---

## 📁 Dataset
- **Source:** [Brazilian E-Commerce Public Dataset by Olist](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)
- **Size:** 100,000+ orders
- **Period:** 2016 – 2018
- **Tables:** orders, order_items, order_payments, customers, products, sellers, reviews

---

## 📈 Dashboard Pages

### 1. Revenue Overview
- Monthly revenue trend
- Top 10 product categories by revenue
- Payment method breakdown
- Key KPIs: Total Revenue, Total Orders, Avg Order Value, Delivered Orders

### 2. Logistics Performance
- Average delivery days per state
- Order distribution map by state
- Order status filter (slicer)
- Key KPIs: Avg Delivery Days, Avg Review Score, Total Orders

### 3. Customer Analysis
- Order status distribution
- Top 10 cities by orders
- Review score trend over time
- State filter (slicer)
- Key KPIs: Total Orders, Avg Review Score, Repeat Customers

---

## 💡 Key Insights
- **Total Revenue:** 16M+
- **Top Category:** Bed Bath Table (1.7M revenue)
- **Dominant Payment Method:** Credit Card (78%)
- **Most Active State:** SP (São Paulo)
- **Peak Revenue Month:** [isi dari dashboard kamu]
- **Average Delivery Time:** [isi dari dashboard kamu] days

---

## ⚙️ DAX Measures Used
```
Total Revenue = SUM(order_payments[payment_value])
Total Orders = DISTINCTCOUNT(orders[order_id])
Avg Order Value = DIVIDE([Total Revenue], [Total Orders])
Delivered Orders = CALCULATE(DISTINCTCOUNT(orders[order_id]), orders[order_status] = "delivered")
Avg Delivery Days = AVERAGEX(FILTER(orders, orders[order_delivered_customer_date] <> BLANK()), DATEDIFF(orders[order_purchase_timestamp], orders[order_delivered_customer_date], DAY))
Avg Review Score = AVERAGE(order_reviews[review_score])
```

---

## 📥 Download Dashboard File
> 📎 [Download .pbix file](GANTI_DENGAN_LINK_GDRIVE_KAMU)

---
