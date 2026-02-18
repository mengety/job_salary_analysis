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
                        └── dashboard.png
                            

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

## 📊 Dashboard Preview
dashBoard.png

🚀 How to Use

Open Job_Salary_Analysis.xlsx

Select:

         Job title

         Country

        Schedule type

View automatically calculated median salary and chart  and map.

📊 Skills Demonstrated

          Excel Data Analysis

          Structured Tables

          Advanced Filtering Logic

          Conditional Array Formulas

          Salary Data Cleaning

          Analytical Thinking

🔮 Future Improvements in the upcoming days

Add salary visualization charts

Add experience-level filtering

Convert to Power BI dashboard

Automate data update with Power Query


## 📜 License

This project is licensed under the MIT License.

You are free to use, modify, customize, and distribute this project for personal or commercial purposes.

See the LICENSE file for full details.


## 📊 Data Source & Acknowledgment

The dataset used in this project was provided by Luke Barousse through his platform:

[datanerd.tech](https://datanerd.tech/)

Special thanks to Luke Barousse for making high-quality job market datasets available for educational and analytical purposes.

This project is an independent analysis and is not officially affiliated with Luke Barousse or Datanerd.Tech.





