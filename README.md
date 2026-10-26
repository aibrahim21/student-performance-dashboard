# Student Performance Dashboard

An interactive Power BI dashboard that explores student Math, Reading, and Writing scores across lunch type, test preparation, gender, race/ethnicity, and parental education.

![Dashboard preview](student_dashboard_updated.png)

## Overview

This project analyzes a dataset of 1,000 students (`study_performance.csv`) to show how different factors relate to academic performance. The dashboard lets viewers explore the full student cohort and filter it to compare groups.

## Features

- **KPI cards:** Total Students, Average Math Score, Average Reading Score, Average Writing Score
- **Overall Performance:** how the three subject scores compare
- **Gender Distribution:** student breakdown by gender
- **Performance Gap by Race/Ethnicity:** score differences between groups
- **Parental Education Impact:** how parents' education level relates to scores
- **Slicers:** filter the whole report by **Lunch Type** and **Test Preparation**

## Tools Used

| Tool | Purpose |
|------|---------|
| **Power BI** | Data modeling, DAX measures, visuals, and interactivity |
| **Figma** | Designing the dashboard layout, cards, icons, and background |
| **Microsoft Fabric** | Source of the color themes (.json) applied to the visuals |

## Design Process

1. **Layout in Figma:** I designed the dashboard frame (header, filter bar, KPI cards, and a 2x2 chart grid) at 1280 x 720 px and exported it as a PNG.
2. **Background in Power BI:** The exported image is used as the canvas background. The canvas is set to a custom 1280 x 720 px size and the page view is set to **Fit to page**, so the dashboard displays without scrolling.
3. **Visuals on top:** Power BI visuals are placed over the empty cards from the Figma design.
4. **Theme from Microsoft Fabric:** I applied a downloaded theme through **View > Themes > Browse for themes** to restyle the chart colors and fonts consistently.

## Repository Contents

```
├── student_performance_dashboard.pbix   # Power BI report file
├── student_dashboard_updated.png        # Dashboard design / preview image
├── study_performance.csv                # Dataset (1,000 students)
└── README.md
```

## How to Open

1. Install [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (Windows).
2. Download or clone this repository.
3. Open `student_performance_dashboard.pbix`.
4. If Power BI asks for the data source, point it to `study_performance.csv`.
5. Use **View > Page view > Fit to page** for the best display.

## What I Learned

- Designing a dashboard layout in Figma and bringing it into Power BI as a canvas background
- Setting custom canvas sizes and page view so a report fits without scrolling
- Applying and customizing JSON themes for consistent visual styling
- Building slicers that filter every visual on the page

## Author

**Amira Ibrahim**
Aspiring Data Analyst | Computer Science graduate, Assiut University

Feel free to open an issue or reach out with feedback.
