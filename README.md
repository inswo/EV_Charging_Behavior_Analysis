# EV_Charging_Behavior_Analysis

## Schema

### Demographic and Socioeconomic Data Table Schema

| Column Name            | Data Type    | Description                                                                                     |
|------------------------|--------------|-------------------------------------------------------------------------------------------------|
| `region_id`            | VARCHAR(50) | Unique identifier for the geographic region (e.g., Census tract, ZIP code, or city name).       |
| `location_city`        | VARCHAR(100)| Name of the city or locality.                                                                  |
| `median_income`        | FLOAT       | Median household income in the region (in USD).                                                |
| `population_density`   | FLOAT       | Number of people per square kilometer.                                                         |
| `vehicle_ownership_rate`| FLOAT      | Percentage of households in the region that own at least one vehicle.                          |
| `electric_vehicle_rate`| FLOAT       | Percentage of vehicles in the region that are electric.                                        |
| `commuter_percentage`  | FLOAT       | Percentage of the population identified as commuters (traveling daily for work).               |
| `age_distribution`     | JSON        | JSON object summarizing the population age distribution (e.g., `{ "0-18": 20%, "19-65": 70% }`).|
| `education_level`      | JSON        | JSON object summarizing the education levels (e.g., `{ "High School": 40%, "College": 50% }`). |
| `accessibility_index`  | FLOAT       | A score indicating infrastructure accessibility for underserved populations (1–10 scale).       |
| `region_type`          | VARCHAR(50) | Type of area (e.g., Urban, Suburban, Rural).                                                   |
