# Monthly-Report-Portfolio
# HSEQ Monthly Report — Dashboard Design Case Study

A technical case study of an Production and HSEQ monthly reporting solution, using the October 2026 presentation as the visual reference.

## Overview

The report brings together data for production and quality, material assurance, non-conformance reports, root-cause signals, customer complaints, health and safety, testing, and training.

The source data is maintained in multiple worksheets within SharePoint-hosted workbooks. Power Query prepares the data for analysis, the Power BI semantic model connects related tables, and DAX measures provide the calculations used by report visuals.

This repository presents selected screenshots from the presentation master to show the intended report design. The images are presentation screenshots, not screenshots of a completed interactive Power BI report.

## Data architecture

**SharePoint workbooks and worksheets → Power Query → semantic model → DAX measures → report visuals**

### SharePoint sources

The source workbooks are stored in SharePoint and contain separate worksheets for HSEQ reporting areas. Power Query connects to the relevant files and selects the worksheets needed for the report.

### Power Query transformations

Power Query is used to prepare the source data before it enters the semantic model. Typical preparation steps include selecting relevant columns, setting data types, standardizing field names and categories, and applying the transformations needed for reporting.

Where worksheets have compatible structures, their data can be combined. Worksheets covering different subject areas are retained as separate tables.

### Power BI semantic model

The prepared tables are loaded into the Power BI semantic model. Relationships connect related tables using shared keys and date fields, allowing report filters to work across connected HSEQ subject areas.

The semantic model provides a consistent structure for analyzing the source data. It contains the tables and relationships used by report visuals and DAX measures.

### DAX measures and report visuals

DAX measures calculate the values presented in the report, such as monthly totals, status counts, rates, and period comparisons. Report visuals use these measures and model fields to display KPI cards, trends, comparisons, and category breakdowns.

The report output depends on the SharePoint source data, Power Query transformations, semantic-model relationships, and DAX measures working together. Refreshing the model updates the report from its connected sources, subject to the configured credentials and refresh settings.

## Selected views

### Executive overview

![Executive overview](images/executive-overview.png)

### Production and quality

![Production and quality](images/production-quality.png)

### TestBay

![TestBay](images/hse-dashboard.png)

## Design focus

- Consistent page hierarchy, colors, typography, and spacing
- Clear KPI summaries and trend views
- Navigation across HSEQ reporting areas
- Visual consistency across summary and detail pages
- A layout designed to make operational status and areas requiring attention easy to scan

## Tools and technologies

- Microsoft SharePoint — source workbook storage
- Power Query — data connection and transformation
- Power BI semantic model — tables and relationships
- DAX — KPI and reporting calculations
- Microsoft Power BI — report visuals
- Microsoft PowerPoint — visual design reference

## Notes

The screenshots in this repository are from the presentation master and illustrate the intended design. They do not, by themselves, demonstrate a completed interactive Power BI report.

Before making this repository public, confirm that the screenshots and any company information shown in them are approved for public sharing. Do not publish SharePoint URLs, workspace identifiers, credentials, employee-level records, or confidential company data.
