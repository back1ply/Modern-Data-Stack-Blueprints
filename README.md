# Modern Data Stack (MDS) Blueprints 🏗️

A curated collection of lean, modern, and cost-effective Data/BI stack implementations. 



This list focuses on Modern Data Stack (MDS) architectures optimized for Small to Medium Businesses (SMBs), solo data engineers, and highly performant portfolio projects. The emphasis is on battle-tested, classic ELT patterns that provide enterprise-grade robustness *without* requiring a dedicated Platform/DevOps team to maintain.

## 🛠️ Core MDS Technologies Featured
* **Storage/Compute:** Google BigQuery, AWS S3, Snowflake, DuckDB, MinIO, Apache Iceberg
* **Ingestion (EL):** dlt, Airbyte
* **Transformation/Semantic (T):** dbt (Core)
* **Orchestration:** Mage.ai, Dagster, Prefect, GitHub Actions
* **Visualization (BI):** Metabase, Looker Studio, Evidence.dev

---

## 🚀 The Pragmatic Cloud MDS (BigQuery / Snowflake / S3)
These repositories showcase the "Classic" cloud MDS architecture, but use lightweight orchestrators (like Mage or Dagster) instead of heavy Airflow setups to keep maintenance near zero.

* **[E-Commerce Profitability Pipeline (Real-World Use Case)](https://github.com/Snowboard-Software/dbt_airbyte_shopify_facebook_paypal_fedex_gls_ecommerce_profitability)**
  * **Stack:** Airbyte, BigQuery, dbt.
  * **Highlights:** A masterclass in real-world analytics engineering. It uses Airbyte to pull data from Shopify, Facebook Ads, and FedEx, dumps it into BigQuery, and uses dbt to model true business profitability (ROI, margins, shipping costs). 

* **[Airbyte + Dagster + dbt + BigQuery ELT](https://github.com/mustafa0taru/airbyte-dbt-dagster-bigquery-elt-pipeline)**
  * **Stack:** Airbyte, Dagster, dbt, BigQuery.
  * **Highlights:** The quintessential lean cloud stack. It flawlessly demonstrates how to use Dagster (a modern orchestrator) to trigger an Airbyte sync and then seamlessly run downstream dbt models in BigQuery.

* **[Dengue Public Health Data Pipeline](https://github.com/DNR258/de_dengue)**
  * **Stack:** Mage.ai, Google Cloud Storage (Data Lake), BigQuery, dbt, Looker Studio.
  * **Highlights:** A fantastic example of using cloud storage (GCS/S3) as a staging lake. It uses Mage to pull API data into Cloud Storage, loads it into BigQuery, transforms it with dbt, and visualizes the results in Looker Studio.

---

## 💻 Local-First & "Zero Cloud" Environments
Templates designed to run the classic MDS entirely on a single machine or cheap VPS using local storage and DuckDB to completely bypass cloud compute costs.

* **[Open-Source Lakehouse (Iceberg + dlt + dbt)](https://github.com/dlt-hub/workshop-iceberg-summit)**
  * **Stack:** dlt, MinIO, Apache Iceberg, dbt, DuckDB.
  * **Highlights:** An incredible blueprint for building a "Zero Cloud" Lakehouse. Uses `dlt` to extract API data and dump it into MinIO (a local S3 alternative), formats it with Apache Iceberg, and models it locally.

* **[Aviation Analytics Pipeline (dlt + DuckDB + dbt)](https://github.com/guidok91/duckdb-dbt)**
  * **Stack:** dlt, DuckDB, dbt, GitHub Actions.
  * **Highlights:** Pulls live flight data using `dlt`, stores and models it locally with DuckDB and `dbt`, and uses GitHub Actions for an incredibly lean, zero-cost CI/CD orchestration pipeline.

* **[Reproducible General Ledger](https://github.com/polarbear333/gl-pipeline)**
  * **Stack:** dbt, DuckDB, DVC, Metabase.
  * **Highlights:** An excellent example of modeling standard business ledger and financial transaction data cleanly within a lean, local MDS framework.

---

## 📊 Minimal Deployments & "BI-as-Code"
For when you want to cut out the noise, write code, and serve lightweight analytics.

* **[PyPI Duck Flow](https://github.com/mehd-io/pypi-duck-flow)**
  * **Stack:** Prefect, DuckDB, dbt, Metabase.
  * **Highlights:** A beautifully clean pipeline that pulls Python package download statistics from PyPI, orchestrates the ingestion with Prefect, models it locally in DuckDB, and visualizes the trends in Metabase.

* **[Nobel Prize Report (BI-as-Code)](https://github.com/tzelleke/nobel-prize-report)**
  * **Stack:** Python, dbt, DuckDB, Evidence.dev.
  * **Highlights:** Replaces traditional dashboards with "BI-as-code." Pulls from an API, transforms locally, and generates a blazing-fast, static Markdown/SQL website for analytics. 

---

## 📚 Architecture Guides & Must-Reads
Articles, blogs, and manifestos that define the lean Modern Data Stack philosophy.

* **[Building a Local Data Lake with DuckDB (Dagster)](https://dagster.io/blog/duckdb-data-lake)**
  * **Summary:** A brilliant architectural breakdown of how to bypass expensive cloud data warehouses by using DuckDB and Parquet files to create an "Embedded Data Lake."
* **[Big Data is Dead (MotherDuck)](https://motherduck.com/blog/big-data-is-dead/)**
  * **Summary:** The defining manifesto for the SMB data stack. It argues that most companies do not have "big data" and shouldn't be paying for architectures built for petabyte scale, championing the rise of leaner analytics engines.
* **[The Micro Data Stack (dltHub)](https://dlthub.com/blog/micro-data-stack)**
  * **Summary:** Explores how open-source, Python-native tools like `dlt`, `dbt`, and `DuckDB` have democratized data engineering, allowing single developers to build pipelines that previously required entire teams.

---

### How to use these Blueprints
1. **Fork/Clone:** Pick the architecture that best matches your SMB's scale or your portfolio's goals.
2. **Reverse Engineer:** Look specifically at how the folders are structured (`/ingestion`, `/models`, `/orchestration`).
3. **Swap the Source:** Replace the sample API or synthetic data script with your own pipelines connected to your actual business data sources.
