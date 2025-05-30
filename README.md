# DSA 2040A US 2025 LAB 2: OLTP + OLAP Integration

[![Build Status](https://img.shields.io/badge/build-passing-brightgreen)](https://github.com/aykahsay)
[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Last Commit](https://img.shields.io/github/last-commit/aykahsay/DSA2040-LAB2)](https://github.com/aykahsay/DSA2040-LAB2/commits)

## 📚 Table of Contents

- [🧠 Project Overview](#-project-overview)
- [🗂️ Repository Structure](#️-repository-structure)
- [🎯 Core Objectives](#-core-objectives)
- [🚀 Getting Started](#-getting-started)
- [🔄 Normalization vs. Denormalization](#-normalization-vs-denormalization)
- [❓ Why Separate OLTP and OLAP?](#-why-separate-oltp-and-olap)
- [⏱️ Automation & ETL Scheduling](#️-automation--etl-scheduling)
- [🧪 Testing](#-testing)
- [🐞 Known Issues](#-known-issues)
- [🤝 Contributing](#-contributing)
- [👥 Team Members](#-team-members)
- [📄 License](#-license)

---


## 🧠 Project Overview

This project simulates a real-world retail system integrating an Online Transaction Processing (OLTP) system with an Online Analytical Processing (OLAP) system.

The objective is to:
- Design normalized OLTP schemas
- Construct an OLAP star schema
- Implement ETL (Extract, Transform, Load)
- Run OLAP queries for insights

---

## 🗂️ Repository Structure

- [`etl_scripts/`](etl_scripts) — SQL ETL scripts (e.g., `dim_date` population)
- [`olap_schema/`](olap_schema) — OLAP star schema creation
- [`oltp_schema/`](oltp_schema) — OLTP normalized database setup
- [`queries/`](queries) — Analytical SQL queries on the OLAP DB
- [`sample_data/`](sample_data) — CSV files and sample data loaders
- [`LICENSE`](LICENSE) — MIT License
- [`Ass2.pdf`](Ass2.pdf) — Assignment / Question Paper
- [`Question 5 Answers.pdf`](Question%205%20Answers.pdf) — Written reflections and answers

---

## 🎯 Core Objectives

- **OLTP Design:** Create normalized transactional schemas
- **OLAP Modeling:** Build efficient star schema for analytics
- **ETL Workflow:** Automate data transfer and transformation
- **Analytics:** Run insightful business queries

---

## 🛠️ Technologies Used

- **SQL** — Schema definition, ETL, querying
- **PostgreSQL / MySQL** — Database engines
- **CSV** — Sample data files

---

## 🚀 Getting Started

### ✅ Step 1: Build OLTP  
Use [`oltp_schema/`](oltp_schema) to create normalized tables (e.g., `customers`, `products`, `stores`, `transactions`).

### ✅ Step 2: Populate OLTP Data  
Load data from [`sample_data/`](sample_data).

### ✅ Step 3: Build OLAP Star Schema  
Use [`olap_schema/`](olap_schema) for `fact_sales`, `dim_date`, etc.

### ✅ Step 4: Run ETL  
Transform and load data using scripts in [`etl_scripts/`](etl_scripts).

### ✅ Step 5: Perform Analysis  
Use queries in [`queries/`](queries) to generate insights.

---
## Reflection
### 🔄 Normalization vs. Denormalization

| OLTP (Normalized) | OLAP (Denormalized) |
|------------------|---------------------|
| 3NF Design        | Star Schema         |
| Write-heavy       | Read-heavy          |
| Data integrity    | Query performance   |

---

### ❓ Why Separate OLTP and OLAP?

- ✅ Avoids performance bottlenecks
- ✅ Ensures transactional stability
- ✅ Enables historical trend analysis
- ✅ Allows for complex reporting

---

### ⏱️ Automation & ETL Scheduling

Benefits of automated ETL:

- 📅 Timely data refresh
- 📉 Reduces human error
- 🔁 Continuous integration of new data
- 🧩 Supports data pipelines

  #### For more information visit [`Question 5 Answers.pdf`](Question%205%20Answers.pdf) — Written reflections and answers
---

## 🧪 Testing

- ✔️ Validate row counts between OLTP and OLAP
- ✔️ Confirm dimensions align with expected records
- ✔️ Run queries from [`queries/`](queries) and inspect results

---

## 🐞 Known Issues

- ETL requires tweaks for edge cases
- Query performance may depend on indexes or hardware
- Potential duplicate handling in sample data

---

## 🤝 Contributing

We welcome contributors!

1. Fork the repo
2. Create a feature branch
3. Submit a pull request with a clear description
4. Mention relevant issues or suggestions

---

## 👥 Team Members

| Name | GitHub | Student ID |
|------|--------|------------|
| Misati Nyambane | [@mistiusiu](https://github.com/mistiusiu) | 670145 |
| Justice Chawanda | [@jpchawanda1](https://github.com/jpchawanda1) | 670444 |
| Samuel Abrha | [@SamAbr](https://github.com/SamAbr) | 670533 |
| Paul Mbuvi | [@paulmbuvi](https://github.com/paulmbuvi) | 669984 |
| Cynthia Gathogo | [@cngathogo](https://github.com/cngathogo) | 668745 |
| Ambachow Kahsay | [@aykahsay](https://github.com/aykahsay) | 670550 |

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---
