# AngelOne-Stock-Trading-Platform-Database---MYSQL-PROJECT
AngelOne Stock Trading Platform Database - MYSQL PROJECT

AngelOne Stock Trading Platform Database
The AngelOne Stock Trading Platform Database is designed to support the operations of a stock trading platform, offering users the ability to buy and sell stocks, manage their portfolios, and track stock prices and transaction histories. This MySQL-based project organizes and stores the essential data required for a trading platform, ensuring smooth and efficient management of user accounts, stock transactions, portfolios.


ER DIAGRAM:

<img width="416" alt="image" src="https://github.com/user-attachments/assets/6c80ef9a-8683-4bcb-8a7a-314010335cc9" />









**Database Structure Overview:**

1. Users Table (Accounts)
Stores user details such as personal information, email, and available balance for trading.
Columns : user_id, name, email, phone, password, balance, created_at.

2. Stocks Table
Contains stock data, including stock symbols, company names, market sectors, and current prices.
Columns : stock_id, symbol, current_price, created_at.

3. Orders Table
Tracks buy and sell orders placed by users, including order type, quantity, and status.
Columns: order_id, user_id, order_type, quantity, price, order-status, created_at.

4. Transactions Table
Records completed transactions (buy/sell) for stocks, linking users and stocks with transaction details.
Columns: transaction_id, order_id, user_id, stock_id, quantity, price, transaction_type,
transaction_time.

5. Portfolio Table
Manages users' stock holdings, tracking the quantity of stocks each user owns.
Columns: user_id, stock_id, quantity.


**Summary of Relationships:**

Users → Orders: One user can place multiple orders (one-to-many).

Stocks → Orders: A stock can have multiple orders placed for it (one-to-many).

Orders → Transactions: One order can result in one or more transactions (one-to-many).

Users → Portfolio: A user can have a portfolio containing multiple stocks (one-to-many).

Stocks → Portfolio: A stock can be held by multiple users (one-to-many).

Technologies Used:

MySQL: The relational database management system used for storing and querying data.

SQL Queries: For retrieving stock prices, transaction history, and portfolio details.

Foreign Keys: Used to maintain data integrity across users, stocks, transactions, and portfolios.

Stored Procedures: Used for complex queries such as calculating portfolio values, fetching transaction history, and retrieving the most traded stocks.


Thank you 🤝
