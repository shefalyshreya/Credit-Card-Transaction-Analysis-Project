# **CreditCard Transaction Analysis Project** #
# Table Of Content  #
1.[Description](#Descrption)

2.[FolderType](#FolderType)

3.[Dataset](#Dataset)

4.[DataExploration](#DataExploration)

5.[AdhocAnalysis](#AdhocAnalysis)

 # **Description** #
 
This project analyzes the Kaggle Credit Card Transactions dataset. It demonstrates:
- Exploratory Data Analysis (EDA) to understand patterns and distributions in the dataset
  
     - SQL queries for ad-hoc analysis and insights, including:
       
        - JOINs to combine multiple tables
        - GROUP BY / HAVING for aggregated analysis
        - Window functions for running totals and ranking
        - Subqueries and CTEs for complex calculations
        - Stored procedures for automated trend analysis and high-risk transaction detection
          
    - The analysis covers transactions by card type, expense type, city, gender, and time trends, helping identify usage patterns and high-risk behaviors.
 
 # **FolderType** #
  
CreditCardTransactions
 - StoredProcedure/  Key stored procedure for analysis
 - AdhocAnlaysis/ SQL queries to perform the analysis
 - DataExploration/  SQL scripts exploring the dataset
 - Dataset/ Raw CSV dataset
 - README.md  Project documentation  (file)

# **Dataset** #
File: credit_card_transactions.csv (https://www.kaggle.com/datasets/thedevastator/analyzing-credit-card-spending-habits-in-india)

Columns include:
- transaction_id – Unique identifier for each transaction
- city – City where transaction occurred
- transaction_date – Date of the transaction
- card_type – Card type: Gold, Platinum, Silver, Signature
- exp_type – Expense type: Bills, Food, Entertainment, Grocery, Fuel, Travel
- gender – Customer gender: Male/Female
- amount – Transaction amount
  
The dataset covers transactions from **2013-10-04 to 2015-05-26**.

# **Data Exploration** #

  DataExploration explore dataset properties:

- Transaction counts and uniqueness
- Date ranges and trends
- Distribution of card types and expense types
- Top cities by spend and transaction count
- Gender-based expense patterns
This helps understand behavior patterns before running advanced analysis.

# **Adhoc Analysis** #

The SQL scripts in the AdhocAnalysis/ folder include 9 analytical questions with their answers:


1. Top 5 cities with highest spends and their percentage contribution of total credit card spends.
2. Highest spend month and amount spent in that month for each card type.
3. Transaction details (all columns) for each card type when it reaches a cumulative of ₹1,000,000 total spends.
4. City with the lowest percentage spend for Gold card type.
5. City-wise expense pattern: Display 3 columns — city, highest_expense_type, lowest_expense_type.
   Example: Delhi | Bills | Fuel
6. Percentage contribution of spends by females for each expense type.
7. Card and expense type combination with the highest month-over-month growth in Jan-2014.
8. City with highest spend-to-transaction ratio during weekends.
9. City that reached its 500th transaction fastest after the first transaction in that city.

# **Summary** #

    - Provides combined summary and trend analysis for each card type and expense type by year
    - Flags high-risk transactions automatically (If more than 50% of transactions in a card type exceed the average amount for that card type, expense type and by year ,    flagging them 'High Risk'.)


  



