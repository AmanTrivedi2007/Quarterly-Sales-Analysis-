Quarterly Sales Analysis
A Python mini-project that turns raw order data into clear insights using pandas and Matplotlib. It highlights quarterly and monthly trends, top product lines (e.g., Classic Cars), country contributions, deal-size mix, average order value, and status-phase volumes, with concise charts and an easy handoff to dashboards or forecasting workflows.

Features
Robust CSV ingestion with multi-encoding fallback and schema checks for smooth local runs and portability.

Descriptive statistics and quick data profiling to validate ranges, nulls, and dtypes at a glance.

Business KPIs and segmentations: total sales, average order value, sales by quarter/month, product line, product code, country, and deal size.

Visuals in Matplotlib (bar and pie charts) for exploratory insights; structure is ready to extend into dashboards (e.g., Power BI).

Getting started
Prerequisites: Python 3.10+ with pandas, numpy, matplotlib installed; any Jupyter environment (Jupyter, VS Code) works well.

Optional: Power BI Desktop if extending to interactive dashboards later, following typical data-to-report handoffs.

Data: A CSV like sales_data_sample.csv with fields such as ORDERNUMBER, PRICEEACH, SALES, ORDERDATE, STATUS, PRODUCTLINE, PRODUCTCODE, COUNTRY, DEALSIZE.

Installation
Create a virtual environment and install packages:

pip install pandas numpy matplotlib

Open and run analysis.ipynb in Jupyter/VS Code; execute cells top-to-bottom to reproduce the EDA and charts.

Usage
Load the dataset (multi-encoding fallback is built in) and validate with df.info() and df.describe() to confirm schema.

Compute and visualize KPIs:

Sales by quarter and month, total sales, average order value.

Segment by country, product line/code, deal size; highlight top-performing segments.

Plot bar and pie charts as included in the notebook; adjust labels/rotation for readability as needed.

Extend to dashboards: export aggregates to CSV or connect a BI tool (e.g., Power BI) to the outputs for stakeholder-facing reports.

Repository structure
analysis.ipynb — core exploratory notebook with ingestion, profiling, KPIs, and visuals.

data/ (optional) — place the sales CSV here or update the path in the notebook’s loader cell.

outputs/ (optional) — exported CSVs or images for BI/reporting if desired.

Key insights produced
Overall metrics: total sales and average order value for the dataset period.

Time trends: quarterly and monthly sales distributions to spot seasonality and peaks.

Product and geography: product line/product code and country-level sales to identify mix and concentration.

Deal size and status: sales by Small/Medium/Large and order quantity by status-phase pie chart to assess pipeline distribution.

Roadmap
Add requirements.txt and an environment.yml for one-command setup on new machines.

Parameterize file paths via .env or a config cell to streamline re-runs across environments.

Export standardized aggregates (e.g., per month/country/product) for downstream BI or forecasting.

Optional: add lightweight tests (pytest) for schema and business-rule validations before charting.

Contributing
Keep cells modular (ingestion, profiling, KPIs, visuals) and comment non-obvious steps for maintainability.

Prefer small, purposeful plots; push advanced interactive visuals into BI/reporting tools for stakeholders.

Consider a CONTRIBUTING.md once the repo grows (style, commit messages, PR process).

Troubleshooting
UnicodeDecodeError on CSV load: the loader iterates encodings; add more or inspect source encoding if needed.

Missing columns: confirm dataset schema matches groupby keys; adjust fields in the aggregation cells.

Overlapping labels: increase figure size, rotate tick labels (plt.xticks(rotation=...)), or trim category names for clarity.

Jupyter rendering issues: ensure matplotlib is imported and an appropriate backend is active; restart kernel and re-run.
