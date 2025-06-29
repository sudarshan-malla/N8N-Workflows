# Automate Data Quality Reports with n8n

## The Data Quality Bottleneck Every Data Scientist Knows

Every data scientist recognizes this scenario:

- A new dataset arrives.
- You spend 15–30 minutes running `.info()`, `.describe()`, `.isnull().sum()`, and visualizing missing data.
- This manual routine becomes tedious if you evaluate multiple datasets daily.

**This project solves that problem.**

## Solution Overview

Using a 4-node workflow in [n8n](https://n8n.io), you can analyze any CSV dataset and generate a professional data quality report in under 30 seconds — no Python environment or manual coding required.

## How It Works

The workflow includes:

1. **Manual Trigger Node**  
   Starts the workflow manually.

2. **HTTP Request Node**  
   Fetches any CSV file from a URL.

3. **Code Node**  
   - Parses CSV data.
   - Detects missing values in multiple formats.
   - Calculates an overall data quality score.
   - Provides actionable recommendations.

4. **HTML Node**  
   Creates a color-coded, professional HTML report.

## Setup Instructions

### Prerequisites

- An [n8n account](https://n8n.io) (free trial available).
- Any publicly accessible CSV URL.

### Steps

1. **Import Workflow**
   - Download the provided workflow JSON.
   - Go to n8n > Import > Import from File.
   - Save the workflow with your preferred name.

2. **Customize CSV URL**
   - Click the HTTP Request node.
   - Replace the example URL with your dataset:
     ```
     https://your-domain.com/your-dataset.csv
     ```

3. **Run the Workflow**
   - Click **Execute Workflow**.
   - Review the HTML output for your data quality report.

## Example Datasets

- [Recent Grads](https://raw.githubusercontent.com/fivethirtyeight/data/master/college-majors/recent-grads.csv)
- [Titanic](https://raw.githubusercontent.com/datasciencedojo/datasets/master/titanic.csv)
- [Iris](https://raw.githubusercontent.com/uiuc-cse/data-fa14/gh-pages/data/iris.csv)

## Quality Score Interpretation

- **95–100%** – Perfect or near-perfect data.
- **85–94%** – Excellent, minimal cleaning.
- **75–84%** – Good, moderate cleaning.
- **60–74%** – Fair, more significant preprocessing needed.
- **< 60%** – Poor quality, significant remediation required.

## Potential Enhancements

- Scheduled data quality checks.
- Email reports directly to stakeholders.
- Support additional formats (JSON, XLSX).
- Compare multiple datasets in one run.

## Why n8n?

- No-code/low-code, but customizable for advanced logic.
- Visual, shareable workflows.
- Faster iteration vs. standalone scripts.

This project demonstrates how automation bridges the gap between data science expertise and practical, shareable solutions across teams.

---
