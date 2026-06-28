# Karnataka Workforce SQL Analytics using Databricks

## Overview

This project demonstrates SQL-based analytical exploration on a **Gold Layer dimensional data warehouse** built using the Medallion Architecture in Databricks.

Rather than analyzing raw data, the queries operate on a curated **Star Schema**, showcasing how a well-designed data warehouse can support business reporting and workforce analysis.

The project focuses on workforce statistics across Karnataka, exploring occupational distribution, industrial sectors, geographic trends, workforce demographics, and employment patterns using Spark SQL.

---

## Project Objectives

The primary objectives of this project are to:

* Demonstrate analytical querying on a dimensional data warehouse.
* Explore workforce trends using Spark SQL.
* Showcase business-oriented SQL techniques on fact and dimension tables.
* Generate actionable insights from curated Gold-layer datasets.

---

## Data Warehouse Overview

The SQL queries operate on the Gold layer of a Medallion Architecture data warehouse.

### Fact Tables

* `fact_occupation_workforce`
* `fact_industrial_workforce`

### Dimension Tables

* `dim_geography`
* `dim_occupation`
* `dim_community`
* `dim_worker_type`
* `dim_industry`

---

## Analytics Workflow

> *(Insert your Analytics Workflow diagram here)*

```
Gold Layer
      │
      ▼
Fact Tables + Dimensions
      │
      ▼
Spark SQL Queries
      │
      ▼
Aggregations & Business Logic
      │
      ▼
Business Insights
```

---

## Business Questions Explored

This project answers a variety of workforce-related business questions, including:

### Occupational Analysis

* Which occupations employ the largest workforce?
* Which occupations have the highest female participation?
* What are the dominant occupations among Scheduled Castes (SC)?
* What are the dominant occupations among Scheduled Tribes (ST)?

### Geographic Analysis

* Which districts have the largest workforce?
* Which districts have the highest female workforce participation?

### Demographic Analysis

* How is the workforce distributed between Scheduled Castes and Scheduled Tribes?
* What is the Rural vs Urban workforce distribution?

### Industrial Analysis

* Which industries employ the largest workforce?
* How are Main Workers and Marginal Workers distributed?
* Which industries dominate Bengaluru?
* How do industries vary across districts?

---

# SQL Techniques Demonstrated

The analysis makes extensive use of analytical SQL operations, including:

* INNER JOINs
* Aggregate Functions (`SUM`)
* GROUP BY
* ORDER BY
* Filtering (`WHERE`)
* Top-N Analysis (`LIMIT`)
* Fact-Dimension Joins
* Dimensional Modeling Queries
* Business Aggregations

---

# Query Categories

> *(Insert your Query Categories diagram here)*

```
                 SQL Analytics
                       │
        ┌──────────────┼──────────────┐
        │              │              │
 Occupation      Geography      Industry
        │              │              │
 Demographics   Workforce     Sector Analysis
```

---

# Analytical Queries

## Occupation Analysis

### 1. Top Occupations in Karnataka

**Objective**

Identify occupations employing the largest workforce.

**Tables Used**

* fact_occupation_workforce
* dim_occupation

**SQL Concepts**

* JOIN
* GROUP BY
* SUM
* ORDER BY
* LIMIT

**Key Insight**

Elementary occupations represent the largest workforce category, followed by craft and related trades.

---

### 2. Occupations with Highest Female Participation

**Objective**

Identify occupations with the highest female workforce participation.

**Key Insight**

Female participation is concentrated in elementary occupations, agriculture, and craft-related work.

---

### 3. Top Occupations among Scheduled Caste Workers

**Objective**

Understand occupational distribution within the Scheduled Caste workforce.

**Key Insight**

Elementary occupations dominate SC employment, followed by craft and agricultural occupations.

---

### 4. Top Occupations among Scheduled Tribe Workers

**Objective**

Analyze occupational trends among Scheduled Tribe workers.

**Key Insight**

Agriculture and elementary occupations constitute a significant portion of ST employment.

---

# Geographic Analysis

### 5. Top Districts by Workforce

**Objective**

Identify districts with the highest workforce participation.

**Key Insight**

Bengaluru contributes the largest district-level workforce within Karnataka.

---

### 6. Female Workforce Participation by District

**Objective**

Compare female workforce participation across districts.

**Key Insight**

Bengaluru records the highest female workforce participation, followed by Dakshina Kannada and Chikmagalur.

---

# Demographic Analysis

### 7. Scheduled Caste vs Scheduled Tribe Workforce

**Objective**

Compare workforce size across community categories.

**Key Insight**

The Scheduled Caste workforce is substantially larger than the Scheduled Tribe workforce in the available census data.

---

### 8. Rural vs Urban Workforce Distribution

**Objective**

Compare workforce participation across rural and urban regions.

**Key Insight**

The workforce distribution is relatively balanced between rural and urban populations.

---

# Industrial Analysis

### 9. Most Dominant Industries

**Objective**

Identify industries employing the highest number of workers.

**Key Insight**

Manufacturing, Trade, Construction, and Other Services collectively account for a significant share of employment.

---

### 10. Main Workers vs Marginal Workers

**Objective**

Compare employment by worker type.

**Key Insight**

Main workers represent the overwhelming majority of the workforce compared to marginal workers.

---

### 11. Top Industries in Bengaluru

**Objective**

Analyze Bengaluru's industrial employment profile.

**Key Insight**

Manufacturing, Trade, and Information & Communication sectors contribute significantly to Bengaluru's workforce.

---

### 12. Industry Specialization by District

**Objective**

Examine industry concentration across districts.

**Key Insight**

Manufacturing and Trade consistently appear among the largest employment sectors across Karnataka districts.

---

# Key Insights

The SQL analysis highlights several important workforce trends:

* Elementary occupations account for the largest share of Karnataka's workforce.
* Bengaluru is the largest workforce hub among all districts.
* Manufacturing and Trade are the state's dominant employment sectors.
* Female workforce participation is strongest in elementary, agricultural, and service occupations.
* Rural and Urban workforce participation is nearly balanced.
* Main workers significantly outnumber marginal workers.
* Occupational distributions differ between Scheduled Caste and Scheduled Tribe communities while sharing similar dominant occupation groups.

---

# Repository Structure

```
sql-workforce-analytics/
│
├── README.md
├── notebooks/
│   └── sql_gold_layer_analytics.sql
│
├── assets/
│   ├── analytics_workflow.png
│   ├── business_questions.png
│   ├── query_categories.png
│   └── query_pattern.png
│
└── outputs/
    └── sample_query_results.md
```

---

# Technologies Used

* Databricks
* Apache Spark SQL
* Delta Lake
* SQL
* Star Schema
* Medallion Architecture

---

# Future Enhancements

Potential extensions for this project include:

* Interactive Power BI or Tableau dashboards
* Time-series workforce trend analysis
* Additional demographic segmentation
* KPI dashboards for workforce analytics
* Advanced SQL analytics using window functions and Common Table Expressions (CTEs)

---

# Related Project

This analytics project is built on top of a separate **Databricks Medallion Data Warehouse** project, where the Bronze, Silver, and Gold layers, validation framework, and Star Schema were designed and implemented. This repository focuses exclusively on demonstrating the analytical capabilities enabled by that warehouse through Spark SQL.
