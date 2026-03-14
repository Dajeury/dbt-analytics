# dbt Analytics
A dbt project built on BigQuery using the Jaffle Shop dataset as a foundation for practicing and demonstrating analytics engineering best practices — including staging models, data tests, documentation, and SQL linting.

## Project Structure
```
dbt-analytics/
├── models/          # Staging and mart models
├── seeds/           
├── macros/          # Reusable Jinja macros
├── analyses/       
├── snapshots/       
├── tests/           # Custom singular tests
├── dbt_project.yml  # Project configuration and flags
└── packages.yml     # dbt package dependencies
```

## Data Sources
This project uses the Jaffle Shop and stripe fictional e-commerce datasets, which includes:

- customers: customer records
- orders: order transactions with status tracking
- payments: payments per order

## Models
- Staging (models/staging/)
  Lightweight models that clean and rename raw source data. One model per source table.

- Marts (models/marts/)
  Fact and dimensional tables to be consumed by analysis tools (BI or ML)

## Data Tests
Tests are defined in YAML alongside the models and cover:

### Generic tests
- unique and not_null on primary keys
- accepted_values on status fields (e.g., placed, shipped, returned, completed, return_pending)
- relationships for referential integrity between models

### Singular tests
- custom sql tests adapted to a especific business case


## Tech Stack
- dbt (Data Build Tool)
- BigQuery
- SQL & sqlfluff
- Github / Git
- YML

Author
**Dajeury** — Data Analyst  
[github.com/Dajeury](https://github.com/Dajeury)
