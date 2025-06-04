# sales-modeling

## Orginal Guide
### Business Goal

- Objective: Enable an e-commerce store to track revenue, top products, and monthly growth accurately.
- Key Insight: Clean, reliable data helps marketing and finance forecast sales and optimize inventory.

### Data & Dataset Description

- Data Source:
    - [UCI Online Retail Data](https://archive.ics.uci.edu/ml/datasets/online+retail)
    - [Kaggle E-Commerce Datasets](https://www.kaggle.com/datasets?search=ecommerce)
- Data Format: CSV with InvoiceNo, StockCode, Description, Quantity, InvoiceDate, UnitPrice, CustomerID.
- Data Details: Missing CustomerIDs, negative quantities (returns), inconsistent date/time formats.

### Expectations

1. **Ingest**
    - Download CSV from UCI/Kaggle, store locally or in cloud.
    - Load into Postgres using Python or an Airflow ingest task.
2. **Cleanse**
    - Fix negative Quantity for returns or exclude them if needed.
    - Convert InvoiceDate to a standard timestamp.
    - Remove duplicates or missing CustomerIDs where appropriate.
3. **Model in Postgres**
    - fact_sales: invoice number, product key, date key, customer key, quantity, total amount.
    - dim_product, dim_date, dim_customer for analytics.
4. **Orchestrate**
    - Airflow pipeline for monthly or weekly ingestion and transformations.
5. **Simple Dashboard**
    - Charts: daily/weekly revenue, top products, growth rate.
    - Use Case: marketing sees product performance, finance monitors revenue trends.


## Expanded Development Steps
0. **Set Up**
    - [x] Set up Github repo
    - [x] Add instructions to README and write out development steps
    - [x] Create venv
    - [x] Setup .gitignore
    - [ ] 
1. **Ingest**
    - [x] Download CSV from UCI/Kaggle, store locally or in cloud.
    - [ ] Load into Postgres using Python or an Airflow ingest task.
        - [x] Set up Docker and launch Postgres instance
        - [x] Set up DBeaver
        - [ ] Develop data ingest task
2. **Cleanse**
    - [ ] Fix negative Quantity for returns or exclude them if needed.
    - [ ] Convert InvoiceDate to a standard timestamp.
    - [ ] Remove duplicates or missing CustomerIDs where appropriate.
3. **Model in Postgres**
    - [ ] fact_sales: invoice number, product key, date key, customer key, quantity, total amount.
    - [ ] dim_product, dim_date, dim_customer for analytics.
4. **Orchestrate**
    - [ ] Airflow pipeline for monthly or weekly ingestion and transformations.
5. **Simple Dashboard**
    - [ ] Charts: daily/weekly revenue, top products, growth rate.
    - [ ] Use Case: marketing sees product performance, finance monitors revenue trends.