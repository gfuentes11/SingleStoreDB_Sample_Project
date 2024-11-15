# Global Terrorism Data Analysis with SingleStoreDB

This project demonstrates how to use SingleStoreDB to analyze global terrorism data, providing real-time insights and trend analysis. From creating a synthetic dataset to building a Tableau dashboard, this project showcases how SingleStore’s high-performance capabilities optimize data ingestion, processing, and visualization for large datasets, tailored specifically for defense applications.

## Project Overview

This project was designed to:
- Simulate and ingest synthetic global terrorism data.
- Perform analytical queries optimized by shard and sort keys.
- Generate insights for defense-related threat detection and situational awareness.
- Visualize terrorism trends using a Tableau dashboard, leveraging precomputed metrics for real-time analysis.

## Table of Contents
1. [Project Setup](#project-setup)
2. [Data Preprocessing and Ingestion](#data-preprocessing-and-ingestion)
3. [Table Optimization with Shard and Sort Keys](#table-optimization-with-shard-and-sort-keys)
4. [Connecting to Tableau for Visualization](#connecting-to-tableau-for-visualization)
5. [Key Features](#key-features)
6. [Requirements](#requirements)
7. [Usage](#usage)

---

### Project Setup

1. **Synthetic Data Generation**: The dataset includes simulated data based on historical global terrorism incidents. Synthetic data generation techniques were used to simulate realistic data patterns, ensuring comprehensive analysis and testing capabilities.
   
2. **SingleStoreDB Setup**: Use SingleStoreDB to create a high-performance environment optimized for large-scale data analysis, capable of ingesting and processing real-time data feeds.

### Data Preprocessing and Ingestion

In this phase, we load the synthetic dataset into SingleStoreDB:
- **Data Cleaning**: Fill missing values and encode categorical data to ensure compatibility.
- **Ingestion**: Import the dataset into SingleStore using Python’s `pymysql` library. This provides a streamlined pipeline for ongoing data ingestion and allows SingleStore to handle preprocessing directly within the database.

### Table Optimization with Shard and Sort Keys

To optimize query performance, we implemented:
1. **Shard Key** on `country_txt` to improve data distribution, ensuring rapid retrieval for location-based queries.
2. **Sort Keys** on `iyear`, `attacktype1_txt`, and `region_txt` to streamline time-based and categorical filtering, essential for detecting patterns in terrorism data.
3. **Optimized Tables**: We created additional tables, like `globalterrorism_dashboard`, for real-time visualization, with precomputed metrics to support Tableau’s analytics dashboard.

### Connecting to Tableau for Visualization

The final step involves building a Tableau dashboard for data visualization:
1. **Tableau Connection**: Connect Tableau to the SingleStore database, using the optimized table (`globalterrorism_dashboard`) as the primary data source.
2. **Visualizations**: Develop visualizations for trends in terrorist activity, showing metrics like total incidents, casualties, and regional analysis, which are valuable for real-time threat detection and situational awareness.

---

## Key Features

- **Unified Data Pipeline**: Integrates synthetic data creation, ingestion, analysis, and visualization within a single pipeline.
- **Compare Query Performance**: Leverages SingleStore’s ability to compare with Shard and Sort Keys and without.
- **Optimized for Scale**: Shard and sort keys enhance performance, allowing defense applications to scale without infrastructure concerns.
- **Tableau Dashboard**: Provides an interactive, real-time dashboard for monitoring terrorism trends and patterns.

## Requirements

- Python 3.x
- `pymysql` for database connection
- SingleStoreDB account and setup
- Tableau for data visualization

## Usage

1. **Install Dependencies**:
   ```bash
   pip install pymysql pandas


## Project Organization

```
├── LICENSE            <- Open-source license if one is chosen
├── README.md          <- The top-level README for developers using this project
├── data
│   ├── processed      <- The final, canonical data sets for modeling
│   └── raw            <- The original, immutable data dump
│

├── notebooks          <- Jupyter notebooks.
│
│
├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
│                         generated with `pip freeze > requirements.txt`
