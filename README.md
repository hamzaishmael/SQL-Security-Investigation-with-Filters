# SQL Security Investigation with Filters

## Overview

This project demonstrates how SQL can be used to support cybersecurity investigations by retrieving and analysing security-related data. The project was completed as part of the Google Cybersecurity Professional Certificate and focuses on using SQL filtering techniques to investigate suspicious login activity and identify employee systems requiring security updates.

Using the `AND`, `OR`, `NOT`, and `LIKE` operators, I queried organisational datasets to detect failed authentication attempts, investigate suspicious events, and retrieve employee information for security maintenance.

---

## Scenario

As a security analyst for a large organisation, I was tasked with investigating potential security incidents involving employee login attempts and organisational assets.

The investigation involved analysing two database tables:

* **log_in_attempts** – Contains authentication records such as login dates, login times, countries, and login success status.
* **employees** – Contains employee information including department and office location.

The objective was to retrieve relevant records using SQL filters to support security investigations and operational security tasks.

---

## Objectives

This project demonstrates how to:

* Investigate failed login attempts outside normal business hours.
* Review login activity surrounding a suspected security incident.
* Identify login attempts originating outside a specific country.
* Locate employee machines requiring security updates.
* Apply SQL filtering techniques commonly used by SOC analysts.
* Build efficient database queries using logical operators.

---

## SQL Skills Demonstrated

* SELECT statements
* WHERE clause
* AND operator
* OR operator
* NOT operator
* LIKE operator
* Wildcard (`%`) pattern matching
* Date filtering
* Time filtering
* Query optimisation through logical conditions

---

## Queries Included

### 1. Retrieve After-Hours Failed Login Attempts

Filters failed login attempts occurring after **18:00**.

**Concepts Used**

* AND
* Boolean filtering
* Time filtering

---

### 2. Retrieve Login Attempts on Specific Dates

Retrieves login attempts that occurred on **8 May 2022** or **9 May 2022**.

**Concepts Used**

* OR
* Date filtering

---

### 3. Retrieve Login Attempts Outside Mexico

Returns login attempts originating outside Mexico using pattern matching.

**Concepts Used**

* NOT
* LIKE
* Wildcard (%)

---

### 4. Retrieve Marketing Employees in East Offices

Identifies employees in the Marketing department located in East building offices.

**Concepts Used**

* AND
* LIKE
* Wildcard (%)

---

### 5. Retrieve Employees in Finance or Sales

Retrieves employees belonging to either the Finance or Sales departments.

**Concepts Used**

* OR

---

### 6. Retrieve Employees Not in Information Technology

Identifies employees who still require a scheduled security update.

**Concepts Used**

* NOT

---

---

## Sample SQL Query

```sql
SELECT *
FROM log_in_attempts
WHERE login_time > '18:00'
AND success = FALSE;
```

---

## Key Cybersecurity Concepts

* Authentication monitoring
* Security event investigation
* Log analysis
* Access monitoring
* Employee asset management
* Security maintenance
* Database querying for incident response

---

## What I Learned

Through this project, I strengthened my ability to use SQL as a cybersecurity investigation tool. I learned how to combine logical operators to retrieve specific records, use pattern matching with the `LIKE` operator, and efficiently analyse authentication logs and employee data. These are practical skills used by Security Operations Centre (SOC) analysts during threat investigations and routine security operations.

---

## Tools Used

* SQL
* Relational Database
* Google Cybersecurity Professional Certificate Lab

---
