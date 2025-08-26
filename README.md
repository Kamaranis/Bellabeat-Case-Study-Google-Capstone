# Fitbit User Insights: A Google Data Analytics Capstone Project

## 📄 Project Overview & Business Task

This repository contains my capstone project for the **Google Data Analytics Professional Certificate**. The project is a real-world case study where I act as a junior data analyst for **Bellabeat**, a high-tech company that manufactures health-focused smart products for women.

The central business task was to analyze user data from a competitive product (Fitbit) to uncover insights into consumer behavior. The final goal is to deliver data-driven recommendations that can guide Bellabeat's marketing strategy and product development.

## ✨ A Structured Analysis Following the Google Framework

This project rigorously follows the six steps of the data analysis process as taught by Google: **Ask, Prepare, Process, Analyze, Share, and Act**.

### 1. Ask & Prepare
*   **Business Objective:** Identify trends in smart device usage to inform Bellabeat's growth opportunities.
*   **Data Vetting:** The initial phase involved a critical evaluation of the provided dataset (Fitbit Fitness Tracker Data from Kaggle). I identified key limitations, including a small sample size (30 users), outdated information (from 2016), and a lack of demographic data, which are crucial considerations for a real-world business scenario.

### 2. Process: A Hybrid R & SQL Data Cleaning Pipeline

This phase was focused on transforming 18 raw, disorganized CSV files into a single, unified, and clean dataset ready for analysis.
*   **Data Cleaning in R:** Used the **Tidyverse** suite in R to process the majority of the datasets. This involved:
    *   Standardizing date and time formats across all files.
    *   Merging multiple tables (e.g., `dailyActivity`, `sleepDay`, `weightLogInfo`) into a cohesive master table.
    *   Checking for and handling inconsistencies.
*   **Handling Big Data with SQL:** The `heartrate_seconds` dataset was too large for efficient processing in memory with R. I demonstrated adaptability by:
    1.  Uploading the data to **Google BigQuery**.
    2.  Using **SQL queries** to clean the data and aggregate the second-level heart rate data into hourly averages.
    3.  Importing the processed, smaller dataset back into R to merge with the main table.

### 3. Analyze & Share: Uncovering Key Insights

With the clean, unified dataset, I performed a deep exploratory data analysis to uncover user habits.
*   **Key Findings:**
    *   A strong positive correlation was found between total steps and calories burned, confirming that daily activity is a key driver of energy expenditure.
    *   Analysis of activity intensity revealed that users spend the vast majority of their time in sedentary or lightly active states, with very few minutes of high-intensity activity.
    *   Sleep analysis showed most users get within the recommended 7-9 hours of sleep, but there is a negative correlation between sedentary time and sleep quality.
*   **Visualizations:** The analysis is supported by a variety of visualizations created with `ggplot2` in R, including scatter plots, bar charts, and time-series plots to make the findings clear and actionable.

### 4. Act: Data-Driven Business Recommendations

The project culminates in a set of strategic recommendations for Bellabeat, directly derived from the data insights:
*   **Recommendation 1 (Marketing):** Launch targeted campaigns encouraging users to convert light activity into moderate activity, highlighting the significant calorie-burn benefits.
*   **Recommendation 2 (App Features):** Implement a "sedentary alert" feature in the Bellabeat app that nudges users to move after prolonged periods of inactivity, explaining the positive impact on sleep.
*   **Recommendation 3 (Product):** Develop personalized daily and weekly summary reports that focus on key achievements (like total steps and sleep quality) to keep users engaged and motivated.

## 💻 Technologies & Tools

*   **Languages:** R, SQL
*   **R Packages:** `Tidyverse` (including `dplyr`, `ggplot2`), `janitor`, `skimr`
*   **Database:** Google BigQuery
*   **Environment:** RStudio

## 🚀 Getting Started

1.  **Clone the repository.**
2.  The repository contains the R Markdown file with the complete, documented code.
3.  The raw data can be downloaded from [this Kaggle link](https://www.kaggle.com/datasets/arashnic/fitbit).
4.  Follow the steps in the notebook to reproduce the entire analysis from data cleaning to final recommendations.

## 👤 Author

**[Tu Nombre]**

*   **LinkedIn:** [Tu Perfil de LinkedIn]
*   **GitHub:** @Kamaranis