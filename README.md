# Student Performance Dashboard

An interactive Power BI dashboard that explores how 1,000 students performed in Math, Reading, and Writing, and how scores differ by gender, race/ethnicity, and parental education.

![Dashboard screenshot](dashboard_screenshot.png)

## Project Goal

To turn a flat student exam dataset into a clear, visual dashboard that answers four questions:

1. **Overall performance:** how do students score in each subject?
2. **Gender distribution:** how is the student group split between female and male students?
3. **Performance gap:** do average scores differ across race/ethnicity groups?
4. **Parental education impact:** how do score bands change with parents' level of education?

## Dataset

- **File:** `study_performance.csv`
- **Size:** 1,000 students, 8 columns, no missing values and no duplicate rows
- **Columns:** `gender`, `race_ethnicity`, `parental_level_of_education`, `lunch`, `test_preparation_course`, `math_score`, `reading_score`, `writing_score`

## Tools Used

- **Power BI Desktop:** data model, DAX measures, visuals
- **Power Query:** data cleaning and calculated columns
- **DAX:** measures for counts and averages
- **Figma:** dashboard layout and design (used as the page background)

## Data Preparation (Power Query)

- Set the three score columns to numeric types and the remaining columns to text
- Checked data quality (nulls, blanks, duplicates)
- Added a `Student ID` index column to give each row a unique key
- Added an `Avg Score` column: the average of the three subject scores
- Added a `Score Band` column: **Below 60**, **60-79**, **80+**, based on `Avg Score`
- Added an `Education Order` column (1 = some high school up to 6 = master's degree) and used **Sort by Column**, so education levels appear in the right order instead of alphabetically

## DAX Measures

- `Student Count`: number of students
- `Avg Math Score`, `Avg Reading Score`, `Avg Writing Score`: average score per subject
- `Avg Overall Score`: average of the `Avg Score` column

## Dashboard Visuals

| Visual | Chart type | What it shows |
|---|---|---|
| KPI cards | Card | Total students and the average score per subject |
| Overall Performance | Clustered column | Average Math, Reading, and Writing scores |
| Gender Distribution | Pie | Student count by gender |
| Performance Gap by Race/Ethnicity | Donut | Average overall score by group |
| Parental Education Impact | 100% stacked bar | Share of students in each score band, by parental education |
| Filters | Slicers | Lunch type and test preparation course |

## Key Findings

These numbers come directly from the dataset:

- **Overall averages:** Math 66.1, Reading 69.2, Writing 68.1 (overall average 67.8)
- **Gender:** the group has 518 female and 482 male students. Female students average higher in Reading (72.6 vs 65.5) and Writing (72.5 vs 63.3), while male students average higher in Math (68.7 vs 63.6)
- **Race/ethnicity:** the average overall score rises from Group A (63.0) to Group E (72.8)
- **Parental education:** students whose parents hold a master's degree have the highest average (73.6), and students whose parents finished only high school have the lowest (63.1). In the score bands, 34% of students with a master's-degree parent score 80+, compared with 10% of those whose parents finished high school
- **Test preparation:** students who completed the course average 72.7, compared with 65.0 for those who did not

These are patterns in this dataset only. They show association, not cause.

## Design

The layout was designed in Figma and exported as the Power BI canvas background, with the visuals placed on top of it.

[View the Figma design](ADD-YOUR-FIGMA-LINK-HERE)

## Repository Contents

```
student-performance-dashboard/
├── student_performance_dashboard.pbix   # Power BI report
├── study_performance.csv                # Dataset
├── dashboard_screenshot.png             # Screenshot of the finished dashboard
├── design/                              # Figma design export
└── README.md
```

## How to Open

1. Download `student_performance_dashboard.pbix`
2. Open it in [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free)
3. If prompted, update the data source path to point to `study_performance.csv`

## Author

**Amira Ibrahim**: aspiring data analyst, Computer Science graduate
