# Anxiety Support App: Marketing Audience Identification (Data Analysis Project)

[![Project Status](https://img.shields.io/badge/Status-Complete-green.svg)]()  
[![Language](https://img.shields.io/badge/Language-R-blue.svg)]()
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)]()

## Project Overview

This project is a data analysis case study focused on identifying and characterizing high-potential target audiences for a hypothetical "Calm Button" mobile application.  The "Calm Button" app is designed to provide immediate, discreet anxiety relief, particularly in workplace settings.  The project follows the data analysis process (Ask, Prepare, Process, Analyze, Share, Act) as outlined in the Google Data Analytics Certification program.

**Disclaimer:** This is a *fictional* case study using a *simulated* dataset for educational purposes. The findings and recommendations should not be interpreted as representing real-world population trends or as definitive marketing advice.  The project is intended to demonstrate data analysis skills and techniques.

## Business Problem

The primary business problem is to optimize marketing spend and user acquisition for the "Calm Button" app.  Broad, untargeted marketing is inefficient.  To maximize ROI, we need to identify specific demographic and lifestyle segments that are:

1.  Most susceptible to anxiety (particularly in workplace contexts).
2.  Most likely to benefit from the app's features (immediate, discreet relief).
3.  Potentially "untreated" (not currently using traditional anxiety management methods like therapy or medication).

## SMART Questions

The analysis was guided by the following SMART (Specific, Measurable, Actionable, Relevant, Time-bound) questions:

**High-Stress & Lifestyle Segments:**

1.  **Stress & Severity:** Among individuals reporting high stress levels (stress_level_1_10 >= 8), what is the distribution of `severity_of_anxiety_attack_1_10`? What percentage report severe anxiety attacks (>= 8)?
2.  **Lifestyle & High Stress/Severity:** Within the high-stress, high-severity group (defined in Q1), what are the average values and distributions of key lifestyle factors: `sleep_hours`, `physical_activity_hrs_week`, `caffeine_intake_mg_day`, `alcohol_consumption_drinks_week`, and `diet_quality_1_10`? How do these compare to the overall dataset averages?
3.  **Untreated Need:** What proportion of individuals with high stress and high anxiety severity (defined in Q1) report no therapy (`therapy_sessions_per_month` = 0) and no medication use (`medication` = "No")? This identifies a potential "untreated" segment.
4.  **Age & High Stress/Severity:** Within the high-stress, high-severity group, are there significant differences in anxiety severity, lifestyle factors, or treatment usage across different age groups (e.g., 18-29, 30-44, 45-64)?
5.  **Physiological Response:** What is the average `heart_rate_bpm_during_attack` and the average `breathing_rate_breaths_min` in people with a `severity_of_anxiety_attack_1_10` of 8 or higher, versus people with a `severity_of_anxiety_attack_1_10` of 3 or lower?
 6. **Therapy Usage and Severity:** Among those who report attending therapy (`therapy_sessions_per_month` > 0) , what is the median reported `severity_of_anxiety_attack_1_10`?

**Behavioral & Contextual Analysis:**

7.  **Lifestyle Correlations:** Across the *entire* dataset, what are the correlations between the key lifestyle factors (`sleep_hours`, `physical_activity_hrs_week`, `caffeine_intake_mg_day`, `alcohol_consumption_drinks_week`, `diet_quality_1_10`) and `severity_of_anxiety_attack_1_10`? Are these correlations statistically significant?
8.  **Smoking, Family History, Dizziness, Life Events:** What proportion of individuals with high anxiety severity (>= 8) report: smoking, a family history of anxiety, dizziness during anxiety attacks and a recent major life event. How do these proportions compare to those with low anxiety severity (< 4)?
9.  **Messaging & Value Proposition:** Based on the identified needs, behaviors, and pain points of the target segments, how should the "Calm Button" app be positioned?

## Data

The dataset used in this project is a *simulated* dataset (`anxiety_attack_dataset.csv`) containing information on 12,000 individuals.  It includes the following variables:

*   **ID:** Unique identifier for each individual.
*   **Age:**  Age in years.
*   **Gender:**  Gender identity (Female, Male, Other).
*   **Occupation:**  Occupation (Doctor, Engineer, Other, Student, Teacher, Unemployed). *Note: The dataset was constructed to have a relatively even distribution across occupations, limiting the ability to draw strong conclusions about specific professions.*
*   **Sleep Hours:**  Average number of hours of sleep per night.
*   **Physical Activity (hrs/week):** Average hours of physical activity per week.
*   **Caffeine Intake (mg/day):**  Average daily caffeine intake in milligrams.
*   **Alcohol Consumption (drinks/week):** Average weekly alcohol consumption in drinks.
*   **Smoking:**  Whether the individual smokes (Yes/No).
*   **Family History of Anxiety:** Whether the individual has a family history of anxiety (Yes/No).
*   **Stress Level (1-10):**  Self-reported stress level on a scale of 1 to 10.
*   **Heart Rate (bpm during attack):**  Self-reported heart rate during an anxiety attack.
*   **Breathing Rate (breaths/min):** Self-reported breathing rate during an anxiety attack.
*   **Sweating Level (1-5):**  Self-reported sweating level during an anxiety attack.
*   **Dizziness:**  Whether the individual experiences dizziness during anxiety attacks (Yes/No).
*   **Medication:** Whether the individual is currently taking medication for anxiety (Yes/No).
*   **Therapy Sessions (per month):**  Number of therapy sessions attended per month.
*   **Recent Major Life Event:** Whether the individual has experienced a recent major life event (Yes/No).
*   **Diet Quality (1-10):** Self-reported diet quality on a scale of 1 to 10.
*   **Severity of Anxiety Attack (1-10):** Self-reported severity of anxiety attacks on a scale of 1 to 10.

## Data Analysis Process

The analysis followed the standard data analysis process:

1.  **Ask:** Define the business problem and formulate SMART research questions.
2.  **Prepare:** Import, inspect, and understand the raw data.  Identify potential data quality issues.
3.  **Process:** Clean and transform the data to prepare it for analysis (data type conversion, outlier handling, variable creation).
4.  **Analyze:** Explore relationships between variables, calculate statistics, perform statistical tests, and build models to address the research questions.
5.  **Share:** Communicate findings and recommendations through visualizations and reports.
6.  **Act:** (Hypothetical in this case study) Implement data-driven marketing strategies.

## Tools and Technologies

*   **R:** Programming language for statistical computing and graphics.
*   **RStudio:** Integrated development environment (IDE) for R.
*   **tidyverse:**  A collection of R packages for data manipulation, transformation, and visualization (including `ggplot2`, `dplyr`, `tidyr`, `readr`).
*   **skimr:**  For generating summary statistics.
*   **janitor:** For data cleaning (specifically, `clean_names()`).
*   **patchwork:** For combining multiple `ggplot2` plots.
*   **knitr:** For generating dynamic reports with R Markdown.
*   **R Markdown:**  For creating reproducible reports that combine code, results, and narrative text.

## Repository Structure

*   **`anxiety_support_app_analysis.Rmd`:**  The main R Markdown notebook containing the complete analysis, code, and narrative.  This is the primary document.
*   **`data/`:**  Directory containing the input data file (`anxiety_attack_dataset.csv`).
*   **`output/`:** Directory containing generated output files:
    *   `plots/`:  Subdirectory containing saved plots (e.g., `combined_analysis_plots.png`).
*   **`README.md`:** This file.

## How to Run the Code

1.  **Install R and RStudio:** Download and install the latest versions of R and RStudio Desktop.
2.  **Clone the Repository:** Clone this GitHub repository to your local machine:

    ```bash
    git clone [repository URL]
    ```
    Replace `[repository URL]` with the actual URL of your repository.
3.  **Open the R Markdown File:** Open the `anxiety_support_app_analysis.Rmd` file in RStudio.
4.  **Install Required Packages:** Run the following code in the R console to install the necessary packages:

    ```R
    install.packages(c("tidyverse", "skimr", "here", "janitor", "patchwork", "knitr"), dependencies = TRUE)
    ```
5.  **Set Working Directory (Optional but Recommended):** If you are *not* using an RStudio Project, set the working directory to the project's root directory. This is not necessary if you open the `.Rmd` file from within an RStudio Project.

     ```R
      setwd("path/to/your/project/directory")
      ```

     Replace `path/to/your/project/directory` with the correct path.

6.  **Knit the Document:** Click the "Knit" button in RStudio (or use `rmarkdown::render("anxiety_support_app_analysis.Rmd")`) to execute the code and generate the HTML output.

**Important Notes:**

*   The code assumes that the `anxiety_attack_dataset.csv` file is located in a subdirectory named `data` within the project's root directory.
*   The generated plots will be saved in an `output/plots` subdirectory.

## Key Findings

*   **High Stress and Severity are Prevalent, but "Untreated" is a Smaller Group:** A significant proportion of the sample reports high stress and/or severity, but the group that is *both* high stress/severity *and* not receiving treatment/medication is a smaller, potentially more receptive, target group.
*   **Weak Lifestyle Correlations:** Lifestyle factors, *in isolation*, show weak and mostly non-significant correlations with anxiety severity.
*   **Dizziness as an Indicator:** Dizziness during anxiety attacks shows a statistically significant, though weak, association with high anxiety severity.
* **Interaction Effects:** There's evidence of an interaction between stress levels and sleep.

## Limitations

*   **Simulated Data:** The findings are based on simulated data and may not generalize to real-world populations.
*   **Self-Reported Measures:**  Data relies on self-reported measures, which are subject to bias.
*   **Cross-Sectional Data:** The data is from a single point in time, preventing causal inferences.
*   **Even Occupational Distribution:** The dataset was constructed with an even distribution of occupations, which limited our ability to draw conclusions about specific professions.
