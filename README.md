BookShelf – ReadingRadar

Book Metadata Analytics Pipeline using Databricks

1. Project Overview

BookShelf – ReadingRadar is a data engineering and analytics project built using Databricks and PySpark. It processes book metadata from Open Library and transforms it into structured datasets for analytical reporting.

The project follows a Medallion Architecture consisting of Bronze, Silver and Gold layers. The processed data is used to build an interactive Databricks SQL dashboard called ReadingRadar, providing insights into fiction books, authors, publication trends and edition distribution.

2. Project Objectives

Ingest book metadata from Open Library.

Organize data using the Bronze, Silver and Gold architecture.

Clean and transform raw metadata using PySpark.

Create analytical datasets using aggregations.

Store processed data as Delta tables.

Build SQL-based analytics and an interactive dashboard.

Explore publication trends, author contributions and edition distributions.

3. Technology Stack

Databricks-Data engineering and analytics environment

Apache Spark / PySpark-Data processing and transformations

Python-Pipeline implementation

SQL-Analytical queries and aggregations

Delta Lake-Structured data storage

Databricks SQL Dashboards-Data visualization

Git and GitHub-Version control

4. Data Pipeline Architecture

The project follows the Medallion Architecture.

Bronze Layer – Raw Data

The initial ingestion layer stores retrieved book metadata for downstream processing.

Silver Layer – Cleaned Data

The Silver layer processes raw metadata, applies cleaning and transformations, and prepares structured book records for analytics.

Gold Layer – Analytical Data

The Gold layer contains aggregated datasets designed for analytical queries and dashboard visualizations.

The Gold layer includes:

Books aggregated by author.

Books aggregated by publication year.

Books aggregated by publication decade.

Book edition information.

Edition distribution categories.

A consolidated KPI summary.

5. Gold Layer Analytical Datasets

Dataset - Purpose

books_gold_by_author - Book counts by author

books_gold_by_year - Book counts by publication year

books_gold_by_decade - Book counts by publication decade

books_gold_by_editions - Work-level book and edition information

books_gold_edition_distribution - Distribution of books across edition-count categories

books_gold_kpi_summary - Consolidated analytical KPIs

6. ReadingRadar Dashboard

ReadingRadar is an interactive Databricks dashboard built on the Gold-layer datasets.

Key Performance Indicators

Total Fiction Books: 100
Total Reported Editions: 2,259
Unique Authors: 260
Average Editions per Work: 22.6

Visualizations

Top Authors by Number of Books.
Publication-Year Trend.
Books Published by Decade.
Book Edition Distribution.

A publication-decade filter is available for exploring decade-level distributions.

Dashboard Preview

7. Repository Structure

bookshelf-data-engineering/
│
├── notebooks/
│   └── 03_gold_analytics.ipynb
│
├── assets/
│   └── readingradar-dashboard.png
│
├── .gitignore
├── README.md
└── requirements.txt

8. Project Goals

The goal of BookShelf is to demonstrate practical data engineering concepts, including data ingestion, layered data processing, PySpark transformations, analytical data modeling, SQL querying and dashboard development.

Further improvements focus on pipeline reliability, data quality, reproducibility and documentation.