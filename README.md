# E_Commerce_Sales_Analysis
# 🛒 E-Commerce Sales & Supply Chain Analytics Dashboard

### 📊 Project Overview
This project analyzes a dataset of **100k+ orders** from a Brazilian E-Commerce platform (Olist) to extract insights on sales performance, product trends, and supply chain efficiency.

The goal was to build an end-to-end data pipeline that transforms raw CSV logs into an actionable **Business Intelligence Dashboard**.

**Live Dashboard / Key Insights:**
![Dashboard Screenshot](dashboard_screenshot.png) 
<img width="688" height="519" alt="Screenshot 2026-01-02 223412" src="https://github.com/user-attachments/assets/22ec1db6-d29f-4c6f-b296-6ddf67c43611" />

<img width="773" height="497" alt="Screenshot 2026-01-02 223428" src="https://github.com/user-attachments/assets/e01b5f26-f067-4b81-b20d-720c5125562c" />

<img width="779" height="501" alt="Screenshot 2026-01-02 223506" src="https://github.com/user-attachments/assets/b7a4461d-3a79-4417-9101-47e66e72bab0" />

<img width="978" height="524" alt="Screenshot 2026-01-02 223518" src="https://github.com/user-attachments/assets/ee11cfac-2491-4bb3-927d-6fc8170c338a" />

<img width="952" height="527" alt="Screenshot 2026-01-02 223523" src="https://github.com/user-attachments/assets/27d2d3ad-7d4c-4bb5-979e-edc7922739d8" />



### 🛠️ Tech Stack
*   **Python (Pandas):** For data extraction (ETL) and cleaning.
*   **SQL (SQLite):** For data storage and complex querying (Joins, CTEs, Date Math).
*   **Power BI:** For data visualization and interactive reporting.

### 🔍 Key Features & Analysis
1.  **ETL Pipeline:** 
    *   Ingested 5 raw CSV files (`orders`, `items`, `products`, `payments`, `customers`).
    *   Loaded them into a relational **SQLite database** using Python.
    *   Performed data validation to handle missing values and date formats.

2.  **Advanced SQL Analysis:**
    *   Created a "Master View" by performing **multi-table JOINS** across the entire schema.
    *   Calculated **Delivery Performance** (Actual vs. Estimated Delivery Date) using SQL date functions (`julianday`).
    *   Segmented customers by location to identify logistics bottlenecks.

3.  **Business Insights (Power BI):**
    *   **Sales Trends:** Identified seasonal spikes in Q4 (Black Friday/Holidays).
    *   **Top Products:** "Bed_Bath_Table" and "Health_Beauty" account for the highest revenue.
    *   **Logistics Lag:** Discovered that customers in Northern states (e.g., RR, AP) face an average delivery time of **25+ days**, compared to 8 days in the South (SP).

### 📂 Project Structure
```text
├── data/                   # Raw CSV files (Git ignored if large)
├── scripts/
│   ├── 1_load_db.py        # Python script to load CSVs into SQLite
│   └── 2_extract_data.py   # Python script to run SQL & export Master CSV
├── olist_store.db          # SQLite Database file
├── master_sales_data.csv   # Final Cleaned Data for Power BI
└── README.md               # Project Documentation


🚀 How to Run
Clone the repo:
git clone https://github.com/your-username/ecommerce-analytics.git

Install dependencies:
pip install pandas sqlite3

Run the ETL Pipeline:
python scripts/1_load_db.py
python scripts/2_extract_data.py


View the Dashboard:
Open dashboard.pbix in Power BI Desktop to explore the visualizations.
