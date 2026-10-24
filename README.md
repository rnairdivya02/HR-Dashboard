# HR Analytics Dashboard

A Power BI dashboard for exploring workforce trends, hiring performance, employee separations, and potentially unsuccessful hires. The report is organized into four pages so users can move from a high-level overview to more focused analyses.

## Contents

- `Assignment.pbix` — Power BI report file.
- `Mapping File.xlsx` — Supporting lookup and mapping tables used by the report.

## Dashboard Pages

### 1. Index
Provides a high-level entry point to the report, including summary indicators for:
- New Hires
- Active Employees
- Bad Hires

Use this page to orient yourself before moving to a detailed analysis page.

### 2. New Hires
Examines hiring performance for the current year compared with the previous year. The report includes measures for:
- New Hires CY (current year)
- New Hires LY (previous year)
- Variance between current year and previous year
- Variance percentage

The page also breaks hiring results down by dimensions such as age group, job type, region, and vice president (VP).

### 3. Active Employees vs. Separated Employees
Compares the active workforce with employees who have separated. The report includes:
- Active Employees and their percentage
- Separated Employees and their percentage
- Separation-related comparisons and breakdowns

Available analysis dimensions include age group, separation reason, and region.

### 4. Bad Hires
Focuses on the report's “Bad Hires” measure in relation to the total employee population. The page includes:
- Total Employees
- Bad Hires
- Bad Hires percentage

The report also supports breakdowns by year, job type, and region.

> **Metric definitions:** The names above reflect the measures and labels present in the Power BI report. Confirm the exact business definitions, inclusion rules, and date logic in the report's DAX measures or with the report owner before using the figures for formal HR decisions.

## Supporting Mapping Workbook

`Mapping File.xlsx` contains lookup tables used to categorize or organize report data.

| Worksheet | Purpose / values represented |
|---|---|
| `AgeGroup` | Age-group IDs and labels (`<30`, `30-49`, `50+`) |
| `RegionMapping` | Business unit, region sequence, VP, and region mapping |
| `PeriodMapping` | Calendar attributes, including date, month, period, quarter, year, month start/end dates, and month increment |
| `Ethnicity` | Ethnicity/group IDs and labels (`Group A` through `Group G`) |
| `JobType` | Job-type codes and descriptions (Full-Time, Part-Time) |
| `Gender` | Gender IDs, labels, and sort order |
| `PayType` | Pay-type codes and descriptions (Hourly, Salaried) |
| `Seperation` | Separation-type IDs and reasons (Involuntary, Voluntary) |

**Note:** The worksheet is named `Seperation` in the supplied workbook. Preserve that name in any existing references unless you also update the Power BI model.

## How to Open and Use the Dashboard

1. Install or open **Microsoft Power BI Desktop**.
2. Open `Assignment.pbix`.
3. Wait for the report and its data model to load.
4. Use the page navigation to open **Index**, **New Hires**, **Active Employees v/s Separated Employees**, or **Bad Hires**.
5. Use available slicers, filters, and visual interactions to focus on a year, region, job type, age group, or other available category.
6. Select a data point in a visual to cross-filter or highlight related visuals, where interactions are enabled.
7. Hover over a visual to view any available tooltips.

The exact filter controls and interactions depend on the report configuration.

## Data Refresh and Maintenance

- Open the PBIX in Power BI Desktop to review its data sources, queries, relationships, measures, and refresh settings.
- If the source data or mapping workbook changes, verify the file paths and credentials in **Transform data** and **Data source settings**, then refresh the model.
- When adding new mapping values, check that the relevant keys match the fact data and that relationships remain valid.
- Confirm date-table coverage and sorting for period fields before extending the reporting period.
- After changing DAX measures or mappings, validate the results against known totals and representative records.
- If publishing to Power BI Service, configure the required credentials and gateway (if applicable) and verify scheduled refresh settings.

## Important Notes and Limitations

- This README documents the report structure and mapping workbook. It does not independently validate the underlying HR data or the business logic behind each measure.
- The exact source-system tables, refresh cadence, access permissions, and calculation rules should be documented by the report owner if they are required for operational use.
- HR data can be sensitive. Follow organizational access controls and privacy requirements when sharing the PBIX, workbook, screenshots, or exported data.
- Confirm whether “Bad Hires” is an officially defined business term and how it is calculated before interpreting or sharing the metric.

## Suggested Future Improvements

- Add a data dictionary describing each KPI and its DAX definition.
- Document the source systems, refresh schedule, data owner, and reporting period.
- Add a “Last Refreshed” indicator to the report.
- Include validation checks for missing or unmatched mapping keys.
- Document expected access permissions and the process for reporting data issues.

## File List

```text
.
├── Assignment.pbix
├── Mapping File.xlsx
└── README.md
```
