# Media-Analytics-Power-Query-Framework
Power Query transformation framework automating ingestion,  cleansing, validation, and consolidation of multi-platform  media datasets into analytics-ready reporting outputs.

# 📊 Media Analytics Power Query Transformation Framework

## Project Overview

Designed and developed a reusable Power Query-based ETL and data transformation framework to automate the ingestion, cleansing, validation, and consolidation of multi-source media reporting datasets into a unified analytics-ready dataset.

This project demonstrates practical ETL concepts, data transformation, and data quality techniques commonly used in reporting, analytics, and business intelligence environments.

---

## Business Problem

Media reporting data is often received from multiple sources with varying structures, inconsistent formatting, duplicate records, and missing business-critical metrics.

Manual consolidation, validation, and standardization of these datasets can be time-consuming, repetitive, and prone to errors.

The objective of this project was to automate the transformation process and improve data readiness for analytics and reporting.

---

## Solution

Built a Power Query-based ETL workflow capable of:

* Automated folder-based file ingestion
* Multi-source dataset consolidation
* Schema standardization
* Data type validation and conversion
* Platform identification from source files
* Duplicate record detection and removal
* Data quality validation
* Reporting-ready dataset preparation

---

## ETL Workflow

### Extract

* Imported multiple Excel files from a folder
* Automatically identified and processed source datasets

### Transform

* Combined source files into a single dataset
* Standardized column structures
* Applied data type conversions
* Extracted platform names from filenames
* Removed duplicate records
* Implemented data quality validation rules
* Generated reporting-ready data structure

### Load

* Loaded the transformed dataset into a consolidated reporting model
* Prepared data for reporting, dashboarding, and analytics

---

## Dataset

The project simulates media reporting data received from multiple content providers and includes:

* Content metadata
* Genre classifications
* Viewership metrics
* Revenue metrics
* Country information
* Language information
* Asset classifications

### Dataset Structure

| Column      |
| ----------- |
| Platform    |
| Report_Date |
| Content_ID  |
| Title       |
| Genre       |
| Country     |
| Language    |
| Asset_Type  |
| Views       |
| Revenue     |
| DQ_Status   |

---

## Data Quality Flags

| Flag                    | Description                        |
| ----------------------- | ---------------------------------- |
| Valid                   | All required metrics are available |
| Missing Views           | Viewership data is unavailable     |
| Missing Revenue         | Revenue data is unavailable        |
| Missing Revenue & Views | Both metrics are unavailable       |

---

## Key Transformations

### Automated File Ingestion

* Imported multiple Excel files from a folder
* Combined source datasets automatically
* Eliminated manual file-by-file processing

### Platform Identification

Extracted platform names from source filenames.

```powerquery
Text.BeforeDelimiter([Source.Name], "_")
```

### Data Standardization

* Standardized column structures across all datasets
* Applied consistent naming conventions
* Converted columns to appropriate data types
* Reordered columns for reporting readiness

### Duplicate Detection & Removal

Implemented duplicate record identification and removal to improve reporting accuracy.


### Data Quality Validation

Created a DQ_Status field using business validation rules.

```powerquery
if [Revenue] = null and [Views] = null then "Missing Revenue & Views"
else if [Revenue] = null then "Missing Revenue"
else if [Views] = null then "Missing Views"
else "Valid"
```

### Reporting Dataset Preparation

Prepared a clean reporting-ready dataset by:

* Applying data quality checks
* Standardizing source data
* Removing duplicate records
* Consolidating multiple files into a single dataset
* Organizing columns for downstream reporting and analytics

---

## Power Query Workflow

```text
Source Files
      ↓
Folder-Based Ingestion
      ↓
Combine Files
      ↓
Platform Extraction
      ↓
Data Standardization
      ↓
Duplicate Removal
      ↓
Data Quality Validation
      ↓
Reporting-Ready Dataset
```

---

## Technical Skills Demonstrated

* Power Query
* Power Query M Language
* ETL Concepts
* Folder-Based Data Ingestion
* Multi-File Consolidation
* Data Transformation
* Data Standardization
* Data Quality Validation
* Duplicate Detection
* Data Cleansing
* Reporting Automation
* Business Intelligence Preparation

---

## Technologies Used

* Microsoft Excel
* Power Query
* Power Query M Language
* ETL Concepts
* Data Quality Management
* Business Intelligence

---

## Repository Contents

| File                      | Description                                                                |
| ------------------------- | -------------------------------------------------------------------------- |
| README.md                 | Project documentation and implementation overview                          |
| PowerQuery_M_Code.txt     | Power Query M code used for data ingestion, transformation, and validation |
| Before_Transformation.png | Raw dataset before applying transformation logic                           |
| DQ_Validation.png         | Data quality validation logic and DQ_Status implementation                 |
| Final_Output.png          | Final consolidated analytics-ready dataset                                 |

---

## Outcome

Successfully developed a reusable Power Query-based ETL and transformation framework that automates data preparation workflows and produces a clean, validated, and analytics-ready dataset.

The solution demonstrates practical experience in:

* Data Ingestion
* Data Transformation
* Data Quality Validation
* Duplicate Detection & Removal
* Data Standardization
* Reporting Automation
* ETL Concepts using Power Query

The final output provides a consolidated reporting dataset suitable for analytics, dashboarding, and business intelligence applications.

---


