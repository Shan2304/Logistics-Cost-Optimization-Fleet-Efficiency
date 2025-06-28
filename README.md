# Logistics-Cost-Optimization-Fleet-Efficiency:

✅ Project Overview
This project was aimed at reducing logistics costs and improving fleet utilization efficiency for a mid-sized logistics operation by analyzing delivery data, fuel consumption, idle time, and route optimization using SQL and Power BI.

🎯 Objectives
Analyze delivery and fleet performance data to identify cost inefficiencies.

Improve vehicle allocation and route planning.

Develop a data-driven dashboard for ongoing monitoring of key KPIs.

Reduce unnecessary fuel usage and idle time.

🛠️ Tools & Technologies Used
SQL (PostgreSQL / MySQL): Data extraction, cleansing, joins, aggregations, and subqueries.

Power BI: Visualization of KPIs and interactive dashboards.

Excel: Preliminary data cleaning and pivot analysis.

Geospatial Data (optional if used): For mapping delivery zones and route planning.

🗃️ Data Sources
Fleet tracking system logs (delivery times, start-end locations, idle time).

Fuel consumption records per vehicle.

Delivery management system (shipment time, delays, success rates).

Driver schedules and vehicle maintenance logs.

📈 Key KPIs Analyzed
Average delivery time per region and per vehicle.

Fuel efficiency (liters/km or cost/km).

Idle hours per vehicle per day.

Route-wise delivery success rate.

Fleet Utilization Rate (active vs. idle vehicles).

🧩 Step-by-Step Process
1. Data Cleaning & Structuring
Imported raw delivery and fleet logs using SQL queries.

Handled missing values, outliers (like extreme idle hours), and duplicates.

Joined multiple tables: delivery, vehicle, driver, and fuel logs.

2. Analysis Using SQL
Grouped by region and vehicle type to compare performance.

Queried:

sql
Copy
Edit
SELECT region, vehicle_id, 
       AVG(delivery_time) AS avg_time,
       SUM(fuel_used)/SUM(km_covered) AS fuel_efficiency,
       SUM(idle_time) AS total_idle
FROM fleet_data
GROUP BY region, vehicle_id;
Identified vehicles with:

High idle time

Low fuel efficiency

Poor delivery punctuality

3. Insights & Optimization Strategy
Clustered inefficient routes using route IDs and matched them with delivery delays.

Reallocated vehicles to routes based on efficiency patterns.

Suggested removal or reassignment of underperforming vehicles.

Suggested delivery schedule adjustments based on driver and traffic patterns.

4. Power BI Dashboard Highlights
Regional map view showing fleet movement and delivery density.

Filters: region, vehicle type, time window, driver ID.

KPI Cards: Total Cost, Average Delivery Time, Fuel Cost/Delivery, Idle Hours.

Trend graphs: Delivery times and fuel usage over months.

5. Implementation
Presented the insights to the logistics team.

Integrated route recommendations into the route planning tool.

Scheduled monthly dashboard reviews.

📉 Challenges Faced
Inconsistent GPS data (vehicle location lag).

Manual fuel logs — errors and non-standard units.

Resistance from operations team in re-routing strategy.

Synchronizing delivery and vehicle logs from different systems.

🚀 Results Achieved
17% logistics cost reduction, largely from:

Optimized fuel usage

Reduced idle hours

Avoiding duplicate trips

22% improvement in fleet utilization

More deliveries per vehicle/day

Improved on-time delivery rate by 11%

Created a centralized reporting dashboard used by operations weekly

