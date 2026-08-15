# Vehicles-Registration-Analysis-Jan-Apr-2026
Exploratory data analysis of 270,314 vehicle registrations in Malaysia from January–April 2026, with comparison against the same period in 2025.

The objectives of this analysis are;
1) To understand the overall vehicle registrations pattern in Malaysia.
2) Identify the most registered vehicle manufacturers and models.
3) Examine the distribution of different vehicle types.
4) Analyse the market composition by fuel type.
5) Explore registration patterns across Malaysian states.
6) Examine the electric vehicles (EV) and hybrid electric vehicles (HEV) registration patterns.
7) Comparing the performance on the same period with 2025.

Tool used for this analysis;
R
   - Data cleaning
   - Data aggregation
   - EDA
   - Visualisation

The dataset was obtain from Malaysia Department of Statistic (DOSM) web page dated 14th May 2026. The dataset was last updated on 30th April 2026, covering the registrations of vehicles from 1st January 2026 to 30th April 2026.

The dataset contains the following variables:

Variable	Description
date_reg	Vehicle registration date
type	    Vehicle type
maker	    Vehicle manufacturer
model	    Vehicle model
colour	  Vehicle colour
fuel	    Fuel type
state	    Registration state

The original date_reg variable was stored as a character field and was converted to the appropriate Date data type using ymd().

Several data quality checks were performed before the analysis:

- Data structure inspection
- Missing-value checks
- Duplicate investigation
- Data-type validation

No missing values were identified across the seven original variables.

In this dataset, there were 219161 duplication found.

However, identical combinations of manufacturer, model, vehicle type, colour, fuel and state do not necessarily represent duplicate registrations. Multiple vehicles can legitimately share the same characteristics.

Therefore, the observations were not automatically removed as duplicates and I decided to create new column named regID as unique transaction identifier.

The analysis examines several dimensions of the vehicle registration dataset.

1. Registration Trends
Monthly registrations volumes were analysed to identify changes in registration activity throughout the January – April 2026 period.

2. Manufacturer Analysis
Vehicle registrations were grouped by manufacturer to identify the major contributors to the  market.

3. Vehicle Type Analysis
The dataset was analysed by vehicle type to understand the composition of vehicles types eg;
- Motokar (Sedan)
- Jip (SUV)
- MPV
- Pickup Truck
- Van

4. Fuel Type Analysis
Fuel categories were compared to examine the composition of the market eg;
- Petrol
- Diesel
- Electric
- Hybrid

5. State-Level Analysis
Registrations were compared across Malaysian states to identify differences in registration volume and geographical distribution.

6. Alternative Fuel Types Analysis
EV and hybrid vehicles were isolated to analyse the adoption by the regions.

7. Comparison between 2026 vs 2025
The comparison is restricted to the same four-month period to make the year-on-year analysis more consistent.

The comparison examines:
- Total registrations
- Monthly registration volume
- Fuel composition
- State-level registration volume
- EV registrations
- Percentage changes between years
