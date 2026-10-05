# Kenya 2022 Voter Demographics & Gender Analysis 🇰🇪

## Overview

This project analyzes Kenya's 2022 registered-voter data by **county, region, age group, and gender** using Microsoft Power BI.

The cleaned analytical structure is:

| Field | Description |
|---|---|
| `COUNTY CODE` | County/location identifier |
| `COUNTY` | County or special location |
| `Region` | Eight Kenyan regions; Diaspora/Prisons retained as Other |
| `Age Group` | 18–24, 25–35, 36–45, 46–55, Over 55 |
| `Gender` | Female or Male |
| `Registered Voters` | Number of registered voters |

The dataset contains **49 locations**: 47 counties, Diaspora, and Prisons. With five age groups and two genders, this produces **490 analytical records**.

## Power BI Dashboard
![Kenya 2022 Voter Demographics Dashboard](screenshots/gender_demographic_analysis_dashboard.png)

### Measures

- Total Registered Voters
- Male Voters
- Female Voters
- Male %
- Female %
- Gender Gap
- Female Share %

### Visualizations

1. Registered Voters by Age Group and Gender
2. Overall Registered Voters by Gender
3. Registered Voters by Region and Gender
4. Male–Female Voter Gap by Region
5. Female Share of Registered Voters by Region
6. Age and Gender Distribution by Region

### Regions

- Central
- Coast
- Eastern
- Nairobi
- North Eastern
- Nyanza
- Rift Valley
- Western

Diaspora and Prisons remain under **Other** rather than being assigned to a geographic region.

## Data Preparation

The original wide-format age/gender columns were transformed in Power Query into a normalized structure:

```text
COUNTY CODE
COUNTY
Age Group
Gender
Registered Voters
```

The source `TOTAL` column was not used as the combined voter total because, in the supplied data structure, it corresponded to the female total. Combined totals are calculated from the male and female records.

## Skills Demonstrated

- Power Query data cleaning
- Data transformation and normalization
- DAX
- Demographic analysis
- Regional aggregation
- Gender analysis
- Interactive Power BI dashboard design
- Data storytelling

## Important Note

This project analyzes the supplied **2022 voter-registration dataset**. It should not be presented as an official 2027 voter register or a 2027 forecast unless a separate projection methodology and source are added.

## Repository Structure

```text
kenya-voter-demographics-2022/
│
├── README.md
├── data/
│   └── voter_gender_age_2022.csv
│
├── powerbi/
│   └── Kenya_Voter_Demographics_2022.pbix
│
├── screenshots/
│   ├── dashboard_overview.png
│   ├── gender_by_age.png
│   └── regional_analysis.png
│
├── documentation/
│   └── methodology.md
│
└── LICENSE
```

## Author

**Joseph Mugo**

Data Analysis Portfolio Project

## Tools

- Microsoft Power BI
- Power Query
- DAX
- GitHub

## Status

**Dashboard analysis completed — repository packaging in progress.**
