# Real Time Retail Data KPI Pipeline

### KPI Pipeline Architecture

![KPI Pipeline Architecture](https://github.com/santosh-gs/real-time-retail-kpi-pipeline/blob/main/images/kpi_pipeline_architecture.png?raw=true)


### Invoice Stream Schema

![Invoice Stream Schema](https://github.com/santosh-gs/real-time-retail-kpi-pipeline/blob/main/images/invoice_stream_schema.png?raw=true)


### Tasks
1. Reading the sales data from the Kafka server.
2. Preprocessing the data to calculate additional derived columns such as total_cost etc.
3. Calculating the time-based KPIs and time and country-based KPIs.
4. Storing the KPIs (both time-based and time- and country-based) for a 10-minute interval into separate JSON files for further analysis.  


### Data Dictionary
- Invoice number: Identifier of the invoice
- Country: Country where the order is placed
- Timestamp: Time at which the order is placed
- Type: Whether this is a new order or a return order
- SKU (Stock Keeping Unit): Identifier of the product being ordered
- Title: Name of the product is ordered
- Unit price: Price of a single unit of the product
- Quantity: Quantity of the product being ordered
