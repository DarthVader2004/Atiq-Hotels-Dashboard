# 🏨 Atliq Hotels Business Dashboard – Power BI Project

## 📊 Overview
This project showcases a comprehensive **Business Intelligence Dashboard** for **Atliq Hotels**, created using **Microsoft Power BI**. The dashboard provides actionable insights into hotel operations, bookings, revenue, and room utilization across different properties and cities.

It utilizes 5 structured CSV datasets and one metrics documentation file to build visual, interactive reports that help stakeholders make data-driven decisions.

---

## 🧾 Project Objective
To analyze hotel performance, identify booking trends, and uncover revenue patterns by creating an interactive Power BI dashboard for hotel business executives and analysts.

---

## 📁 Files in the Repository

| File Name                        | Description |
|----------------------------------|-------------|
| `Atliq_Hotels_Dashboard.pbix`    | Main Power BI Dashboard file |
| `dim_date.csv`                   | Date dimension for time-series analysis |
| `dim_hotels.csv`                 | Hotel property details |
| `dim_rooms.csv`                  | Room types and categories |
| `fact_aggregated_bookings.csv`   | Aggregated booking information |
| `fact_bookings.csv`              | Detailed individual bookings |
| `metrics list.xlsx`              | Documentation of metrics/KPIs used |

---

## 🧱 Data Model (Star Schema)
The dashboard is built using a **star schema**, comprising **3 dimension tables** and **2 fact tables**:

### 🔹 Dimension Tables
1. **`dim_date`** – Date-level granularity for time-based filtering (e.g., month, week, day type).
2. **`dim_hotels`** – Metadata about hotel properties (name, category, city).
3. **`dim_rooms`** – Classification of rooms (type and class).

### 🔸 Fact Tables
1. **`fact_bookings`** – Contains granular, transaction-level booking details.
2. **`fact_aggregated_bookings`** – Aggregated summary of bookings per room per date, optimized for performance-based visuals.

---

## 📐 Column Metadata

### `dim_date`
| Column        | Description |
|---------------|-------------|
| `date`        | Dates from May to July |
| `mmm yy`      | Month-Year format (e.g., May 23) |
| `week no`     | Week number of the year |
| `day_type`    | Weekend or Weekday |

### `dim_hotels`
| Column         | Description |
|----------------|-------------|
| `property_id`   | Unique ID for each hotel |
| `property_name` | Hotel name |
| `category`      | Hotel class: Business or Luxury |
| `city`          | City where hotel is located |

### `dim_rooms`
| Column        | Description |
|---------------|-------------|
| `room_id`     | Room type (RT1 to RT4) |
| `room_class`  | Class (Standard, Elite, Premium, Presidential) |

### `fact_aggregated_bookings`
| Column             | Description |
|--------------------|-------------|
| `property_id`       | Hotel ID |
| `check_in_date`     | Check-in date |
| `room_category`     | Room type |
| `successful_bookings` | Number of confirmed bookings |
| `capacity`          | Total room availability |

### `fact_bookings`
| Column             | Description |
|--------------------|-------------|
| `booking_id`        | Unique booking transaction ID |
| `property_id`       | Hotel ID |
| `booking_date`      | Date of booking |
| `check_in_date`     | Guest check-in date |
| `check_out_date`    | Guest check-out date |
| `no_guests`         | Number of guests |
| `room_category`     | Room type |
| `booking_platform`  | Booking channel used |
| `ratings_given`     | Customer service rating |
| `booking_status`    | Booking outcome (Cancelled, Checked Out, No show) |
| `revenue_generated` | Total revenue before refund |
| `revenue_realized`  | Final revenue after deductions |

---

## 📈 Key Metrics Visualized

Based on the `metrics list.xlsx` and dashboard analysis, the following KPIs are visualized:
- Total Bookings and Trends
- Revenue Generated vs. Realized
- Booking Status Distribution
- City-wise and Property-wise Performance
- Room Category Performance
- Average Rating per Property
- Weekend vs Weekday Booking Trends

---

## ⚙️ Technical Details

- **Tool Used:** Microsoft Power BI Desktop
- **Data Source:** Static CSV files (loaded into Power BI model)
- **Model Type:** Import Mode with Data Transformation using Power Query
- **DAX Used For:**
  - Calculating revenue insights
  - Status-based filters
  - Custom date aggregations (MMM YY, week no)
- **Power Query Used For:**
  - Cleaning column names
  - Merging room and hotel metadata
  - Creating normalized dimension tables

---

## 📌 Highlights of the Dashboard

- Interactive filters for cities, room types, and months
- Drill-down capabilities for revenue and booking trends
- Clean UX design with separate pages for:
  - Summary overview
  - Room analysis
  - Property analysis
  - Revenue performance

---

## 💡 Insights Drawn
- Weekends show higher booking activity and realized revenue
- Business hotels in Tier-1 cities outperform luxury hotels in occupancy
- Presidential and Premium rooms contribute disproportionately to revenue
- High cancellation rates from a specific booking platform identified

---

## 🧠 Learnings & Takeaways
- Designed an optimized star schema for reporting
- Learned effective DAX for revenue logic based on booking status
- Used slicers, bookmarks, and KPI cards for enhanced UX
- Employed Power BI best practices for modeling and visualization

---

## 🚀 How to Use
1. Download the repository.
2. Open the `Atliq_Hotels_Dashboard.pbix` file using **Power BI Desktop**.
3. Explore dashboard pages and interact with filters for analysis.
4. Refer to `metrics list.xlsx` and CSV files for understanding data structure.

---

## 📮 Contact
Created by **Aruj Singhvi**  
For questions or suggestions, feel free to reach out via (https://github.com/DarthVader2004).

