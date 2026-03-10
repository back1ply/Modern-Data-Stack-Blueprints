# Modern Data Stack (MDS) Blueprints 🏗️

A curated collection of lean, modern, and cost-effective Data/BI stack implementations. 



This list focuses on Modern Data Stack (MDS) architectures optimized for Small to Medium Businesses (SMBs), solo data engineers, and highly performant portfolio projects. The emphasis is on open-source, local-first, or serverless tools that provide enterprise-grade robustness without the enterprise price tag.

## 🛠️ Core MDS Technologies Featured
* **Storage/Compute:** DuckDB, MotherDuck, BigQuery, MinIO, Apache Iceberg
* **Ingestion (EL):** dlt, Airbyte, Prefect
* **Transformation/Semantic (T):** dbt (Core), SQLMesh, Cube
* **Orchestration:** Dagster, Mage.ai, Prefect
* **Visualization (BI):** Metabase, Evidence.dev, Streamlit, Apache Superset

---

## 🚀 End-to-End Orchestrated Pipelines
These repositories demonstrate complete MDS lifecycles, from extracting raw data to serving it in a dashboard, wired together with modern orchestrators.

* **[PyPI Duck Flow](https://github.com/mehd-io/pypi-duck-flow)**
  * **Stack:** Prefect, DuckDB, dbt, Metabase.
  * **Highlights:** A beautifully clean pipeline that pulls Python package download statistics from PyPI, orchestrates the ingestion with Prefect, models it locally in DuckDB, and visualizes the trends. 

* **[Dagster + dlt + dbt + DuckDB SDLC](https://github.com/jairus-m/dagster-sdlc)**
  * **Stack:** Dagster, dlt, dbt-core, DuckDB, Snowflake.
  * **Highlights:** Treats data like software. Excellent showcase of a complete Software Development Life Cycle (SDLC) with dev/staging/prod environments.

* **[Tech Career Explorer](https://github.com/shayansm2/tech-career-explorer)**
  * **Stack:** Mage.ai, dbt, DuckDB, Postgres, Metabase.
  * **Highlights:** A highly practical, real-world pipeline processing scraped web data and pushing clean metrics to a Metabase dashboard.

* **[vTasks: Personal Data Pipeline](https://github.com/villoro/vtasks)**
  * **Stack:** Prefect, MotherDuck, dbt, Metabase.
  * **Highlights:** A perfect standard SMB blueprint. Extracts from APIs/Sheets, utilizes cloud-hosted MotherDuck, and serves via Metabase.

* **[Reproducible General Ledger](https://github.com/polarbear333/gl-pipeline)**
  * **Stack:** dbt, DuckDB, DVC, Metabase.
  * **Highlights:** An excellent example of modeling standard business ledger and financial transaction data cleanly within an MDS framework.

---

## 💻 Local-First & "Zero Cloud" MDS Environments
Templates designed to run a massive data operation entirely on a single machine with zero cloud compute costs.

* **[Orca - A Modern Data Platform](https://github.com/mathisdrn/orca)**
  * **Stack:** dbt, DuckDB (highly modular).
  * **Highlights:** A polished "reference implementation" framework for a modern open-source platform. Built to integrate easily with agentic AI workflows.

* **[SBDK (Single Binary Data Kit)](https://github.com/sbdk-dev/sbdk-dev)**
  * **Stack:** dlt, DuckDB, dbt.
  * **Highlights:** An incredibly fast toolkit built on Python foundations. Generates synthetic data and runs transformations with a single CLI command.

* **[Local Modern Data Stack (MDS)](https://github.com/l-mds/local-data-stack)**
  * **Stack:** Dagster, dbt, DuckDB.
  * **Highlights:** A cookiecutter boilerplate to instantly generate a working data environment, complete with built-in secret management (SOPS) and testing.

* **[NBA Monte Carlo Simulator](https://github.com/matsonj/nba-monte-carlo)**
  * **Stack:** dbt, DuckDB, Evidence.dev.
  * **Highlights:** A legendary proof-of-concept simulating an NBA season. Proves you can run computationally heavy models entirely locally and serve them via a static site.

---

## 📊 Minimal MDS & "BI-as-Code" Deployments
For when you want to cut out the noise, write code, and serve lightweight analytics.

* **[Nobel Prize Report (BI-as-Code)](https://github.com/tzelleke/nobel-prize-report)**
  * **Stack:** Python, dbt, DuckDB, Evidence.dev.
  * **Highlights:** Replaces traditional dashboards with "BI-as-code." Pulls from an API, transforms locally, and generates a blazing-fast, static Markdown/SQL website for analytics. 

* **[Mimosa (Minimal MDS)](https://github.com/EJOOSTEROP/mimosa)**
  * **Stack:** dbt, MotherDuck, Docker.
  * **Highlights:** Cuts out heavy orchestration logic to show exactly how to wire dbt directly to MotherDuck for the leanest possible cloud deployment inside a single container.

---

## 🐳 Containerized Data Platforms
* **[Portable Data Stack with SQLMesh](https://github.com/cnstlungu/portable-data-stack-sqlmesh)**
  * **Stack:** Docker, DuckDB, dbt-core, SQLMesh, Apache Superset.
  * **Highlights:** A fully portable Datamart and BI suite. Shows how to containerize an entire SMB data architecture for easy deployment on a single cheap cloud instance.

---

## 📖 Real-World Case Studies & Dev Journals
Learn from the trenches. These articles detail the exact hurdles engineers faced when building these lean stacks.

* **[My Journal: Dagster + dlt + DuckDB (by Wambui Gitau)](https://medium.com/@ywg/my-journal-dagster-dlt-duckdb-part-1-15051f20e597)**
  * **Summary:** A brilliant, transparent 3-part series detailing the friction points of setting up this specific stack (like dealing with DuckDB's single-write locks during ingestion) and how to overcome them.
* **[Building a Production-Grade, Serverless EV Data Pipeline (by Nitish Karekar)](https://medium.com/@nitishkarekar/first-elt-project-364dec0ca259)**
  * **Summary:** A fantastic blueprint for using GCP Cloud Functions for defensive ingestion, GitHub Actions for orchestration, and MotherDuck/dbt for compute, served finally on Streamlit.

---

## 📚 Architecture Guides & Must-Reads
Articles, blogs, and manifestos that define the lean Modern Data Stack philosophy.

* **[Lean Data Stack with dlt, DuckDB, DuckLake, and dbt (Datacoves)](https://datacoves.com/post/dbt-duckdb)**
  * **Summary:** An excellent architectural breakdown of separating ingestion, storage, and transformation, introducing "DuckLake" to turn local Parquet files into a true lakehouse.
* **[8 ways to flex DuckDB (Tasman Analytics)](https://tasman.ai/news/8-ways-to-flex-duckdb)**
  * **Summary:** Explores advanced, real-world DuckDB use cases, including using it as a multi-engine stack connector and querying raw JSON/CSV files seamlessly.
* **[Building a Local Data Lake with DuckDB (Dagster)](https://dagster.io/blog/duckdb-data-lake)**
  * **Summary:** A brilliant architectural breakdown of how to bypass expensive cloud data warehouses by using DuckDB and Parquet files to create an "Embedded Data Lake."
* **[Big Data is Dead (MotherDuck)](https://motherduck.com/blog/big-data-is-dead/)**
  * **Summary:** The defining manifesto for the SMB data stack. It argues that most companies do not have "big data" and shouldn't be paying for architectures built for petabyte scale, championing the rise of DuckDB.

---

### How to use these Blueprints
1. **Fork/Clone:** Pick the architecture that best matches your SMB's scale or your portfolio's goals.
2. **Reverse Engineer:** Look specifically at how the folders are structured (`/ingestion`, `/transform`, `/orchestration`).
3. **Swap the Source:** Replace the sample API or synthetic data script with your own `dlt` pipeline connected to your actual data sources.
