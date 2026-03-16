# 🛒 Walmart Sales Data Analysis: End-to-End SQL & Python Project

## 📌 Project Overview
This project is an end-to-end data analysis pipeline utilizing a Walmart sales dataset containing 10,000 transactions. The objective is to extract actionable business insights regarding branch performance, customer payment preferences, and category profitability. 

The workflow encompasses data extraction via the Kaggle API, data manipulation and cleaning using Python (Pandas), database integration via SQLAlchemy, and complex exploratory data analysis (EDA) using MySQL.

## 🛠️ Tech Stack & Tools
* **Data Extraction:** Kaggle API
* **Data Cleaning & Preprocessing:** Python, Pandas, Jupyter Notebook
* **Database Management:** MySQL, SQLAlchemy (Python integration)
* **Data Analysis:** SQL (MySQL Workbench)
* **Environment:** Visual Studio Code (VS Code)

## 📂 Project Structure
```text
WALMART_DATA_ANALYSIS/
│
├── my_env/                     # Python virtual environment
├── project.ipynb               # Jupyter notebook for data cleaning and DB connection
├── Readme.md                   # Project documentation
├── requirements.txt            # Python dependencies
├── walmart-10k-sales-dat...    # Raw dataset (downloaded via API)
├── Walmart.csv                 # Working copy of raw data
└── walmart_clean_data.csv      # Cleaned dataset ready for SQL import
🚀 Methodology
1. Data Extraction & Environment Setup
Set up a virtual environment (my_env) in VS Code.

Configured the Kaggle API (kaggle.json) in the home directory.

Downloaded the raw Walmart sales dataset (10,000 rows, 11 columns) directly into the project workspace.

2. Data Cleaning & Transformation (Python/Pandas)
Loaded the data into a Pandas DataFrame.

Engineered a new feature: total_price (calculated as unit_price * quantity).

Standardized all column names to lowercase for seamless database integration.

Exported the cleaned data to walmart_clean_data.csv.

3. Database Integration (SQLAlchemy)
Established a connection to a local MySQL server using Python's sqlalchemy library.

Automated the table creation and data insertion process by appending the Pandas DataFrame directly into the walmart database.

4. Exploratory Data Analysis (MySQL)
Conducted advanced SQL queries (utilizing Window Functions, CTEs/Subqueries, and Date/Time extractions) to solve key business problems.

📊 Business Problems Solved
Below are the core business questions answered through SQL queries in this project:

Transaction Volume by Payment: What are the different payment methods, and what is the total number of transactions and quantities sold for each?

Branch Category Performance: What is the highest-rated product category in each branch? (Calculated using Window Functions and average ratings).

Peak Traffic Days: What is the busiest day of the week for each branch based on transaction volume?

Item Movement by Payment: What is the total quantity of items sold grouped by payment method?

Rating Distributions: What is the minimum, maximum, and average rating for products in each city and category?

Profitability Analysis: What is the total revenue and profit margin for each product category, ordered from highest to lowest?

Preferred Payment by Location: What is the most common and preferred payment method for each specific branch?

Shift-Based Sales Analysis: How are sales distributed across different times of the day (Morning, Afternoon, Evening), and what is the invoice count per shift?

⚙️ How to Run the Project
Clone the repository and open it in VS Code.

Activate the virtual environment:

Bash
source my_env/bin/activate  # On macOS/Linux
my_env\Scripts\activate     # On Windows
Install dependencies:

Bash
pip install -r requirements.txt
Run the Jupyter Notebook (project.ipynb) to execute the Python data pipeline and push the data to your local MySQL server.

Execute the SQL queries provided in the project files within MySQL Workbench to view the analysis output.