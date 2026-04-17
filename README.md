# cdc-databricks
databricks_cdc_project/
│
├── data/
│   └── cdc_sales.csv        ← dataset fake (CDC realista)
│
├── notebooks/
│   └── cdc_pipeline.py     ← pipeline completo
│
├── README.md               ← instruções


Volumes/
 └── main_cdc/
      └── default/
           ├── landing/sales/        (CSV original)
           ├── checkpoints/
           ├── schema/
           
Catalog:
 └── main_cdc
      ├── bronze.sales_raw
      ├── silver.sales_cdc
      └── gold.sales_analytics


Arquitetura Final:

Bronze (raw, CDC, append-only)
   ↓
Silver (tratado, deduplicado, merge/upsert)
   ↓
Gold (KPIs, agregações, consumo BI)
