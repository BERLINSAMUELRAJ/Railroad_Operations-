# Railroad Operations & Performance Dashboard
![](https://github.com/BERLINSAMUELRAJ/Railroad_Operations-/blob/main/MRA-Class-Hero-Image_Operations.png)

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

## Data Model Overview

The data model integrates multiple datasets from five CSV files:

1. **Train_Operations** (TrainID, Date, Route, Departure_Time, Arrival_Time, Actual_Arrival, Freight_Type):
   - This table tracks the train’s journey, the scheduled and actual arrival times, delays, and the type of freight being transported.
   
2. **Equipment_Master** (LocomotiveID, Model, Manufacture_Date, Last_Maintenance, Status):
   - Contains information on each locomotive, including its status, maintenance schedule, and the date of its last maintenance.
   
3. **Track_Maintenance** (TrackID, Section, Last_Inspection, Maintenance_Due, Condition_Rating):
   - This table tracks the condition of the tracks, their inspection schedules, and maintenance requirements.
   
4. **Crew_Data** (CrewID, Name, Certification, Hours_Worked, Route_Assignment):
   - This table records the crew’s working hours, certifications, and their route assignments.
   
5. **Incident_Reports** (IncidentID, Date, Location, Type, Severity, Resolution_Time):
   - This table tracks safety incidents and reports their type, severity, and resolution time.

## Data Relationship

- A **Dim_Date** table was created using DAX, and a relationship was built between `Dim_Date[Date]` and the other date columns of various tables. This helps handle missing dates and multiple dates involved.
- A relationship was also created between the **Incident_Reports** table and the **Weather** table using the common column "Location" through a bridge table to avoid many-to-many relationships.

## Business Logic Implemented

- **On-Time Performance Metrics**: A measure was created to calculate the percentage of trains that arrive on time (i.e., where the difference between "Arrival_Time" and "Actual_Arrival" is zero).
- **Delay Analysis**: Categorizes delay causes (weather, equipment failure, operational inefficiency) and evaluates performance by route.
- **Train Utilization Rates**: Calculated the average number of trains in service, considering the route, freight type, and frequency of use.
- **Maintenance Schedules and Preventive Maintenance**: Tracks the maintenance of locomotives and tracks. The dashboard triggers predictive alerts for upcoming maintenance and overdue inspections.
- **Safety & Compliance**: Safety incidents are categorized by type (e.g., derailment, signal failure) and severity. Compliance checks on crew certifications were implemented, showing the percentage of certified versus non-certified crew.

## Dashboard Components

### a) Operational Performance:
- **On-Time Performance**: Displays the percentage of trains arriving on time versus delayed trains.
- **Delay Analysis**: Interactive visuals break down delays by cause, route, and time.
- **Train Utilization Rates**: Visualizes the number of trains in service by route, freight type, and day.
- **Route Efficiency Metrics**: Analyzes network velocity and dwell time per terminal.

### b) Equipment & Maintenance:
- **Locomotive Status & Availability**: Shows the availability and maintenance status of each locomotive.
- **Preventive Maintenance Schedule**: Displays upcoming and overdue preventive maintenance tasks for both locomotives and track segments.
- **Track Condition Monitoring**: Monitors the condition rating and inspection schedules of tracks.
- **Equipment Reliability**: Metrics on equipment failures and mean time between failures (MTBF).

### c) Safety & Compliance:
- **Incident Trends & Patterns**: Tracks incidents over time and their impact on operations, segmented by type and severity.
- **Safety Compliance Scores**: Visualizes the percentage of certified crew and other safety compliance indicators.
- **Crew Certification Status**: Breaks down crew certifications and training levels.
- **Risk Assessment Indicators**: Highlights high-risk routes and areas based on past incidents.

### d) Advanced Requirements:
- **Dynamic Route Maps**: Shows real-time train locations and their routes on a map.
- **Time-Based Filtering**: Allows users to filter data by specific time periods, such as monthly or weekly views.
- **Predictive Maintenance Alerts**: Alerts are generated when the maintenance date is near or overdue.
- **Weather Impact Analysis**: Integrates weather data to analyze its effect on operational delays.

## Operational KPIs

- **Average Delay Time by Route**: This metric calculates the average delay per train for each route.
- **On-Time Performance by Route**: Measures the percentage of trains that arrive on time (within a defined threshold, like ±15 minutes).
- **Train Utilization by Route**: Measures the average number of trains operating on each route.
- **Fuel Efficiency by Route**: If fuel consumption data is available, fuel efficiency can be calculated as fuel used per distance traveled or per train operation.
- **Total Freight Movement (Volume) by Route**: Measures the amount of freight transported along each route, either by freight type or weight of goods moved.
- **Total Fuel Consumption by Route**: Shows the total amount of fuel consumed across each route.
- **Total Cargo Weight by Route**: Indicates the total amount of cargo moved across each route.
- **Freight Transport Efficiency (Cargo Weight per Train)**: Measures the average weight of cargo transported per train.
- **Total Delay Time by Route**: Displays the cumulative delay time experienced by each route.
- **Train Utilization Rate (based on Cargo Weight)**: Calculates the utilization rate based on cargo weight moved by each train.
- **Total Available Locomotives**: The count of locomotives in service.
- **Total Under Maintenance Locomotives**: The count of locomotives under maintenance.
- **Mean Time Between Failures (MTBF) (in Miles)**: Estimates the average lifetime miles per locomotive.
- **Average Maintenance Cost (YTD)**: Tracks the average maintenance cost per locomotive year-to-date.
- **Percentage of Locomotives Due for Maintenance Soon**: Calculates the percentage of locomotives due for maintenance within a specified threshold.
- **Days Until Next Track Maintenance Due**: Calculates the number of days remaining until the next track maintenance is due.
- **Total Track Repair Costs (YTD)**: Calculates the total repair cost incurred for all tracks in the current year.
- **Track Condition Monitoring**: Assesses the condition of tracks and prioritizes maintenance based on condition ratings.
- **Average Track Condition Rating**: Calculates the average condition rating for all tracks.
- **Total Track Length by Condition**: Calculates the total length of tracks by their condition rating.
- **Tracks Needing Immediate Attention (Priority Level = High)**: Calculates the number of tracks with the highest priority level, indicating immediate maintenance needs.
- **Track Length for High-Priority Maintenance**: Calculates the total length of tracks assigned high priority maintenance.
- **Safety Compliance Score**: Tracks safety performance and calculates an average safety score for the crew.
- **Crew Training and Performance**: Tracks how well-trained crew members are based on their last training date and performance rating.
- **Crew Experience and Safety Score**: Analyzes the impact of crew experience on safety scores.
- **Average Shift Hours Worked**: Tracks the total hours worked by crew members to identify overworking and safety compliance risks.
- **Incident Count Over Time**: Tracks the incident count over time to identify patterns or trends.
- **Incident Root Cause Distribution**: Analyzes the root cause of incidents to identify contributing factors.
- **Average Incident Resolution Time**: Measures how long it takes, on average, to resolve incidents.

## Other KPIs

- **Average Incident Resolution Time**
- **Percentage of Crew Trained in Last Year**
- **Average Precipitation Over Time**
- **Risk Assessment Indicator**

## Recommendations for Operational Improvements

- **Improve On-Time Performance**: Focus on addressing delays caused by weather conditions and operational inefficiencies.
- **Preventive Maintenance Strategy**: Shift towards a predictive maintenance strategy, leveraging MTBF and maintenance alerts to proactively handle equipment issues.
- **Crew Certification Management**: Ensure that crew certifications and training schedules are up to date for compliance.
- **Track Maintenance Optimization**: Optimize inspection schedules based on condition ratings to avoid unexpected failures.

## Conclusion

This Power BI dashboard offers a comprehensive view of the railroad operator's performance, safety, and maintenance operations, enabling data-driven decision-making. The advanced features, including predictive maintenance alerts and geospatial visualizations, provide valuable insights that can drive operational improvements and ensure better service delivery.

