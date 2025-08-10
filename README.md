🚲 Cyclistic Data Integration
Cleaning & Bike Usage Analysis


📌 Project Overview
This project explores Cyclistic bike-sharing service data by integrating large CSV files, cleaning and transforming them with Python, and performing SQL-based analysis to uncover usage patterns between annual members and casual riders.

The aim is to produce a clean, unified dataset ready for analysis and generate actionable insights to inform marketing strategies, service improvements, and operational planning.

🎯 Objectives
Python – Data Integration & Cleaning
Merge multiple large CSV files into a single dataset.

Handle missing values and remove duplicates.

Convert date/time columns into standardized formats.

Save the cleaned dataset for future analysis.

SQL – Bike Usage Analysis
Compare usage patterns of annual members vs. casual riders.

Analyze ride frequency, duration, and timing trends.

Understand preferred bike types and seasonal variations.

🛠️ Tools & Technologies
Python: Pandas, NumPy

PostgreSQL: SQL queries for analysis

Jupyter Notebook: Data preparation

CSV Files: Raw trip data

GitHub: Version control & documentation

📂 Dataset
Source: Cyclistic bike-sharing service database

Data Size: 12 CSV files (~1.7M rows each)

Key Columns:

ride_id

rideable_type (classic, electric, docked)

started_at, ended_at

start_station_name, end_station_name

member_casual (annual member or casual rider)

Geographic coordinates

🔄 Methodology
1. Python – Data Integration & Cleaning
Data Collection: Load all CSV files from the data directory.

Integration: Merge with pd.concat() into one DataFrame.

Cleaning:

Fill missing station names/IDs with "not specified".

Fill missing coordinates with -999.

Remove duplicate rows with .drop_duplicates().

Transformation:

Convert timestamps to datetime format.

Standardize column formats.

Export: Save as merged_data.csv.

2. SQL – Usage Pattern Analysis
Data Preparation:

Import merged_data.csv into PostgreSQL (COPY command).

Create derived columns:

Month, weekday, hour of day

Ride duration in minutes

Analysis Queries:

General Overview

Ride counts by rider type & bike type

Avg ride length per rider type

Total Rides Analysis

Rides by month, weekday, time of day

Ride Duration Analysis

Avg ride length by month, weekday, time of day

📊 Key Findings
General Overview
Electric bikes are most popular for both rider types.

Casual riders take longer rides than annual members.

Ride Frequency
Annual members ride more on weekdays, especially mornings & afternoons (commuting patterns).

Casual riders ride more on weekends & afternoons (leisure).

Ride Length
Annual members → Shorter rides (practical use).

Casual riders → Longer rides (recreational).

📌 Conclusion
Annual members use Cyclistic mainly for commuting.

Casual riders use Cyclistic mainly for leisure.

Insights can guide targeted marketing, pricing strategies, and bike allocation.
