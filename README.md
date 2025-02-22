# Railroad Operations & Performance Dashboard

## Introduction

The **Railroad Operations & Performance Dashboard** is a comprehensive Power BI solution designed to analyze the operational efficiency, safety metrics, and maintenance schedules of a railroad operator. It aggregates data from various sources, including train operations, equipment maintenance, track conditions, crew data, and incident reports. The dashboard provides valuable insights and key performance indicators (KPIs) to improve decision-making and optimize operations.

## Task Background

You are working with a major railroad operator that manages both freight and passenger services across multiple routes. The company requires an in-depth analysis of its operational efficiency, safety metrics, and maintenance schedules.

## Data

The project uses the following data source: **[Railroad Data GitHub Repository](https://github.com/balasista/railroad_data)**  

It contains the following CSV files:

- **Train_Operations** (TrainID, Date, Route, Departure_Time, Arrival_Time, Actual_Arrival, Freight_Type)
- **Equipment_Master** (LocomotiveID, Model, Manufacture_Date, Last_Maintenance, Status)
- **Track_Maintenance** (TrackID, Section, Last_Inspection, Maintenance_Due, Condition_Rating)
- **Crew_Data** (CrewID, Name, Certification, Hours_Worked, Route_Assignment)
- **Incident_Reports** (IncidentID, Date, Location, Type, Severity, Resolution_Time)

## Task Requirements

### Data Modeling & ETL

The following tasks were performed to prepare the data for analysis:

- Data extraction and cleaning of multiple CSV files.
- Data transformation to create relationships between datasets.
- Data modeling for optimal report creation in Power BI.

### Dashboard Creation

The following key components were included in the Power BI dashboard:

#### a) Operational Performance
- On-time performance metrics
- Delay analysis by route and cause
- Train utilization rates
- Route efficiency metrics

#### b) Equipment & Maintenance
- Locomotive status and availability
- Preventive maintenance schedule
- Track condition monitoring
- Equipment reliability metrics

#### c) Safety & Compliance
- Incident trends and patterns
- Safety compliance scores
- Crew certification status
- Risk assessment indicators

### Advanced Requirements
The following advanced features were implemented:

- DAX calculations for:
  - Average delay time by route
  - Equipment downtime analysis
  - Crew utilization rates
  - Mean time between failures
- Dynamic route maps
- Time-based filtering for trend analysis
- Predictive maintenance alerts
- Weather impact analysis

### Bonus Features
- Geospatial visualization of routes
- Custom tooltips for detailed route information
- Cross-filtering between related metrics

## Key Focus Areas

- Railroad operational metrics
- Maintenance scheduling
- Safety compliance
- Route optimization
- Equipment reliability
- Crew management

## Key Performance Indicators (KPIs)

- Terminal Dwell Time
- Network Velocity
- Cars Online
- First Mile/Last Mile Performance
- Fuel Efficiency
- Safety Incident Rate
