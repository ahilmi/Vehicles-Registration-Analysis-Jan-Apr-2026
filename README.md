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

The dataset was obtain from Malaysia Department of Statistic (DOSM) web page dated 14th May 2026. The dataset contained 270,314 entries, was last updated on 30th April 2026, covering the registrations of vehicles from 1st January 2026 to 30th April 2026.

The dataset contains the following variables:

Variable	Description
date_reg   Vehicle registration date
type       Vehicle type
maker      Vehicle manufacturer
model      Vehicle model
colour	  Vehicle colour
fuel       Fuel type
state	     Registration state

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

In this dataset also, there is a state level variable registration by 'Rakan Niaga'. According to readme by the uploader, 'Rakan Niaga' is a third party registration services approved by the Jabatan Pengangkutan Jalan (JPJ). There was 236,984 registrations from this channel. However this information could skewed the number registration by state. We can't really tell which state the vehicles were registered, it could give a false assumption. Therefore whenever the analysis is related with state variable, I opt to exclude the 'Rakan Niaga' to achieve more accurate result.

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
The comparison is restricted to the same month January - April period to make the analysis more consistent.

The comparison examines:
- Total registrations
- Monthly registration volume
- Fuel composition
- State-level registration volume
- EV registrations
- Percentage changes between years

From this analysis, there are few key findings.

1) There are 270,314 vehicles were registered from January to April 2026, a 2.56% increase from the same period on 2025 (263,578).
2) Monthly registrations saw an irregularity through out the same period in 2025 and 2026. 
3) Perodua top the list for both 2025 and 2026 as top maker followed by Proton.
4) Petrol vehicles, whilst maintain a top chosen, saw a dip in registration significantly in 2026 compare to 2025.
5) Electric and hybrid vehicles are on the rise significantly.
6) Total regional registrations saw a significant disparity between high income vs low income states.

Some highlighted visualisation.

<img width="840" height="840" alt="1" src="https://github.com/user-attachments/assets/f389a15b-7055-4bff-920f-e21e4e43dff4" />

<img width="840" height="840" alt="2" src="https://github.com/user-attachments/assets/49cf0481-2714-41d7-be01-ffbb66ac1389" />

<img width="840" height="840" alt="3" src="https://github.com/user-attachments/assets/8a780125-ff6b-42e5-a9c5-e8ce2eb22953" />

<img width="840" height="840" alt="4" src="https://github.com/user-attachments/assets/d095419f-297f-4aaf-a3c7-351399f95cab" />

<img width="840" height="840" alt="5" src="https://github.com/user-attachments/assets/bee5258e-7904-4e87-b253-1ad9c796de15" />

<img width="840" height="840" alt="6" src="https://github.com/user-attachments/assets/60752879-fdc3-4f4b-a62d-86e8c9e7e024" />

<img width="840" height="840" alt="7" src="https://github.com/user-attachments/assets/3d49537d-7aca-419f-8248-5efe5d2bef1b" />

<img width="840" height="840" alt="8" src="https://github.com/user-attachments/assets/e626e4b3-33e3-424c-8c06-e94234895768" />

<img width="840" height="840" alt="9" src="https://github.com/user-attachments/assets/8dc9ff82-c574-41ca-97e3-46d3e3786625" />

<img width="840" height="840" alt="10" src="https://github.com/user-attachments/assets/58ed9200-a8a8-4e2c-9c21-f1cf1e883136" />

This project was created as part of my journey into data analytics, with a focus on developing practical skills in:

- Data cleaning
- Exploratory data analysis
- Data visualisation
- R programming
- Statistical thinking
- Analytical storytelling

For future improvements;

- Automating the data-cleaning workflow
- Adding more detailed year-on-year statistical comparisons
- Building an interactive dashboard using Power BI
- Expanding the analysis to a full-year dataset
- Investigating EV adoption trends over a longer period
- Adding more detailed model-level analysis
- Connecting the analysis directly to a SQL database
- Use Python instead of R
- Dashboard using PowerBI or Tableau

The full analysis and R workflow are available in the project report:

/R-JPJv2.pdf
