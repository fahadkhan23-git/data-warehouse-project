🚀 Data Warehouse & Analytics Project
A comprehensive end-to-end Data Engineering and Analytics solution. This project demonstrates the transformation of raw, disjointed CSV data from ERP and CRM systems into a high-performance Star Schema data warehouse.

---------------------------------------------------------------------------------------------

🏗️ Data Architecture
This project implements the Medallion Architecture, ensuring data quality and lineage at every step:

🟫 Bronze (Raw): Direct ingestion of CSV files from source systems (ERP & CRM) into SQL Server.

⬜ Silver (Standardized): Data cleansing, deduplication, and schema enforcement. Handling of nulls and inconsistent date formats.

🟧 Gold (Analytical): Business-ready Star Schema consisting of Fact and Dimension tables optimized for BI tools.

---------------------------------------------------------------------------------------------

🌟 Key Features
Data Integration: Merging disparate datasets (Sales, Customers, Products) into a single source of truth.

Star Schema Modeling: Designed for performance with clear Fact/Dimension relationships.

Data Quality Assurance: SQL-based testing to ensure zero data loss and referential integrity.

Automated Workflow: Structured SQL scripts for repeatable ETL processes.

---------------------------------------------------------------------------------------------

🛠️ Tech Stack & Tools
Database: Microsoft SQL Server 2019

Management: SQL Server Management Studio (SSMS)

Project Tracking: Notion

Version Control: Git & GitHub

--------------------------------------------------------------------------------------------

📂 Project Structure

├── datasets/           # Raw ERP and CRM CSV files
├── docs/               # Architecture, ERDs, and Data Dictionary
├── scripts/
│   ├── bronze/         # DDL: Creating raw staging tables
│   ├── silver/         # DML: Cleansing and standardization logic
│   └── gold/           # DML: Final Fact & Dimension modeling
├── tests/              # SQL scripts for data validation
└── README.md

---------------------------------------------------------------------------------------------

🚀 How to Run This Project

1. Prerequisites
Install SQL Server Express.
Install SSMS.

2. Implementation Steps
Clone the Repo: git clone https://github.com/your-username/your-repo-name.git

Bronze Layer: Run scripts in /scripts/bronze/ to create the initial database and load raw CSVs.

Silver Layer: Execute scripts in /scripts/silver/ to clean and transform the data.

Gold Layer: Run scripts in /scripts/gold/ to build the final analytical Star Schema.

Validate: Run the scripts in /tests/ to ensure data matches source totals.

---------------------------------------------------------------------------------------------

📊 Sample Analytics Insight
Once the Gold layer is populated, you can run complex queries like Customer Lifetime Value (CLV):

SELECT 
    c.customer_name,
    SUM(f.sale_amount) as total_spent,
    COUNT(f.sale_id) as total_orders
FROM gold.fact_sales f
JOIN gold.dim_customers c ON f.customer_key = c.customer_key
GROUP BY c.customer_name
ORDER BY total_spent DESC;

---------------------------------------------------------------------------------------------

📜 License
Distributed under the MIT License. See LICENSE for more information.

---------------------------------------------------------------------------------------------

📬 Contact & Portfolio
Your Name – Your LinkedIn – your@email.com

Project Link: https://github.com/fahadkhan23-git/data-warehouse-project
