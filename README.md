# TransLink GTFS Data Warehouse

A medallion-style data engineering project built around the real TransLink GTFS feed.

## Goal

Build a clean warehouse pipeline from raw GTFS transit files to reporting-ready dimension and fact tables.

This project is designed to show practical data warehouse thinking:
- raw ingestion without losing source fidelity
- structured cleaning and validation
- fact and dimension modeling for analytics

## Architecture

### Bronze
Store the raw GTFS tables exactly as received from the source zip file.

### Silver
Clean and standardize the GTFS tables:
- normalize column names
- trim string fields
- cast numeric columns
- validate required keys
- derive helper tables such as trip stop counts

### Gold
Build warehouse tables for analysis:
- `dim_agency`
- `dim_route`
- `dim_stop`
- `dim_service`
- `dim_trip`
- `fact_trip_summary`
- `fact_stop_time`

## Source data

Use the real TransLink GTFS static feed and save it as:

```text
data/raw/google_transit.zip
```

## Project structure

```text
transit_data_warehouse/
├── README.md
├── requirements.txt
├── .gitignore
├── data/
│   ├── raw/
│   ├── bronze/
│   ├── silver/
│   ├── gold/
│   └── logs/
├── src/
│   ├── pipeline.py
│   ├── bronze/
│   │   └── ingest_gtfs.py
│   ├── silver/
│   │   └── transform_gtfs.py
│   ├── gold/
│   │   └── build_warehouse.py
│   └── common/
│       ├── config.py
│       ├── io.py
│       ├── logger.py
│       └── quality.py
└── tests/
    └── test_smoke.py
```

## Warehouse design

### Dimensions
- **dim_agency**: transit agency metadata
- **dim_route**: route attributes and display name
- **dim_stop**: stop metadata and location
- **dim_service**: service calendar rules
- **dim_trip**: trip-level operational attributes

### Facts
- **fact_trip_summary**: one row per trip with route, service, direction, and stop count
- **fact_stop_time**: one row per stop event within a trip

## How to run

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
python src/pipeline.py
```

## Good next steps

1. Add `calendar_dates.txt` handling for holiday and exception service.
2. Create a `dim_date` table and expand service dates.
3. Add route-level KPI marts such as trip counts by route and service day.
4. Add data quality logging for duplicate keys and invalid time values.
5. Move from pandas to PySpark later if you want a larger-scale version.
