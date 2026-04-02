<div align="center">


# Vendor Performance Analysis

**An end-to-end supply chain analytics pipeline to identify reliable vendors, detect delivery delays, and drive smarter procurement decisions.**

![Python](https://img.shields.io/badge/Python-3.x-3776AB?style=flat-square&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-Data%20Extraction-4479A1?style=flat-square&logo=mysql&logoColor=white)
![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-F2C811?style=flat-square&logo=powerbi&logoColor=black)
![Status](https://img.shields.io/badge/Status-Complete-2ea44f?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-lightgrey?style=flat-square)

</div>

---

## 📌 Overview

This project provides a comprehensive vendor performance evaluation system built on a three-stage data pipeline: SQL-based extraction, Python-driven cleaning and analysis, and Power BI visualization. It enables procurement teams and supply chain managers to move from raw transactional data to clear, actionable vendor insights.

---

## 📊 Dashboard Preview

> _Open `dashboard/vendor_dashboard.pbix` in Power BI Desktop to explore the full interactive report._

![Dashboard Preview](assets/dashboard_preview.png)

**Dashboard includes:**
- KPI cards — Total Sales, Active Vendors, Avg Rating, Delay Rate
- Top Vendors by Sales (bar chart)
- Vendor Rating Comparison
- Delivery Delay Trend Analysis

---

## 🎯 Problem Statement

Organizations managing large vendor networks often struggle with a critical visibility gap. Without a structured evaluation framework, underperforming suppliers go undetected until they cause material supply chain disruptions.

**Key challenges addressed:**
- No centralized view of vendor reliability across sales, delivery, and ratings
- Delayed identification of vendors causing fulfillment bottlenecks
- Inability to objectively compare vendors in the same product category
- Manual, time-intensive reporting with no repeatable pipeline

---

## 🗄️ Dataset

| Column | Type | Description |
|---|---|---|
| `vendor_id` | String | Unique identifier for each vendor |
| `product_category` | String | Category of product supplied |
| `order_quantity` | Integer | Number of units ordered per transaction |
| `sales_amount` | Float | Total revenue generated from the transaction |
| `delivery_time` | Integer | Days taken to deliver from order date |
| `vendor_rating` | Float | Composite rating score (1.0 – 5.0) |

---

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| **SQL** | Data extraction, aggregation, and vendor-level querying |
| **Python** | Data cleaning, preprocessing, and statistical analysis |
| **Power BI** | Interactive dashboard with drill-throughs and filters |

**Python Libraries:** `pandas` · `numpy` · `matplotlib` · `seaborn` · `sqlalchemy` · `jupyter`

---

## 🔍 Analysis Performed

- Total sales by vendor with product category breakdown
- Vendor-to-vendor performance benchmarking
- Delivery delay frequency and severity analysis
- Identification of high-delay vendors by category
- Rating distribution and outlier detection
- Correlation between vendor rating, delivery time, and sales
- Top vendor ranking by composite performance score
- Category-level vendor concentration analysis

---

## 💡 Key Insights

> **Sales Concentration**
> The top 20% of vendors account for over 70% of total sales — a classic Pareto distribution. Businesses should prioritize relationship management with this core group.

> **Delivery Risk**
> ~14% of vendors show consistently elevated delivery times, directly increasing stockout risk. These vendors require immediate performance review or contract renegotiation.

> **Rating–Performance Correlation**
> Vendors with ratings above 4.0 show on average 28% higher sales and 40% lower delay rates — making vendor ratings a reliable proxy for overall performance.

---

## 📁 Project Structure
```
vendor-performance-analysis/
├── data/
│   ├── vendor_raw.csv          # Raw dataset
│   └── vendor_cleaned.csv      # Preprocessed data
├── sql/
│   └── queries.sql             # Extraction & aggregation queries
├── notebooks/
│   ├── 01_data_cleaning.ipynb  # Cleaning pipeline
│   └── 02_analysis.ipynb       # EDA & statistical analysis
├── dashboard/
│   └── vendor_dashboard.pbix   # Power BI report file
├── assets/
│   └── dashboard_preview.png   # Dashboard screenshot
├── requirements.txt
└── README.md
```

---

## 🚀 Getting Started

**Prerequisites:** Python 3.8+, pip, Jupyter Notebook, Power BI Desktop (Windows)
```bash
# 1. Clone the repository
git clone https://github.com/your-username/vendor-performance-analysis.git
cd vendor-performance-analysis

# 2. Install dependencies
pip install -r requirements.txt

# 3. Run data cleaning
jupyter notebook notebooks/01_data_cleaning.ipynb

# 4. Run analysis
jupyter notebook notebooks/02_analysis.ipynb

# 5. Open dashboard in Power BI Desktop
#    File → Open → dashboard/vendor_dashboard.pbix
```

---

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/your-feature`)
3. Commit your changes (`git commit -m 'Add your feature'`)
4. Push and open a Pull Request

Please follow PEP 8 style guidelines and add comments for any new analysis logic.

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

<div align="center">Made with Python, SQL & Power BI &nbsp;·&nbsp; ⭐ Star this repo if you found it useful!</div>
