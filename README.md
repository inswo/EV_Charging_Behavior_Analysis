# EV_Charging_Behavior_Analysis

## Schema

### Electric Vehicle Charging Patterns

| **Column Name**             | **Data Type**      | **Description**                                                                                  |
|-----------------------------|--------------------|--------------------------------------------------------------------------------------------------|
| `user_id`                   | VARCHAR(50)       | Unique identifier for each user (e.g., `user_1`).                                               |
| `vehicle_model`             | VARCHAR(100)      | Specific model of the electric vehicle (e.g., `BMW i3`).                                        |
| `battery_capacity_kwh`      | FLOAT       | Maximum energy storage of the vehicle's battery in kilowatt-hours (e.g., `108.4630074`).        |
| `charging_station_id`       | VARCHAR(50)       | Unique identifier for the charging station used (e.g., `station_391`).                         |
| `charging_station_location` | VARCHAR(100)      | Geographic location of the charging station (e.g., `Houston`).                                  |
| `start_time`                | DATETIME          | Timestamp for when the charging session began (e.g., `1/1/24 0:00`).                           |
| `end_time`                  | DATETIME          | Timestamp for when the charging session ended (e.g., `1/1/24 0:39`).                           |
| `energy_consumed_kwh`       | FLOAT       | Total energy consumed during the charging session, in kilowatt-hours (e.g., `60.71234573`).     |
| `charging_duration_hours`   | FLOAT       | Total time taken to charge the vehicle, in hours (e.g., `0.591363425`).                         |
| `charging_rate_kw`          | FLOAT       | Average power delivery rate during the session, in kilowatts (e.g., `36.38918057`).             |
| `charging_cost_usd`         | FLOAT       | Total cost of the charging session in US dollars (e.g., `13.08771679`).                         |
| `time_of_day`               | VARCHAR(50)       | Time segment when charging occurred (e.g., `evening`).                                          |
| `day_of_week`               | VARCHAR(20)       | Day when the charging occurred (e.g., `tuesday`).                                               |
| `state_of_charge_start`     | FLOAT       | Battery percentage at the start of charging (e.g., `29.37157598`).                              |
| `state_of_charge_end`       | FLOAT       | Battery percentage at the end of charging (e.g., `86.11996244`).                                |
| `distance_driven`           | FLOAT       | Distance traveled since the last charge, in kilometers (e.g., `293.6021106`).                   |
| `temperature`               | FLOAT       | Ambient temperature during the session, in degrees Celsius (e.g., `27.94795306`).              |
| `vehicle_age`               | INTEGER           | Age of the electric vehicle, in years (e.g., `2`).                                              |
| `charger_type`              | VARCHAR(50)       | Type of charger used (e.g., `DC Fast Charger`).                                                 |
| `user_type`                 | VARCHAR(50)       | Classification of user based on driving habits (e.g., `Commuter`).                              |

### Demographic and Socioeconomic Data Table

| Column Name            | Data Type    | Description                                                                                     |
|------------------------|--------------|-------------------------------------------------------------------------------------------------|
| `location`             | VARCHAR(100)| Name of the city or locality.                                                                  |
| `median_income`        | FLOAT       | Median household income in the region (in USD).                                                |
| `population_density`   | FLOAT       | Number of people per square kilometer.                                                         |
| `vehicle_ownership_rate`| FLOAT      | Percentage of households in the region that own at least one vehicle.                          |
| `electric_vehicle_rate`| FLOAT       | Percentage of vehicles in the region that are electric.                                        |
| `commuter_percentage`  | FLOAT       | Percentage of the population identified as commuters (traveling daily for work).               |
| `age_distribution`     | JSON        | JSON object summarizing the population age distribution (e.g., `{ "0-18": 20%, "19-65": 70% }`).|
| `education_level`      | JSON        | JSON object summarizing the education levels (e.g., `{ "High School": 40%, "College": 50% }`). |
| `accessibility_index`  | FLOAT       | A score indicating infrastructure accessibility for underserved populations (1–10 scale).       |
| `region_type`          | VARCHAR(50) | Type of area (e.g., Urban, Suburban, Rural).                                                   |

*Source: US Census Bureau, World Bank Open Data.*
