# 📊 E-Commerce Customer Analysis (SQL)

SQL-based business intelligence analysis for TechStore, demonstrating advanced querying techniques across customer, product, and order data.



## 🎯 Project Overview

Comprehensive SQL analysis of an e-commerce dataset to extract actionable business insights. This project showcases proficiency in multi-table JOINs, aggregations, customer segmentation, and time-series analysis.

**Key Highlights:**
- Analyzed $7,660 in revenue across 16 orders from 10 customers
- Identified that top 2 customers account for 46% of total revenue
- Discovered 30% of signups have never made a purchase
- Revealed 192% revenue growth from July to September 2023

---



## 🗄️ Database Schema

### Entity Relationship Diagram
```
┌─────────────┐         ┌──────────────┐         ┌─────────────┐
│  CUSTOMERS  │         │    ORDERS    │         │  PRODUCTS   │
├─────────────┤         ├──────────────┤         ├─────────────┤
│customer_id  │────┐    │ order_id     │    ┌────│ product_id  │
│customer_name│    └───<│ customer_id  │    │    │product_name │
│email        │         │ product_id   │>───┘    │ category    │
│city         │         │ order_date   │         │ price       │
│state        │         │ quantity     │         └─────────────┘
│signup_date  │         │ total_amount │
└─────────────┘         └──────────────┘
```

### Tables

**Customers** (10 customers across 7 states)
- `customer_id` (PK), `customer_name`, `email`, `city`, `state`, `signup_date`

**Products** (10 products across 5 categories)
- `product_id` (PK), `product_name`, `category`, `price`

**Orders** (16 transactions)
- `order_id` (PK), `customer_id` (FK), `product_id` (FK), `order_date`, `quantity`, `total_amount`

---


```

---

## 📊 Analysis Queries & Insights

### 1️⃣ Total Revenue & Order Count
**Business Question:** What's our overall performance?
```sql
SELECT 
    SUM(total_amount) AS total_revenue,
    COUNT(order_id) AS order_count 
FROM orders;
```

**Result:** $7,660 revenue | 16 orders | $478.75 avg order value

---

### 2️⃣ Top 5 Customers
**Business Question:** Who are our most valuable customers?

**Key Finding:** 
- Bob Smith: $2,025 (26.4% of revenue)
- Alice Johnson: $1,535 (20.0% of revenue)
- **Top 2 customers = 46.4% of total revenue** ⚠️

**Recommendation:** Implement VIP retention program

---

### 3️⃣ Category Performance
**Business Question:** Which categories drive revenue?

| Category | Revenue | % of Total |
|----------|---------|------------|
| Computers | $4,200 | 55% |
| Monitors | $1,920 | 25% |
| Accessories | $665 | 9% |

**Insight:** Computers dominate despite being 20% of SKUs

---

### 4️⃣ Geographic Analysis
**Business Question:** Which states are our strongest markets?

**Key Finding:** CA and NY each generate ~$2,300 with just 2 customers

**Recommendation:** Focus marketing on high-value states

---

### 5️⃣ Inactive Customer Detection
**Business Question:** Who signed up but never purchased?

**Result:** 3 inactive customers (30% of signups)

**Action:** Launch re-engagement campaign with first-order discount

---

### 6️⃣ Product Popularity
**Top sellers by units:** USB-C Hub (3 units), Laptop Pro (2 units)

---

### 7️⃣ Customer Segmentation
**Tiers:**
- VIP (≥$1,500): 2 customers
- Regular ($500-$1,499): 3 customers
- Occasional (<$500): 2 customers

---

### 8️⃣ Monthly Revenue Trend
**Growth trajectory:**
- July: $1,250
- August: $2,755 (+120%)
- September: $3,655 (+33%)

**192% growth from July to September!** 📈

---

### 9️⃣ Cross-Sell Opportunities
**Finding:** 3 customers buy from multiple categories

**Action:** Create product bundles for these segments

---

### 🔟 High-Value Orders
**Result:** 4 orders >$1,000 (all Laptops)

**Action:** Premium customer service for these transactions

---

## 💡 Key Business Recommendations

### 🎯 Priority 1: Customer Retention
- **Issue:** 46% revenue from 2 customers (concentration risk)
- **Action:** VIP loyalty program with dedicated account management
- **Impact:** Prevent churn = save $1,700/year per VIP customer

### 📧 Priority 2: Customer Activation
- **Issue:** 30% of signups never purchase
- **Action:** Automated email sequence with first-order discount
- **Impact:** Convert 10% = +$500 revenue

### 🛒 Priority 3: Category Expansion
- **Issue:** Over-reliance on Computers (55% of revenue)
- **Action:** Expand product lines in Monitors and Accessories
- **Impact:** Risk diversification + revenue growth

### 📍 Priority 4: Geographic Focus
- **Issue:** CA and NY = highest ROI markets
- **Action:** Increase marketing spend in these states
- **Impact:** Leverage proven channels

---

## 🛠️ Technical Skills Demonstrated

### SQL Proficiency
- ✅ Multi-table JOINs (INNER, LEFT across 3 tables)
- ✅ Aggregation functions (SUM, COUNT, AVG, COUNT DISTINCT)
- ✅ GROUP BY with HAVING clauses
- ✅ WHERE vs HAVING (pre/post aggregation filtering)
- ✅ CASE WHEN for customer segmentation
- ✅ Date functions (TO_CHAR, date formatting)
- ✅ NULL handling (IS NULL for non-matching records)
- ✅ Subquery concepts
- ✅ Window functions (optional advanced queries)

### Business Analysis
- ✅ KPI definition and tracking
- ✅ Customer segmentation strategies
- ✅ Churn risk identification
- ✅ Revenue concentration analysis
- ✅ Time-series trend analysis
- ✅ Cross-sell opportunity identification

---

## 📈 Sample Output

**Customer Tier Distribution:**
```
| Customer       | Spent  | Orders | Tier       |
|----------------|--------|--------|------------|
| Bob Smith      | $2,025 | 4      | VIP        |
| Alice Johnson  | $1,535 | 4      | VIP        |
| Frank Wilson   | $1,285 | 2      | Regular    |
| Grace Lee      | $300   | 1      | Occasional |
```

---

## 📞 Connect With Me

**[Your Name]**  
📧 Email: your.email@example.com  
💼 LinkedIn: [linkedin.com/in/yourprofile](https://linkedin.com/in/yourprofile)  
🌐 Portfolio: [yourportfolio.com](https://yourportfolio.com)

**Other Projects:**
- [Executive Sales Dashboard (Excel)](link-to-excel-project)
- [Python Data Cleaning Pipeline](link-to-python-project)

---

## 🙏 Acknowledgments

- Dataset structure inspired by real e-commerce patterns
- Created for educational and portfolio demonstration purposes

---

## 📄 License

This project is open source and available under the MIT License.

---

**⭐ If this project was helpful, please star the repository!**

*Last Updated: February 2026*
```

---

## 📁 File 8: .gitignore
```
# Database
*.db
*.sqlite
*.sql~

# IDE
.vscode/
.idea/
*.swp
*.swo

# OS
.DS_Store
Thumbs.db

# Logs
*.log
```

---

## 🎯 Step 2: Create Your Folder Structure

On your computer, create this structure:
```
SQL-Customer-Analysis/
├── data/
│   ├── customers.csv
│   ├── products.csv
│   └── orders.csv
├── sql/
│   ├── 01_create_tables.sql
│   ├── 02_insert_data.sql
│   └── 03_analysis_queries.sql
├── README.md
└── .gitignore
