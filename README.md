# Bellabeat Fitbit Data Analysis Portfolio

Welcome to my portfolio showcasing a comprehensive case study for Bellabeat, using Fitbit data. This repository contains all the materials data, analysis code, visualizations, and the final presentation, to demonstrate my end-to-end analytics workflow.

---

## Repository Structure

```
Bellabeat-Project/
├── data/                       # Cleaned CSVs and raw datasets
│   ├── user_summary.csv
│   ├── avg_daily_steps.csv
│   ├── avg_heart_rate_user.csv
│   ├── avg_hourly_steps.csv
│   ├── avg_mets_user.csv
│   ├── avg_user_steps.csv
│   ├── daily_steps_heart_rate.csv
│   ├── hi_minutes.csv
│   ├── high_intensity_summary.csv
│   ├── hourly_intensity_summary.csv
│   └── weight_change.csv
├── code/                       # Analysis scripts
│   ├── Bellabeat_analysis.R              # R script combining all summaries
│   └── ggplots_bellabeat.R                # R scripts for ggplot2 charts
├── tableau/                    # Tableau workbook and exports
│   └── Bellabeat_Dashboard.twbx
├── presentation/               # Final presentation
│   └── Bellabeat_Insights.pptx
├── images/                     # Exported charts for README or PPT
│   ├── mets_vs_weight_change.png
│   ├── avg_act_per_min.png
│   ├── steps_vs_act_type.png
│   ├── act_vs_rest_heart_rate.png
│   └── act_int_vs_mets.png
└── README.md                   # This document
```


## Key Insights

* **METs vs Weight Change**: Each +1 MET correlates with \~0.23% weight loss (R²=0.29).
* **Activity Intensity vs METs**: Very-active minutes explain \~60% of MET variation (p<0.0001).
* **Activity vs Resting Heart Rate**: No single intensity bucket strongly predicts resting heart rate.
* **User Segmentation**: Users grouped into High, Moderate, Low intensity for targeted recommendations.

---

## Recommendations

* Highlight "Very Active" streaks in the Bellabeat app.
* Send light-activity reminders to boost overall METs.
* Create combined active-minute dashboards linking to resting HR trends.
* Introduce MET-based fitness challenges in marketing campaigns.

---

## Additional Resources

* **Data Sources**: Original Kaggle Fitbit dataset (CC0 Public Domain).
* **R Code**: Modular scripts in `code/` folder.
* **Tableau**: Dashboard workbook in `tableau/`, [View the Bellabeat Dashboard – Exercises](https://public.tableau.com/views/ExercisesBellabeat/Dashboard1?:language=en-GB&:sid=&:redirect=auth&showOnboarding=true&:display_count=n&:origin=viz_share_link)
* **Presentation**: Final slide deck in `presentation/`.

---
