# Fleet Driver Productivity Details with Formulas

## Project Description

Professional delivery and operational fleets are significant contributors to global greenhouse emissions. Fleet owners aspire to achieve net-zero emissions promptly; however, the transition presents a complex dilemma. Balancing the urgency of achieving net-zero emissions with business sustainability and customer satisfaction requires a decision-making framework that considers factors such as timing, location, and approach.

By harnessing the power of data and mathematical models, we navigate the complexities of demand forecasts, dissect emission profiles, and find ways to meet ambitious emission targets. The end game is to develop ingenious solutions that strike a balance between operational effectiveness and environmental impact. 

## Data Overview

The dataset used in this project contains the following columns and values:

### Columns, Roles, and Values Information:

- **Fuel Types and Vehicle Information**
    - **Fuel Types**: 
        - BEV (Battery Electric Vehicles)
        - Diesel (Diesel-powered vehicles)
    - **Example Vehicle IDs**: 
        - BEV_S1_2023, BEV_S2_2023, BEV_S3_2023, BEV_S4_2023, Diesel_S1_2023

- **Driver_ID**
    - A unique identifier for each driver.
    - **Sample values**: 135, 191, 114, 32, 101

- **Name**
    - The name of the driver.
    - **Sample values**: Driver_135, Driver_191, Driver_114, Driver_32, Driver_101

- **Size**
    - Different sizes or tiers representing workloads or vehicle types.
    - **Sample values**: S1, S2, S3, S4

- **Year**
    - The year for which the data is collected.
    - **Sample values**: 2023, 2024, 2025, 2026, 2027

- **Cost ($)**
    - Yearly operational cost associated with vehicle maintenance and other expenses.
    - **Sample values**: 187000, 272000, 309090, 395636, 85000

- **Yearly Range of Vehicle (km)**
    - Represents the range that vehicles of varying sizes can travel.
    - **Sample values**: 102000, 106000, 73000, 118000

- **Distance**
    - Categorizes distances or routes (e.g., D1, D4).
    - **Sample values**: D1, D4, D2, D3

- **Consumption Unit (unit_fuel)**
    - Amount of fuel utilized by a vehicle.
    - **Sample values**: 0.893043, 0.8968, 0.898003, 0.900664, 0.223016

- **Vehicle_ID**
    - Identifies the vehicle assigned to the driver.
    - **Sample values**: BEV_S1_2023, BEV_S2_2023, BEV_S3_2023, BEV_S4_2023, Diesel_S1_2023

- **Fuel Cost ($/unit_fuel)**
    - Cost of different fuel types.
    - **Sample values**: 0.191791, 1.220845, 1.011618, 0.184113, 1.246802

- **Emissions (CO2/unit_fuel)**
    - Carbon emissions released by specific fuels.
    - **Sample values**: 0.0, 3.04858, 2.486188

- **Fuel**
    - Fuels utilized by the vehicles.
    - **Sample values**: Electricity, B20, LNG

- **Collision Rate (collisions/km)**
    - Indicates how often a driver gets into collisions.
    - **Sample values**: 1.82085492743821e-05, 6.02563824762224e-05, 9.37681593043208e-05, 1.16399643086394e-05, 1.10218280290677e-05

- **Rest Days**
    - Number of rest days taken by a driver in a year.
    - **Sample values**: 13, 35, 33, 10, 24

- **Shift Hours per Day**
    - Number of hours a driver works daily.
    - **Sample values**: 9, 6, 5, 8, 7

- **Fuel Cost Uncertainty (%)**
    - Cost of fuel price fluctuation.
    - **Sample values**: 0, 2, 4, 6, 8

- **Demand (km)**
    - Demand a vehicle of a certain size has.
    - **Sample values**: 869181, 995694, 14576, 2183475, 205426

- **Carbon Emission (CO2/kg)**
    - Carbon emissions associated with each driver’s vehicle.
    - **Sample values**: 11677957, 10510161, 9459145, 8513230, 7661907

## Derived Features with Formulas

- **Annual Productivity**
    - **Formula**: 
        ``` 
        Annual Productivity = (Avg Daily Distance * Shift Hours per Day * (365 - Rest Days)) / Fuel Efficiency
        ```
    - **Sample values**: 98367.123, 95835.616, 66400.0, 114767.123, 95293.150

- **Collision Risk Score**
    - **Formula**: 
        ``` 
        Collision Risk Score = Collision Rate * (1000000 / Yearly Range of Vehicle)
        ```
    - **Sample values**: 0.000716, 0.003455, 0.006403, 0.000372, 0.000212

- **Avg Daily Distance (km)**
    - Average distance a driver covers each day.
    - **Sample values**: 279.452, 290.411, 200.0, 323.288

- **Fuel Efficiency (km/unit fuel)**
    - Number of kilometers a vehicle can travel per unit of fuel.
    - **Sample values**: 114216.225, 118198.037, 81291.488, 131014.452, 457366.288
