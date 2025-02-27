**Flu Shots Dashboard for 2022**

**Overview**

This project creates a visualization dashboard in Tableau Public to track flu shot uptake during 2022. The SQL code retrieves and prepares data from a healthcare systems database, which is then used to build visualizations that show key insights into flu vaccination rates.

**Project Objectives**

- **Stratified Flu Shot Rates:**
  Calculate the total percentage of active patients receiving flu shots, broken down by age, race, and county (displayed on a map), as well as overall.

- **Running Total:**
  Display a running total of flu shots administered over the course of 2022.

- **Total Count:**
Report the overall number of flu shots given in 2022.

- **Patient Details:**
Generate a list of patients with an indicator showing whether they received the flu shot.

**Data Preparation & Methodology**

- **Active Patients:**
The query first identifies active patients by filtering those who have had healthcare encounters in the past two years, are not deceased, and are at least 6 months old (since flu shots are recommended for those 6 months and older).

- **Flu Shot Extraction:**
From the immunizations table, it retrieves the earliest flu shot (using code '5302') for each patient during 2022. This prevents duplication when a patient received more than one shot in the year.

- **Final Data Join:**
The resulting flu shot data is then left-joined with the main patients table to include relevant demographic details such as birthdate, race, county, and names. A binary flag is created to indicate whether a patient received a flu shot in 2022.

**Dashboard and Real-World Application**

The cleaned and summarized data is uploaded into Tableau Public, where a dashboard is created to provide a clear, interactive view of the flu shot metrics. Healthcare administrators can use this dashboard to:

- Monitor vaccination rates across different demographic groups.
- Identify areas or populations with lower vaccination uptake.
- Make informed decisions on targeted public health interventions and resource allocation.
  
Access the Tableau dashboard here:
[Flu Shots Dashboard](https://public.tableau.com/app/profile/lonimitona/viz/FluShotsDashboard_17005542554070/Dashboard1)
