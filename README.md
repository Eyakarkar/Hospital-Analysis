<img width="911" height="540" alt="home hospital" src="https://github.com/user-attachments/assets/1e77d550-8359-41cf-899c-3ecb267a48bf" />
<img width="909" height="547" alt="hospital2" src="https://github.com/user-attachments/assets/1625abed-c270-4ec8-a0c3-dea900defca8" />
<img width="906" height="541" alt="hospital3" src="https://github.com/user-attachments/assets/21c6051d-26f9-4131-8bb4-4b654c866bb1" />
🏥 Hospital Analysis — Power BI
📌 Project Overview
This project presents an interactive Power BI analysis of hospital data from New York State in 2016.

The objective is to evaluate hospital efficiency, healthcare costs, patient characteristics, and clinical outcomes, with a particular focus on identifying the factors that influence Length of Stay (LOS) and hospital costs.

The project transforms raw hospital discharge data into an interactive Business Intelligence solution designed to support data-driven healthcare decision-making.

🎯 Project Objectives
The analysis focuses on:

Evaluating overall hospital activity and efficiency
Analyzing Length of Stay (LOS)
Comparing hospital costs and charges
Identifying differences in performance between hospitals
Analyzing patient demographics
Studying severity of illness and mortality risk
Examining patient discharge outcomes
Identifying clinical factors associated with longer hospital stays
📊 Power BI Dashboards
1️⃣ Hospital Efficiency Overview
This dashboard provides an executive overview of hospital performance.

Main KPIs:

Total Admissions
Total Hospitals
Average Length of Stay
Total Costs
Average Cost per Admission
Total Charges
Main analyses:

Hospital performance comparison
Total costs vs. total charges
Admissions by Health Service Area
Average cost by county
Hospital efficiency analysis
Comparison of LOS and costs across hospitals
2️⃣ Clinical and Patient Analysis
This dashboard focuses on clinical characteristics and patient outcomes.

Main KPIs:

Total Admissions
Average LOS
Surgical Admission %
High Severity %
High Mortality Risk %
Discharged Home %
Main analyses:

Average LOS by severity level
Admissions and LOS by gender
Patient disposition
Severity distribution
Mortality risk
Clinical risk analysis
🧮 DAX Measures
Several DAX measures were created to support the analysis.

Total Admissions =
COUNTROWS('Fact')
Total Hospitals =
DISTINCTCOUNT('Dim Hospital'[facility_id])
Average LOS =
AVERAGE('Fact'[length_of_stay])
Total Costs =
SUM('Fact'[total_costs])
Total Charges =
SUM('Fact'[total_charges])
Surgical Admission % =
DIVIDE(
    [Surgical Admissions],
    [Total Admissions],
    0
)
High Severity % =
DIVIDE(
    [High Severity Admissions],
    [Total Admissions],
    0
)
Discharged Home % =
DIVIDE(
    [Discharged Home],
    [Total Admissions],
    0
)
🗂️ Data Model
The Power BI model follows a simplified Star Schema approach.

The main fact table contains hospital discharge information and numerical measures such as:

Length of Stay
Total Costs
Total Charges
Diagnosis codes
Procedure codes
Severity information
Dimension tables are used to organize hospital and patient-related attributes.

Main Tables
Fact

Hospital discharge records
Length of Stay
Costs
Charges
Diagnosis
Procedures
Severity
Mortality risk
Dim Hospital

Facility ID
Facility Name
Hospital County
Health Service Area
Dim Patient

Gender
Age Group
Race
Ethnicity
Patient Disposition
The relationships follow a one-to-many (1:*) structure between dimensions and the Fact table.

🛠️ Tools & Technologies
Power BI Desktop
Power Query
DAX
Data Modeling
Star Schema
Data Visualization
Healthcare Analytics
Business Intelligence
📈 Key Insights
The dashboards make it possible to identify:

Differences in hospital efficiency across New York
Hospitals with higher healthcare costs
Differences in LOS between severity levels
Relationships between clinical severity and hospital stay
Patient discharge patterns
Geographic differences in hospital activity
Differences in admissions and LOS between patient groups
One particularly important observation is that Length of Stay increases substantially with illness severity, highlighting the impact of clinical complexity on hospital resource utilization
📁 Repository Structure
Hospital-Analysis/
│
├── README.md
├── Hospital_Analysis.pbix
├── data/
│   └── hospital_data.csv
│
└── images/
    ├── home-page.png
    ├── hospital-efficiency.png
    └── clinical-patient-analysis.png
💡 Skills Demonstrated
This project demonstrates skills in:

Power BI • DAX • Power Query • Data Modeling • Data Visualization • Healthcare Analytics • Business Intelligence • Dashboard Design
