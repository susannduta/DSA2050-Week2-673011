# DSA2050-Week2-673011
DSA 2050: Week 2 Practical Lab – SQL, Data Acquisition & Join Validation
**Student Name:** Susan Nduta Wanjiru
**Student ID:** 673011

## Objective

The objective of this lab is to practice relational data acquisition, SQL query execution, and join validation using Python, pandas, and SQLite. The practical demonstrates how raw data quality issues such as duplicate customer primary keys and unmatched order records can silently compromise analytical results by duplicating transactions and inflating aggregate sales totals during table joins. Through systematic reconciliation of row counts and control totals, deduplication of keys, and integration of JSON lookups, trustworthy KPIs were calculated across product categories, customer segments, and geographic regions.

## Key Findings

1. **Duplicate Keys Inflate Revenue:** A duplicate primary key (`C004`) in `customers.csv` caused a fan-out effect during a `LEFT JOIN`, increasing total order rows from 15 to 16 and artificially inflating sales from KSh 113,500 to KSh 122,600 until key deduplication was enforced.
2. **Corporate Segment Drives Highest Value:** The Corporate customer segment generated the highest revenue (KSh 46,800) and achieved the highest average order value (KSh 11,700), whereas the Retail segment drove order volume (6 orders) but yielded a lower average order value (KSh 4,933.33).
3. **Nairobi Leads Regional Sales with Data Limitations:** Nairobi produced the highest total regional sales at KSh 39,800 across 7 orders; however, management cannot conclude it is the best-performing region without accounting for dataset limitations such as missing profit margins/costs and a small sample size.
