# Bellabeat Fitbit Data Analysis - Usage Patterns & Wellness Insights
This repository contains my work for the **Bellabeat case study** from the Google Data Analytics programme.
The goal is to analyse Fitbit-style activity data to:
- Understand how users actually engage with their wearable devices.
- Identify patterns in activity, intensity, heart rate, sleep, and weight change.
- Generate concrete, data-backed recommendations for how Bellabeat could position and improve its products.
The analysis is implemented in **R** and summarised in a **Tableau dashboard** and a short slide presentation.
---
## Repository structure
```text
Google_Data_Analytics-Bellabeat-Project/
├── code/
├── data/
├── images/
├── presentation/
└── tableau/
```
### `code/`
- `Bellabeat_analysis.R`  
  Main R script. It:
  - Imports and cleans the Fitbit-derived datasets.
  - Merges user-level summaries.
  - Creates derived features (e.g. total active minutes, METs, activity categories).
  - Produces the aggregated tables used for visualisation and the final dashboard.
- `ggplots_bellabeat.R`  
  R script focused on visualisation:
  - Generates the key plots saved under `images/`.
  - Uses **ggplot2** and related tidyverse tools.
### `data/`
These are the **processed summary tables** created for analysis and visualisation:
- `user_summary.csv`  
  Main user-level summary table (activity / intensity / heart rate / sleep / weight metrics per user).
- `user_summary_write.csv`  
  Final export of `user_summary` tailored for Tableau (cleaned column names, simplified structure).
- `avg_daily_steps.csv`  
  Average daily steps per user.
- `avg_hourly_steps.csv`  
  Average hourly steps profile.
- `avg_user_steps.csv`  
  Additional summary of step behaviour by user.
- `avg_heart_rate_user.csv`  
  User-level average heart rate.
- `avg_mets_user.csv`  
  User-level average METs (metabolic equivalents).
- `avg_sleep_user_minutes.csv`  
  Aggregated sleep minutes per user.
- `high_intensity_summary.csv`  
  Summary of high-intensity activity (e.g. minutes or days in high activity zones).
- `hi_minutes.csv`  
  More granular high-intensity minutes data.
- `daily_steps_heart_rate.csv`  
  Combined daily steps and heart rate summary.
- `hourly_intensity_summary.csv`  
  Hourly breakdown of intensity levels.
- `weight_change.csv`  
  Weight and weight-change information where available.
These files are all derived from the original Fitbit data used in the Bellabeat case study. They’re kept here so the analysis can be reproduced and visualised without repeating every raw data-wrangling step.
### `images/`
Static PNGs created by `ggplots_bellabeat.R`:
- `act_int_vs_mets.png`
- `act_vs_rest_heart_rate.png`
- `avg_act_per_min.png`
- `mets_vs_weight_change.png`
- `steps_vs_act_type.png`
These are the main figures used in the presentation and dashboard to discuss relationships between activity, intensity, METs, heart rate and weight.
### `presentation/`
- `Bellabeat_Insights.pptx`  
  Slide deck summarising:
  - Key findings from the analysis.
  - Visuals illustrating user behaviour patterns.
  - Recommendations for Bellabeat (product focus, target users, feature emphasis).
### `tableau/`
- `Bellabeat_Dashboard.twbx`  
  Packaged Tableau workbook containing the interactive dashboard built from `user_summary_write4.csv` and related data extracts.
---
## How to run the R analysis
1. Open R or RStudio and set the working directory to the `code/` folder (or project root and adjust paths accordingly):
   ```r
   setwd("path/to/Google_Data_Analytics-Bellabeat-Project/code")
   ```
2. Make sure you have the required R packages installed (typical stack):
   ```r
   install.packages(c(
     "tidyverse",
     "lubridate",
     "janitor",
     "scales"
   ))
   ```
3. Run the main analysis script:
   ```r
   source("Bellabeat_analysis.R")
   ```
   This will:
   - Read in the CSVs from `../data/`.
   - Perform any additional cleaning/aggregation needed.
   - Overwrite or regenerate summary tables if scripted to do so.
4. Run the plotting script (optional):
   ```r
   source("ggplots_bellabeat.R")
   ```
   This will regenerate the PNG figures into the `../images/` directory, assuming the expected summary tables exist.
---
## How to use the Tableau dashboard
1. Open `tableau/Bellabeat_Dashboard.twbx` in Tableau Desktop or Tableau Public.
2. The workbook is self-contained (packaged), but it is conceptually driven by:
   - `user_summary_write4.csv`
   - Other summary tables in `data/`
Use the filters and views to explore:
- Activity levels across user segments.
- Relationships between METs, intensity, steps, and weight change.
- Patterns in daily and hourly activity behaviour.
---
## Project outline (high level)
The analysis follows the general Google Data Analytics case study pipeline:
1. **Ask**
   - Business task: identify how Bellabeat can leverage activity data to improve its products and user engagement.
   - Stakeholder: Bellabeat marketing/product team.
2. **Prepare**
   - Use the public Fitbit dataset.
   - Clean and structure the data into the summary tables in `data/`.
3. **Process**
   - Join and aggregate data to user-level and time-based summaries.
   - Create derived metrics (e.g. METs, intensity categories, active minutes).
   - Handle missing or inconsistent entries.
4. **Analyse**
   - Explore distributions of activity, sleep, intensity, heart rate, and weight.
   - Look for relationships between variables (e.g. METs vs weight change, steps vs activity type).
   - Compare behaviour patterns between different user groups.
5. **Share**
   - Build `ggplot2` visualizations (saved under `images/`).
   - Create the `Bellabeat_Dashboard.twbx` Tableau dashboard.
   - Summarise the findings in `Bellabeat_Insights.pptx`.
6. **Act**
   - Turn the findings into recommendations: which behaviours to encourage, which users to target, and what product features or messaging might be most impactful.
---
## Notes
- This is a **learning and portfolio project**, built on a teaching dataset, not real Bellabeat production data.
- The focus is on:
  - Clean data wrangling in R.
  - Sensible feature engineering and summarisation.
  - Clear visual communication through ggplot and Tableau.
  - Translating data findings into business-relevant recommendations.
