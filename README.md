# Palantir-CRM
My learnings to built a CRM application in Palantir Foundry

## Data Assets (input files)

orders_office_goods.csv

orders_bureau_transactional_system.csv

consolidated_customers.csv

### Project Setup

Create a new Project.

In Files, create a folder (e.g., raw/) and upload the three CSVs above.

### Transformations (high level)

Normalize column names

Make names consistent (e.g., lower_snake_case), trim spaces.

Cast date fields to timestamp

Convert all date/datetime columns to timestamp for consistent processing.

Join office goods ↔ bureau

Join the orders_office_goods and orders_bureau_transactional_system tables on their common columns (e.g., shared keys/fields).

Union the joined outputs

After aligning schemas and data types, union the two joined datasets to produce a consolidated view.

<img width="1381" height="522" alt="image" src="https://github.com/user-attachments/assets/f3579571-d56c-4849-af30-fd348e0c3897" />


### Finalize & run the pipeline

Validate schema/types, basic row-count checks, then run the pipeline to materialize outputs (all_orders).

Output of this phase: a curated dataset (all_orders) that merges office goods and bureau order data with consistent types and names.


