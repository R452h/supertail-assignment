# 📊 Data Analyst Intern Assignment

## 📌 Overview

This project analyzes customer engagement and purchasing behavior using three datasets provided as part of the **Data Analyst Intern Assignment**.
The objective is to clean the data, build a **user engagement → purchase funnel**, and derive **actionable business insights** through analysis and visualization.



## 📁 Datasets Used

The analysis is based on three datasets covering a two-week period:

1. **Customers Data**

   * `customer_id`
   * `registered_date`
   * `city`
   * `acq_channel / acquisition_channel`

2. **Orders Data**

   * `order_id`
   * `customer_id`
   * `order_date`
   * `order_status`
   * `net_sales`
   * `disc%`

3. **Events Data**

   * `user_id`
   * `event_date` (YYYYMMDD format)
   * `event_name`



## 🧹 Data Cleaning & Preparation

The following steps were performed to prepare the data for analysis:

* Standardized column names (lowercase, underscore format)
* Converted date columns to proper datetime format
* Removed duplicate records from all datasets
* Renamed `user_id` to `customer_id` for consistency
* Ensured `customer_id` data type consistency across datasets
* Filtered **valid orders** using accepted successful statuses
  (`valid`, `completed`, `success`, `delivered`)
* Handled missing and invalid values safely to avoid runtime errors


## 🔄 User Engagement → Purchase Funnel

The funnel analysis evaluates how user engagement translates into purchases.

### Metrics Calculated:

* **Active Users**: Unique users who triggered at least one event
* **Ordering Users**: Unique users who placed at least one valid order
* **Conversion Rate**:

```
Conversion Rate = Ordering Users ÷ Active Users
```

### Visualization:

* A **time-series line chart** showing:

  * Daily active users
  * Daily ordering users

Defensive checks were added to ensure plots are only generated when data is available.



## 📈 Customer Behavior Insight

To understand customer purchasing behavior:

* Orders data was joined with customer data using `customer_id`
* Revenue was analyzed by **acquisition channel**
* A **bar chart** was created to visualize total revenue by channel

### Key Insight:

> The acquisition channel generating the highest total revenue contributes the most to overall sales.
> Focusing marketing efforts on this channel could significantly improve revenue performance.



## ⚠️ Assumptions

* Since the dataset did not consistently label successful orders as `"valid"`, commonly accepted successful statuses (`completed`, `success`, `delivered`) were treated as valid orders.
* Missing or malformed date values were safely ignored using coercion.



## 🛠 Tools & Technologies

* **Python**
* **Pandas** – data manipulation
* **Matplotlib** – data visualization
* **Jupyter Notebook / Google Colab**



## ✅ Deliverables

* Cleaned and prepared datasets
* Funnel metrics and conversion rate
* Time-series visualization of engagement vs orders
* Revenue analysis by acquisition channel
* Clear business insight and assumptions



## 📌 Conclusion

This project demonstrates a complete data analytics workflow including data cleaning, exploratory analysis, visualization, and insight generation.




