# Dockerized Vacation & Skipass Management System

## 🏢 Project Overview
A comprehensive, containerized database solution developed as part of the **Informatics** curriculum at **IMC University of Applied Sciences Krems**. The project manages complex vacation reservations and real-time skipass telemetry data using a multi-database architecture.

## 🚀 Key Features
- **Relational Data Management:** Full MariaDB implementation for customer profiles, reservations, and payment packages.
- **Time-Series Telemetry:** Integrated **TimescaleDB (PostgreSQL)** to handle high-frequency skipass scan data.
- **Performance Optimization:** Utilized **Hypertables** and **Continuous Aggregates** to provide fast, pre-aggregated daily scan totals for ski resorts.
- **Automated Workflows:** Python-based simulation scripts to generate telemetry data and execute complex business queries.

## 🛠 Tech Stack
- **Databases:** MariaDB, TimescaleDB (PostgreSQL)
- **Containerization:** Docker & Docker Compose
- **Programming:** Python 3.11
- **Querying:** SQL (Relational & Time-series)

## 📁 Project Structure
- `docker-compose.yml`: Defines the database, setup, and query services.
- `init_db.py`: Automated schema loading and sample data insertion.
- `timescale/`: Advanced telemetry scripts, including hypertable creation and scan simulations.
- `queries.sql`: Pre-defined business queries for ROI and reservation analytics.

## ⚙️ Setup & Installation
1. **Clone the repo:** `git clone [link]`
2. **Launch Services:** `docker-compose up --build`
3. **Initialize Telemetry:** `docker exec -i timescaledb psql -U pguser -d vacation_pg < timescale/pg_schema.sql`
4. **Run Analytics:** `docker run --rm [options] python query_aggregates.py`

## 👥 Collaborators
This project was developed as a team assignment at **IMC University of Applied Sciences Krems**.
- **Timur Selivanov** (Data Simulation & TimescaleDB logic)
- **Artur Volkov** (MariaDB Schema & SQL Queries)
