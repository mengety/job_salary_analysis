📊#Job Salary Analysis (Excel Project)
📌 Project Overview

This project is an interactive Excel-based salary analysis tool that helps users determine the median salary of a job based on:

              🌍 Country

             🕒 Job Schedule Type (Full-time, Part-time, Contract, etc.)

💼 ##Job Title

The goal is to help job seekers, analysts, and researchers quickly analyze salary trends across different countries and work types using structured Excel formulas and data filtering techniques.

🎯## Project Objective

Many job seekers struggle to understand:

What is the realistic salary in a specific country?

Does schedule type affect salary?

What is the median salary for a job role?

This Excel tool solves that by dynamically calculating:

Median Salary = MEDIAN(filtered salaries based on selected filters)

🛠️ Features

✅ Dynamic filtering by:

Job Title

Country

Schedule Type

✅ Uses advanced Excel functions:

MEDIAN()

IF()

SEARCH()

ISNUMBER()

Structured table references

✅ Ignores zero salaries automatically
✅ Works with large structured datasets
✅ Clean analysis-ready design

📂 File Structure
job-salary-analysis/
│
├── Job_Salary_Analysis.xlsx
├── README.md
└── screenshots/
    ├── dashboard.png
    └── formula_example.png

📈 How It Works

The core formula logic:

=MEDIAN(
    IF(
        (jobs[job_title_short]=A2) *
        (jobs[salary_year_avg]<>0) *
        (jobs[job_country]=country) *
        (ISNUMBER(SEARCH(schedule,jobs[job_schedule_type]))),
        jobs[salary_year_avg]
    )
)

🔍 What This Formula Does

Filters rows where:

Job title matches selected job

Salary is not zero

Country matches selected country

Schedule type contains selected schedule

Extracts valid salaries

Returns the median salary

This ensures:

Outliers don’t distort results

Zero values are ignored

Results are country-specific

Results are schedule-specific

#🧠 Why Median Instead of Average?

The median is used instead of the average because:

Salaries often contain extreme outliers

Median gives a more realistic central salary

Better for job market analysis

🖼️ Screenshots
## 📊 Dashboard Preview

![Dashboard](screenshots/dashboard.png)


Add These:

📊 Dashboard view

📐 Formula view

📋 Data table preview

📌 Where to Put Screenshots

Create a folder inside your project:

screenshots/


Then save your images like:

screenshots/dashboard.png
screenshots/formula_example.png


In README, display them like this:

## Dashboard Preview

![Dashboard](screenshots/dashboard.png)

## Formula Example

![Formula](screenshots/formula_example.png)

🚀 How to Use

Open Job_Salary_Analysis.xlsx

Select:

Job title

Country

Schedule type

View automatically calculated median salary

📊 Skills Demonstrated

Excel Data Analysis

Structured Tables

Advanced Filtering Logic

Conditional Array Formulas

Salary Data Cleaning

Analytical Thinking

🔮 Future Improvements

Add salary visualization charts

Add experience-level filtering

Convert to Power BI dashboard

Automate data update with Power Query

📍 Where To Put Everything

If uploading to GitHub:

Create new repository
Name: job-salary-analysis

Upload:

Excel file

README.md

screenshots folder

💡 Should You Add Screenshots?

YES. Always.

Recruiters:

Do not download Excel first

They look at screenshots

They scan README quickly

Screenshots increase project professionalism by 200%.