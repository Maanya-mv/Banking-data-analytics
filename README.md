### **Project Description**

**Banking Customer Data: Exploratory Data Analysis (EDA) Case Study**

This project conducts an in-depth **Exploratory Data Analysis (EDA)** on a synthetic dataset of 3,000 banking customers. The goal is to understand customer demographics, financial behaviors, and product usage to uncover patterns, relationships, and insights that can inform business strategy.

The analysis involves:
*   **Data Extraction:** Connecting to a MySQL database to load the customer data.
*   **Data Profiling:** Generating summary statistics and understanding the structure of the dataset.
*   **Data Exploration:** Investigating the distribution of key categorical and numerical variables.
*   **Feature Engineering:** Creating new features, such as an `Income Band`, to facilitate analysis.
*   **Visualization:** Using `matplotlib` and `seaborn` to create bar charts and histograms for visual analysis of customer segments.

This case study serves as a practical example of a standard EDA workflow in data science, from data extraction to initial insights, using the Python data ecosystem (Pandas, NumPy, Matplotlib, Seaborn).

---

### **README.md**

# Banking Customer Data - Exploratory Data Analysis (EDA)

## Overview

This repository contains a Jupyter Notebook performing an Exploratory Data Analysis (EDA) on a dataset of 3,000 banking customers. The analysis aims to uncover insights into customer profiles, financial health, and product engagement to support data-driven decision-making in a banking context.

## Project Structure

*   `Banking- EDA Case Study.ipynb`: The main Jupyter Notebook containing the complete code and analysis.
*   `README.md`: This file, providing an overview and setup instructions.

## Dataset Description

The dataset (`banking_case.customer` table from a MySQL database) contains 25 columns and 3,000 rows. Key features include:

*   **Demographic Information:** `Client ID`, `Name`, `Age`, `GenderId`, `Nationality`, `Occupation`.
*   **Banking Relationship:** `Joined Bank` (date), `Banking Contact`, `Fee Structure` (High, Mid, Low), `Loyalty Classification` (Jade, Gold, Silver, Platinum).
*   **Financial Metrics:**
    *   `Estimated Income`, `Superannuation Savings`
    *   `Bank Deposits`, `Checking Accounts`, `Saving Accounts`, `Foreign Currency Account`
    *   `Credit Card Balance`, `Amount of Credit Cards`, `Bank Loans`, `Business Lending`
*   **Assets & Risk:** `Properties Owned`, `Risk Weighting` (1-5).
*   **Internal IDs:** `Location ID`, `BRId` (likely Branch ID), `IAId` (likely Investment Advisor ID).

## Key Steps and Findings

1.  **Data Connection & Loading:**
    *   Established a connection to a MySQL database using `mysql.connector`.
    *   Loaded the data into a Pandas DataFrame for analysis.

2.  **Initial Data Inspection:**
    *   Verified the dataset shape (3000, 25).
    *   Used `df.head()`, `df.describe()`, and `df.info()` to understand the data's structure, summary statistics, and data types. No missing values were found in this initial inspection.

3.  **Feature Engineering:**
    *   Created a new categorical feature `Income Band` by binning the `Estimated Income` into 'Low', 'Med', and 'High' categories.
    *   This simplifies the analysis of customer behavior across different income levels.

4.  **Exploratory Data Analysis (EDA):**
    *   **Categorical Variables:** Analyzed the distribution of features like `Nationality`, `Fee Structure`, `Loyalty Classification`, `Income Band`, and `Properties Owned`.
        *   *Example Insight:* The majority of customers fall into the 'Med' income band, followed by 'Low' and then 'High'.
    *   **Visualizations:** Generated bar charts to visualize the count of customers in each category for various features.
    *   **Numerical Variables:** Examined the distribution and spread of financial metrics like `Bank Deposits`, `Credit Card Balance`, and `Business Lending` using descriptive statistics.

## Technologies Used

*   **Python 3**
*   **Jupyter Notebook**
*   **Libraries:**
    *   `pymysql` / `mysql.connector`: For database connection.
    *   `pandas`: For data manipulation and analysis.
    *   `numpy`: For numerical operations.
    *   `matplotlib` & `seaborn`: For data visualization.

## Setup and Installation

To run this notebook locally, follow these steps:

1.  **Clone the repository:**
    ```bash
    git clone <your-repository-url>
    cd <repository-directory>
    ```

2.  **Create a Virtual Environment (Recommended):**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3.  **Install required packages:**
    ```bash
    pip install jupyter mysql-connector-python pandas matplotlib seaborn numpy
    ```

4.  **Database Configuration:**
    *   The notebook is configured to connect to a MySQL database at `127.0.0.1:3306`.
    *   You must have a MySQL server running with the `banking_case` database and the `customer` table.
    *   **Important:** Update the connection parameters in the notebook (`host`, `user`, `password`) to match your local or remote database setup.

5.  **Launch Jupyter Notebook:**
    ```bash
    jupyter notebook
    ```
    Open and run the `Banking- EDA Case Study.ipynb` notebook.

## Future Work

This EDA serves as a foundation. Potential next steps include:
*   **Deep-dive Analysis:** Investigating correlations between income, loyalty, and product usage.
*   **Customer Segmentation:** Using clustering algorithms (e.g., K-Means) to identify distinct customer groups.
*   **Predictive Modeling:** Building models to predict customer churn, credit risk, or product affinity.
*   **Dashboard Creation:** Developing an interactive dashboard (e.g., with Tableau or Power BI) to visualize key metrics for business users.

## Disclaimer

This is a case study using a synthetic dataset. The insights and code are for educational and demonstrative purposes. Always ensure compliance with data privacy and security regulations when working with real customer data.

---
