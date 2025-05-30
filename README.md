# DSA 2040A US 2025 LAB 2: OLTP + OLAP Integration

[![Build Status](https://img.shields.io/badge/build-passing-brightgreen)]()
[![License](https://img.shields.io/badge/license-MIT-blue)]()
[![Last Commit](https://img.shields.io/github/last-commit/yourusername/yourrepo)]()

---

## Table of Contents

- [Project Overview](#project-overview)
- [Repository Structure](#repository-structure)
- [Core Objectives](#core-objectives)
- [Technologies Used](#technologies-used)
- [Getting Started](#getting-started)
- [Normalization vs. Denormalization](#normalization-vs-denormalization)
- [Why Not Run Analytics Directly on OLTP?](#why-not-run-analytics-directly-on-oltp)
- [The Importance of ETL Automation](#the-importance-of-etl-automation)
- [Testing](#testing)
- [Known Issues](#known-issues)
- [Contributing](#contributing)
- [License](#license)


---

## Project Overview

This project simulates a real-world retail system by integrating Online Transaction Processing (OLTP) with Online Analytical Processing (OLAP). It focuses on:

- Designing a robust, normalized OLTP transactional database.
- Building an optimized OLAP star schema data warehouse.
- Implementing an efficient ETL (Extract, Transform, Load) pipeline.
- Running analytical queries to uncover critical business insights.

---

## Repository Structure

| Directory       | Description                                                       |
|-----------------|-------------------------------------------------------------------|
| `oltp_schema/`  | SQL scripts for creating the normalized OLTP transactional database. |
| `sample_data/`  | Sample CSV files and SQL scripts for populating OLTP tables.       |
| `olap_schema/`  | SQL scripts to build the denormalized OLAP star schema.            |
| `etl_scripts/`  | SQL scripts that perform the ETL process from OLTP to OLAP.        |
| `queries/`      | SQL scripts for running analytical queries on the OLAP database.  |
| `LICENSE`       | License details for project usage.                                 |
| `Question 5 Answers.docx` | Reflective answers to lab questions.                       |
| `README.md`     | This documentation file.                                           |

---

## Core Objectives

- **OLTP Schema Design:** Develop a normalized database optimized for day-to-day transactional operations.
- **OLAP Star Schema Construction:** Create a denormalized data warehouse optimized for fast analytical queries.
- **Seamless ETL Integration:** Extract, transform, and load data from OLTP to OLAP efficiently.
- **Analytical Query Execution:** Run diverse queries to analyze sales trends, product performance, and key business metrics.

---

## Technologies Used

- **SQL** — Schema definition, ETL processing, and complex querying.
- **Relational Database Management System** — PostgreSQL or MySQL recommended.
- Optional: Any SQL client for running scripts (e.g., pgAdmin, MySQL Workbench).

---

## Getting Started

### Prerequisites

- PostgreSQL 14+ or MySQL 8+
- SQL client tools installed
- Basic knowledge of SQL scripting

### Setup Steps

1. **Create OLTP Database**  
   Run SQL scripts inside `oltp_schema/` to create normalized transactional tables.

2. **Populate OLTP Data**  
   Use scripts or CSV files from `sample_data/` to seed the OLTP database.

3. **Create OLAP Data Warehouse**  
   Execute scripts in `olap_schema/` to build the star schema (fact and dimension tables).

4. **Run ETL Process**  
   Execute the ETL SQL scripts from `etl_scripts/` to transfer and transform data from OLTP to OLAP.

5. **Run Analytical Queries**  
   Use the scripts in `queries/` to perform analytical queries and extract business insights.

---

## Normalization vs. Denormalization

- **OLTP (Normalized):**  
  Designed for transactional integrity and efficient updates with minimal redundancy. Data is split into multiple related tables.

- **OLAP (Denormalized):**  
  Designed for fast querying and reporting. Data is combined into fewer wide tables to reduce complex joins.

---

## Why Not Run Analytics Directly on OLTP?

Running heavy analytical queries on OLTP systems causes:

- **Performance degradation** on transactional processing.
- **Resource contention** between transactions and analytical queries.
- **Data inconsistency** due to ongoing transactions.
- **Complex query design** due to normalized schema.
- **Limited historical analysis** because OLTP focuses on current data.

---

## The Importance of ETL Automation

Scheduled ETL pipelines provide:

- Timely and consistent updates to the OLAP warehouse.
- Reduced manual errors and operational overhead.
- Scalability to growing data volumes.
- Improved monitoring and auditability.
- Optimized resource usage by running during off-peak hours.

---

## Testing

To validate your setup:

- Run data consistency checks comparing OLTP and OLAP counts.
- Execute sample queries in the `queries/` folder and verify results.
- Optionally, use database-specific tools for integrity testing.

## Known Issues

- ETL scripts assume consistent data formats; manual adjustments may be needed for real-world irregularities.
- Performance may vary based on database tuning and hardware.

## Contributing

Contributions, issues, and feature requests are welcome! Feel free to:

- Fork the repo
- Open pull requests
- Submit issues

Please follow standard GitHub contribution guidelines.

## License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

