# Naming Conventions

This document defines the naming conventions used for schemas, tables, views, columns, and other objects in the data warehouse.

## Table of Contents

1. [General Principles](#general-principles)
2. [Table Naming Conventions](#table-naming-conventions)
   - [Bronze Rules](#bronze-rules)
   - [Silver Rules](#silver-rules)
   - [Gold Rules](#gold-rules)
3. [Column Naming Conventions](#column-naming-conventions)
   - [Surrogate Keys](#surrogate-keys)
   - [Technical Columns](#technical-columns)
4. [Stored Procedure](#stored-procedure)

---

## General Principles

- **Naming Convention:** Use `snake_case` with lowercase letters and underscores (`_`).
- **Language:** Use English for all names.
- **Reserved Words:** Avoid using SQL reserved words as object names.

## Table Naming Conventions

### Bronze Rules

- Table names start with the source system name and match the original source table names.
- **Pattern:** `<sourcesystem>_<entity>`
- **Example:** `crm_customer_info`

### Silver Rules

- Table names start with the source system name and match the original source table names.
- **Pattern:** `<sourcesystem>_<entity>`
- **Example:** `crm_customer_info`

### Gold Rules

- Table names use meaningful, business-aligned names with a category prefix.
- **Pattern:** `<category>_<entity>`
- **Examples:**
  - `dim_customers` → Customer dimension table.
  - `fact_sales` → Sales fact table.

| Pattern | Meaning | Example |
|---|---|---|
| `dim_` | Dimension table | `dim_customer`, `dim_product` |
| `fact_` | Fact table | `fact_sales` |
| `report_` | Report table | `report_sales_monthly` |

## Column Naming Conventions

### Surrogate Keys

- Primary keys in dimension tables use the suffix `_key`.
- **Pattern:** `<table_name>_key`
- **Example:** `customer_key`

### Technical Columns

- Technical columns use the `dwh_` prefix.
- **Pattern:** `dwh_<column_name>`
- **Example:** `dwh_load_date`

## Stored Procedure

Stored procedures used for loading data follow the pattern:

- **Pattern:** `load_<layer>`
- **Examples:**
  - `load_bronze` → Loads data into the Bronze layer.
  - `load_silver` → Loads data into the Silver layer.
  - `load_gold` → Loads data into the Gold layer.
