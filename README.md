# EV Charging Behavior Analysis - Project Overview

## Project Background

L'adoption rapide des véhicules électriques dans le monde entier est en train de remodeler les secteurs de l'automobile et de l'énergie. Alors que les gouvernements prônent un transport plus durable et que les particuliers adoptent les VE pour réduire leur empreinte carbone, la demande d'infrastructures de recharge efficaces et abordables pour les VE ne cesse de croître. 

Pour répondre à cette demande, il est nécessaire de bien comprendre les comportements en matière de recharge, les structures de tarification de l'électricité et les caractéristiques démographiques régionales.

Insights and recommendations are provided on the following key areas:

**1. Charging Behavior Analysis:**
**Insight:** Identify peak charging hours, preferred charging locations, and user types (e.g., commuters, long-distance drivers).

**2. Electricity Pricing Impact:**
**Insight:** Correlate electricity costs with energy consumption patterns to understand price sensitivity.

**3. Demographic Influence on EV Adoption:**
**Insight:** Higher-income regions and areas with better education levels show greater EV adoption and higher charging station usage.

## Schema

### Electric Vehicle Charging Patterns

| **Column Name**             | **Data Type**      | **Description**                                                                                  |
|-----------------------------|--------------------|--------------------------------------------------------------------------------------------------|
| `user_id`                   | STRING       | Unique identifier for each user (e.g., `user_1`).                                               |
| `vehicle_model`             | STRING      | Specific model of the electric vehicle (e.g., `BMW i3`).                                        |
| `battery_capacity`      | FLOAT       | Maximum energy storage of the vehicle's battery in kilowatt-hours (e.g., `108.4630074`).        |
| `charging_station_id`       | STRING       | Unique identifier for the charging station used (e.g., `station_391`).                         |
| `charging_station_location` | STRING      | Geographic location of the charging station (e.g., `Houston`).                                  |
| `start_time`                | DATETIME          | Timestamp for when the charging session began (e.g., `1/1/24 0:00`).                           |
| `end_time`                  | DATETIME          | Timestamp for when the charging session ended (e.g., `1/1/24 0:39`).                           |
| `energy_consumed`       | FLOAT       | Total energy consumed during the charging session, in kilowatt-hours (e.g., `60.71234573`).     |
| `charging_duration`   | FLOAT       | Total time taken to charge the vehicle, in hours (e.g., `0.591363425`).                         |
| `charging_rate`          | FLOAT       | Average power delivery rate during the session, in kilowatts (e.g., `36.38918057`).             |
| `charging_cost`         | FLOAT       | Total cost of the charging session in US dollars (e.g., `13.08771679`).                         |
| `time_of_day`               | STRING       | Time segment when charging occurred (e.g., `evening`).                                          |
| `day_of_week`               | STRING       | Day when the charging occurred (e.g., `tuesday`).                                               |
| `state_of_charge_start`     | FLOAT       | Battery percentage at the start of charging (e.g., `29.37157598`).                              |
| `state_of_charge_end`       | FLOAT       | Battery percentage at the end of charging (e.g., `86.11996244`).                                |
| `distance_driven`           | FLOAT       | Distance traveled since the last charge, in kilometers (e.g., `293.6021106`).                   |
| `temperature`               | FLOAT       | Ambient temperature during the session, in degrees Celsius (e.g., `27.94795306`).              |
| `vehicle_age`               | INTEGER           | Age of the electric vehicle, in years (e.g., `2`).                                              |
| `charger_type`              | STRING       | Type of charger used (e.g., `DC Fast Charger`).                                                 |
| `user_type`                 | STRING       | Classification of user based on driving habits (e.g., `Commuter`).                              |

*Dataset Name: EV Charging Patterns*  
*Source: [EV Charging Patterns](https://www.kaggle.com/code/jaishumeda/ev-charging-patterns/)*  
*Description: This dataset provides charging session details, including energy consumed, charging duration, vehicle details, and user classifications. It enables insights into electric vehicle (EV) charging behavior and usage patterns.*

### Demographic and Socioeconomic Data Table

| Column Name            | Data Type    | Description                                                                                     |
|------------------------|--------------|-------------------------------------------------------------------------------------------------|
| `location`             | STRING| Name of the city or locality.                                                                  |
| `median_income`        | FLOAT       | Median household income in the region (in USD).                                                |
| `population_density`   | FLOAT       | Number of people per square kilometer.                                                         |
| `vehicle_ownership_rate`| FLOAT      | Percentage of households in the region that own at least one vehicle.                          |
| `electric_vehicle_rate`| FLOAT       | Percentage of vehicles in the region that are electric.                                        |
| `commuter_percentage`  | FLOAT       | Percentage of the population identified as commuters (traveling daily for work).               |
| `age_distribution`     | JSON        | JSON object summarizing the population age distribution (e.g., `{ "0-18": 20%, "19-65": 70% }`).|
| `education_level`      | JSON        | JSON object summarizing the education levels (e.g., `{ "High School": 40%, "College": 50% }`). |
| `accessibility_index`  | FLOAT       | A score indicating infrastructure accessibility for underserved populations (1–10 scale).       |
| `region_type`          | STRING | Type of area (e.g., Urban, Suburban, Rural).                                                   |

*Source: US Census Bureau, World Bank Open Data.*

### U.S. Electricity Prices

| **Column Name**       | **Data Type**      | **Description**                                                                              |
|------------------------|--------------------|---------------------------------------------------------------------------------------------|
| `year`                | INTEGER           | The year for the data entry (e.g., `2023`).                                                |                         |
| `state_description`   | STRING      | The name of the state or region (e.g., `California`, `Texas`).                             |
| `sector_name`         | STRING      | The name of the sector electricity was provided to (e.g., `Residential`, `Industrial`).    |
| `price`               | FLOAT             | The price of electricity in cents per kilowatt-hour (e.g., `12.34`).                       |
| `revenue`             | FLOAT             | The revenue generated from sales in millions of dollars (e.g., `123.45`).                  |
| `sales`               | FLOAT             | The sales of electricity in million kilowatt-hours (e.g., `456.78`).                       |

*Dataset Name: U.S. Electricity Prices*
*Source: [U.S. Electricity Prices](https://www.kaggle.com/datasets/alistairking/electricity-prices)*  
*Description: This dataset includes information on electricity prices, revenues, and sales across different sectors (e.g., Residential, Industrial) and regions. It provides insights into electricity consumption patterns, pricing trends, and revenue generation over time.*  
