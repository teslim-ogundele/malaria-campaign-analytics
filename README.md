# malaria-campaign-analytics
# Automated Data Pipeline & Performance Dashboard for Integrated Campaigns

```mermaid
graph TD
    classDef bwStyle fill:#fff,stroke:#000,stroke-width:2px,color:#000;
    
    A[schema.sql<br>Defines Database Architecture]:::bwStyle
    B[Raw Field Data<br>Digital Data Collection Tools]:::bwStyle
    C[pipeline.py<br>Python ETL & Validation Engine]:::bwStyle
    D[(campaign_data.db<br>Structured SQLite Database)]:::bwStyle
    E[data_quality_logs<br>Command Center Validation Flags]:::bwStyle
    F[queries.sql<br>Operational Analytics & Coverage Metrics]:::bwStyle
    G[Real-Time Decision Making<br>Target Monitoring & Course Correction]:::bwStyle

    A -->|Builds & Structures| D
    B -->|Ingests Raw Data| C
    C -->|Validates & Cleans| D
    C -->|Logs Flaws & Anomalies| E
    D -->|Feeds Raw Rows| F
    F -->|Outputs Actionable Data| G
```    
This repository showcases an end-to-end data pipeline design built specifically to solve data reconciliation delays and field synchronization errors during large-scale digitized public health initiatives (such as SMC and ITN integrations).

## Features
* Relational Database Design: A structured schema to track real-time field data alongside macro campaign operational targets.
* Automated ETL Pipeline: A programmatic Python validation script that checks incoming records against standard operational rules (e.g., child age guidelines and invalid GPS coordinate ranges).
* Command Center Analytics: Embedded SQL scripts to measure target execution metrics, track coverage rates, and clean erroneous entries.
* Technical Documentation: Fully integrated Product Requirements Document (PRD) frameworks and field deployment Job Aids.

## Technical Stack
* **Language:** Python 3.x (Pandas, SQLite3)
* **Database Engine:** SQL (SQLite / PostgreSQL environment compatible)
* **Documentation Standards:** Markdown Product Architecture Specification

To clone this project,

bash

git clone [https://github.com/teslim-ogundele/malaria-campaign-analytics.git]
