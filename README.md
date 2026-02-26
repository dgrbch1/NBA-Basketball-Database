🏀 NBA Data Warehouse

A fully designed and implemented SQL-based NBA Data Warehouse built to analyze player performance, team statistics, and game outcomes using advanced database concepts including stored procedures, business rules, triggers, transactions, and JSON processing.

📌 Project Overview

This project simulates a professional sports analytics backend system for NBA data. It integrates structured relational tables with automated logic and data integrity controls to support advanced reporting and analytics.

The system is designed following data warehousing principles and includes automation, validation rules, and transactional control to ensure data accuracy and consistency.

🗄️ Database Architecture
Core Tables

Players

Teams

Games

Player_Stats

Team_Stats

Coaches

Seasons

The schema supports relational joins, performance aggregation, and historical trend analysis.

⚙️ Key Features Implemented
✅ Stored Procedures

Insert and update player statistics

Calculate advanced metrics (PPG, FG%, Efficiency Rating)

Generate season summaries

Automate reporting queries

Stored procedures improve performance, enforce logic consistency, and centralize analytics calculations.

📏 Business Rules

Implemented strict business logic including:

A player must belong to one team per season

Game scores cannot be negative

A team must exist before a player can be assigned

Player stats cannot exist without a valid game record

Transactions must roll back if any rule fails

These rules ensure data integrity and prevent invalid inserts or updates.

🔔 Triggers

Triggers were created to automate validation and enforce constraints:

Prevent duplicate player entries

Automatically update team win/loss records after game insert

Log stat changes into an audit table

Restrict stat modifications after a game is marked as “Final”

Triggers help maintain automated database governance.

🔄 Transactions

Used transactions to maintain atomic operations:

BEGIN TRANSACTION

INSERT INTO Games ...
INSERT INTO Player_Stats ...

COMMIT;

If any step fails, the transaction rolls back to prevent partial or corrupted data.

📦 JSON Integration

Implemented JSON functionality to:

Export player performance summaries in JSON format

Store advanced stat breakdowns as structured JSON

Generate API-ready outputs for dashboards

Example use cases:

FOR JSON PATH

JSON data parsing for analytics dashboards

This allows seamless integration with front-end applications or BI tools.

📊 Analytics Capabilities

Player efficiency comparisons

Team performance trends

Season win/loss analysis

Game-by-game performance breakdown

Advanced metric calculations

The warehouse supports business intelligence tools like Power BI, Tableau, or custom dashboards.

🛠️ Technologies Used

Microsoft SQL Server

T-SQL

Stored Procedures

Triggers

Transactions

JSON Functions

Data Warehousing Design Principles

🎯 Learning Outcomes

Through this project, I demonstrated:

Advanced SQL development

Database automation and integrity enforcement

Transaction management

Business rule implementation

JSON data transformation

Real-world sports analytics modeling

🚀 Future Improvements

Implement SSIS ETL pipeline

Build SSRS reporting dashboards

Connect to live NBA API data

Add star schema optimization

Deploy to Azure SQL
