# Uber_DashBoard
Info:-

Uber Operations Dashboard (Power BI)

A Power BI dashboard designed to analyze Uber ride operations and surface actionable insights across demand, supply, geography, and product performance. This project focuses on identifying peak periods, reducing cancellations, improving driver utilization, and supporting data-driven decisions for ops and city teams.

Features

Time intelligence
Peak demand by hour, weekday, and season
Trend analysis with rolling averages and period-over-period deltas
Geography and market mix
City/zone performance and under-served areas
Geo-visuals (maps and heatmaps) for demand concentration
Supply and operations
Driver utilization and wait times
Completion rate, ETA, and surge windows
Product analytics
Performance by category (e.g., UberX, UberXL, etc.)
Pricing and promo effectiveness comparisons
Quality and retention
Cancellation trends and root-cause indicators
Cohort-style views for repeat behavior

<img width="1325" height="783" alt="Screenshot 2025-08-19 204443" src="https://github.com/user-attachments/assets/ed63b139-f6d1-4b83-b2c8-b00148a6b9fb" />


Key Metrics (KPIs)
Total Trips
Active Drivers
Completion Rate
Average ETA / Wait Time
Cancellation Rate
Revenue / GMV
Trips by Product Type
Trips by City/Zone
Peak Hour / Busiest Day
Tip: These are placeholders; your PBIX may have additional or different KPIs. I can extract the exact set on request.

Pages and Interactions

<img width="1327" height="791" alt="Screenshot 2025-08-19 204505" src="https://github.com/user-attachments/assets/52f80509-835b-405c-b9ff-15bab81eb512" />


Overview: Executive KPIs with quick filters (time, city, product)
Demand Trends: Hourly/weekly seasonality, growth rates
Supply & Ops: Driver availability, utilization, wait/ETA, surge
Geography: City/zone heatmaps, top/bottom areas
Product Mix: Category performance, pricing and promo effects
Cancellations: Trend and drill-through diagnostics
Common interactions

Cross-highlighting across charts
Drill-through from summaries to detail
Bookmarks and tooltips for quick narratives

Data Model

Star schema with fact table(s) for trips and dimensions:
Date, City/Zone, Product, Driver, Rider (as available)
Time intelligence via a dedicated Date table with:
Year, Quarter, Month, Week, Day, Hour
IsWeekend, Season, Fiscal periods (if applicable)
DAX measures for KPIs, YoY/PoP, rolling windows, and segmentation
I can inspect the PBIX to document the exact tables, relationships, and DAX measures on request.

How to Customize

<img width="1323" height="789" alt="Screenshot 2025-08-19 204521" src="https://github.com/user-attachments/assets/aa2f04f9-38fb-49d5-8567-9fc554b59d14" />


Add/modify filters: Use Edit Interactions and Sync Slicers
Adjust KPIs: Create or edit DAX measures in the Model view
Add geospatial layers: Ensure latitude/longitude or well-formed geo fields
Performance tuning: Disable auto-date/time, reduce high-cardinality columns, use aggregations
Performance Tips
Prefer numeric surrogate keys for relationships
Summarize granular tables (e.g., by minute/hour) when appropriate
Limit expensive calculated columns; move logic to Power Query where possible
Use incremental refresh for large historical datasets
Avoid bi-directional filters unless necessary
