# Heart Disease Data Analysis — Tableau

An interactive Tableau dashboard suite exploring clinical and demographic risk factors associated with heart disease.

## Overview

This project analyzes a patient-level heart disease dataset to identify patterns across age, gender, and clinical indicators (blood pressure, cholesterol, chest pain type, heart rate, and ECG-related measures) that distinguish diagnosed patients from healthy individuals. The goal is to turn raw clinical data into an interpretable, visual narrative for non-technical stakeholders.

## Dataset

Patient-level records with attributes including `Age`, `Sex`, `ChestPainType`, `RestingBP`, `Cholesterol`, `MaxHR`, `ExerciseAngina`, `ST_Slope`, and `HeartDisease` (diagnosis flag).

## Tools & Technologies

- **Tableau** — interactive data visualization
- **CSV** — data storage format

## Dashboards

The workbook (`heart disease analysis.twbx`) contains **15 worksheets** across **2 dashboards**:

| Dashboard | Focus |
|---|---|
| **DB1 — Overview** | Max heart rate distribution (patient vs. normal), age distribution histogram, gender breakdown (donut charts), gender × chest pain type comparison |
| **DB2 — Clinical Indicators** | KPI cards (% patients, average age, max heart rate), resting blood pressure distribution, chest pain type breakdown, exercise-induced angina and ST slope (pie charts), male vs. female diagnosis comparison |

**Notable techniques:**
- **Calculated fields** — a dynamic patient-percentage KPI: `(COUNT(IF [HeartDisease]=1 THEN 1 END) / COUNT([HeartDisease])) * 100`
- **Custom binning** — bins on `Age`, `MaxHR`, and `RestingBP` to build meaningful distribution histograms
- **Comparative visual encoding** — density/area charts and icon-based dumbbell charts to contrast patient vs. non-patient populations

## Key Insights

- Patients show a higher concentration in the 50–60 age range compared to the non-patient population.
- Asymptomatic chest pain (**ASY**) is disproportionately associated with a heart disease diagnosis, especially among male patients.
- A flat ST slope is far more common among diagnosed patients than an upsloping or downsloping pattern.
- Exercise-induced angina is present in the majority (62%) of diagnosed patients.

## Repository Structure

```
heart-disease-data-analysis/
├── heart disease analysis.twbx   # Tableau packaged workbook (dashboards)
└── README.md
```

## How to Use

1. Download or clone the repository.
2. Open `heart disease analysis.twbx` in Tableau Desktop or Tableau Public.
3. Explore the interactive dashboards and filters.

## Author

**Mohamed Wasef**
[LinkedIn](https://www.linkedin.com/in/mohamed-wasef-789743233/) · [GitHub](https://github.com/Mo7239)
