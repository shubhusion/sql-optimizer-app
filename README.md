# SQL Optimizer Streamlit App

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://sql-optimizer.streamlit.app)
[![GitHub license](https://img.shields.io/github/license/shubhusion/sql-optimizer-app.svg)](https://github.com/shubhusion/sql-optimizer-app/blob/main/LICENSE)
[![GitHub issues](https://img.shields.io/github/issues/shubhusion/sql-optimizer-app.svg)](https://github.com/shubhusion/sql-optimizer-app/issues)
[![GitHub stars](https://img.shields.io/github/stars/shubhusion/sql-optimizer-app.svg)](https://github.com/shubhusion/sql-optimizer-app/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/shubhusion/sql-optimizer-app.svg)](https://github.com/shubhusion/sql-optimizer-app/network)

---

## Welcome to the SQL Optimizer Streamlit App! 🎉

This web application is designed to optimize and lint SQL queries effortlessly, leveraging the power of [**sqlglot**](https://github.com/tobymao/sqlglot) for optimization and [**sqlfmt**](http://sqlfmt.com) for linting.

---

## 🚀 Features

- **SQL Query Optimization:** Utilize various optimization rules from sqlglot to enhance the performance of your SQL queries.
- **SQL Query Linting:** Ensure your SQL queries adhere to best practices and conventions with sqlfmt.
- **Customizable Optimization Rules:** Tailor the optimization process according to your specific requirements.

---

## 🛠️ Usage

1. **Enter your SQL Query:** Input your SQL query in the left editor panel.
2. **Choose Optimization Rules:** Select the optimization rules you wish to apply from the available options.
3. **Preserve or Combine CTEs:** Decide whether to preserve Common Table Expressions (CTEs) or combine them.
4. **Linting Options:** Opt to lint your query with sqlfmt for adherence to coding standards.
5. **Optimize SQL:** Click the "Optimize SQL" button to see the optimized and linted SQL query in the right editor panel.

---

## 📋 Examples

Here's a sample query to illustrate the application of optimization rules:

```sql
WITH users AS (
    SELECT *
    FROM users_table),
orders AS (
    SELECT *
    FROM orders_table),
combined AS (
    SELECT users.id, users.name, orders.order_id, orders.total
    FROM users
    JOIN orders ON users.id = orders.user_id)
SELECT combined.id, combined.name, combined.order_id, combined.total
FROM combined
