# 🛡️ Investigating Security Issues Using SQL Filters

## 📝 Project Description

In this project, I used SQL to investigate potential security issues within an organization by querying login attempts and employee machine data. The main objective was to demonstrate the use of logical operators (`AND`, `OR`, `NOT`) and pattern matching (`LIKE`) to filter relevant data in real-world security scenarios. This project showcases my ability to work with structured query language (SQL) to support cybersecurity operations such as threat investigation and system auditing.

## 🧠 Skills Learned

- SQL query construction and logic filtering  
- Threat investigation using datasets  
- Pattern matching with `LIKE` and wildcards  
- Data analysis for login activity and employee information   

## 🛠️ Tools Used

<img src="https://img.shields.io/badge/SQL-025E8C?style=for-the-badge&logo=postgresql&logoColor=white" />

> *Queries and datasets were part of a simulated lab environment based on realistic security scenarios.*

## ✅ Project Steps

| **Task** | **Description** |
|----------|-----------------|
| **Retrieve after-hours failed login attempts** | Queried the `log_in_attempts` table for failed login attempts (`success = FALSE`) occurring after 18:00 using `AND` conditions. |
| **Retrieve login attempts on specific dates** | Retrieved all login attempts from `log_in_attempts` that occurred on `2022-05-09` or `2022-05-08` using the `OR` operator. |
| **Retrieve login attempts outside of Mexico** | Filtered out records from `log_in_attempts` where the country is not like `MEX%` using `NOT LIKE`. |
| **Retrieve employees in Marketing (East building)** | Queried the `employees` table to get employees from the Marketing department in offices starting with "East", using `AND` with `LIKE`. |
| **Retrieve employees in Finance or Sales** | Queried for employees from Finance or Sales departments using `OR` conditions. |
| **Retrieve employees not in IT** | Used `NOT` to filter out employees from the Information Technology department. |

## 📄 Project Report

### Description

My organization is working to make their system more secure. It is my job to ensure the system is safe, investigate all potential security issues, and update employee computers as needed. The following steps provide examples of how I used SQL with filters to perform security-related tasks.

### Retrieve after hours failed login attempts

There was a potential security incident that occurred after business hours (after 18:00). All after hours login attempts that failed need to be investigated.

The following code demonstrates how I created a SQL query to filter for failed login attempts that occurred after business hours.

<img width="824" alt="image" src="https://github.com/user-attachments/assets/66d3399b-72ac-47f9-a63e-867a43ddda66" />
<br></br>
The first part of the screenshot is my query, and the second part is a portion of the output. This query filters for failed login attempts that occurred after 18:00. First, I started by selecting all data from the `log_in_attempts` table. Then, I used a `WHERE` clause with an `AND` operator to filter my results to output only login attempts that occurred after 18:00 and were unsuccessful.

The first condition is `login_time > '18:00'`, which filters for the login attempts that occurred after 18:00. The second condition is `success = FALSE`, which filters for the failed login attempts.

### Retrieve login attempts on specific dates

A suspicious event occurred on 2022-05-09. Any login activity that happened on 2022-05-09 or on the day before needs to be investigated.

The following code demonstrates how I created a SQL query to filter for login attempts that occurred on specific dates.

<img width="821" alt="image" src="https://github.com/user-attachments/assets/c4cfe004-8361-4536-8ff4-3b0ff0b143c8" />
<br></br>
The first part of the screenshot is my query, and the second part is a portion of the output. This query returns all login attempts that occurred on 2022-05-09 or 2022-05-08. 

First, I started by selecting all data from the `log_in_attempts` table. Then, I used a `WHERE` clause with an `OR` operator to filter my results to output only login attempts that occurred on either 2022-05-09 or 2022-05-08. 

The first condition is `login_date = '2022-05-09'`, which filters for logins on 2022-05-09. The second condition is `login_date = '2022-05-08'`, which filters for logins on 2022-05-08.

### Retrieve login attempts outside of Mexico

After investigating the organization’s data on login attempts, I believe there is an issue with the login attempts that occurred outside of Mexico. These login attempts should be investigated.

The following code demonstrates how I created a SQL query to filter for login attempts that occurred outside of Mexico.

<img width="817" alt="image" src="https://github.com/user-attachments/assets/2c1e5ecd-9038-41cd-9f40-46b7d6dc4342" />
<br></br>
The first part of the screenshot is my query, and the second part is a portion of the output. This query returns all login attempts that occurred in countries other than Mexico. 

First, I started by selecting all data from the `log_in_attempts` table. Then, I used a `WHERE` clause with `NOT` to filter for countries other than Mexico. I used `LIKE` with `MEX%` as the pattern to match because the dataset represents Mexico as MEX and MEXICO. The percentage sign (`%`) represents any number of unspecified characters when used with `LIKE`.



## 💡 Reflections / Lessons Learned

This project enhanced my confidence in using SQL to support cybersecurity investigations. Understanding how to use logical and pattern-matching filters helped me simulate real-world use cases like identifying unauthorized access and segmenting users based on departmental criteria. These techniques are essential for data-driven security analysis and will be valuable in future roles within the field.
