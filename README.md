# RetentionIQ — Customer Churn Analytics Dashboard

RetentionIQ is a self-contained, browser-based customer analytics dashboard built to explore customer churn, understand retention patterns, and identify customer groups that may need targeted retention strategies.

The dashboard includes an embedded customer churn dataset and supports loading another CSV file locally. It is designed for interactive exploratory analysis without requiring a backend or database.

## Dashboard Preview

Open the dashboard directly from the repository:

**[Launch RetentionIQ](https://manikantakarthik30-blip.github.io/BUSINESS-DASHBOARD/)**

> GitHub Pages must be enabled for the link above to work. You can also download `index (1).html` and open it in a modern browser.

## Project Overview

Customer churn occurs when customers stop using a product or service. Understanding which customers leave, when they leave, and the factors associated with churn helps businesses improve customer experience and reduce avoidable revenue loss.

RetentionIQ turns customer-level data into an interactive dashboard. It helps users explore churn outcomes, compare customer segments, inspect revenue-related patterns, and review individual records.

## Dashboard Sections

| Section | Purpose |
|---|---|
| **Overview** | High-level churn and retention metrics, customer outcome distribution, trend/relationship charts, and automatically generated insights. |
| **Customer Segments** | Compare churn behavior across customer attributes and identify segments with elevated churn. |
| **Revenue Analysis** | Explore revenue and charges alongside customer churn and retention patterns. |
| **Data Explorer** | Search, sort, filter, paginate, and inspect customer-level records. |

## Key Features

- **Customer churn KPIs** — summary metrics for the loaded customer dataset.
- **Interactive visualizations** — charts for customer outcomes, segment comparisons, distributions, and relationships between selected variables.
- **Dynamic filtering** — apply filters across available categorical and date fields, and clear them when needed.
- **Customer search** — search the dashboard and the customer-level table.
- **Segment analysis** — compare groups using churn and retention outcomes.
- **Revenue exploration** — inspect billing and revenue-related fields.
- **CSV upload** — load a different CSV file directly in the browser.
- **Filtered CSV export** — export the currently filtered customer records.
- **Table controls** — sort columns, choose visible columns, and change page size.
- **Display controls** — switch between dark and light themes, use fullscreen, and print the dashboard.
- **Local processing** — the dashboard parses and analyzes the data in the browser; no application server is required.

## Dataset

The repository's HTML file contains an embedded customer churn dataset named `Customer_Churn_Cleaned(2).csv`. The embedded data includes customer, service, contract, billing, tenure, location, churn, and revenue-related attributes.

Examples of fields present in the embedded dataset include:

- **Customer profile:** Customer ID, age, gender, marital status, dependents, senior citizen, and location.
- **Services:** Internet service and type, phone service, multiple lines, online security, online backup, device protection, streaming services, and technical support.
- **Account and billing:** Contract, payment method, paperless billing, monthly charges, total charges, and total revenue.
- **Customer lifecycle and outcomes:** Tenure in months, customer status, churn category, churn reason, and churn score.

The dashboard also detects columns from an uploaded CSV, allowing the analysis to adapt to a different compatible customer dataset. The exact fields available in charts and filters depend on the columns in the loaded file.

## Technology Stack

| Technology | Usage |
|---|---|
| **HTML5** | Dashboard structure and content |
| **CSS3** | Responsive layout, styling, themes, and visual components |
| **JavaScript (Vanilla)** | CSV parsing, data processing, filters, calculations, charts, table interactions, and export |

No React, build tool, package installation, backend API, or database is required by the current implementation.

## Run Locally

### Option 1 — Open in a browser

1. Open the repository.
2. Download `index (1).html`.
3. Open the downloaded file in a modern browser such as Chrome, Edge, or Firefox.

The embedded dataset loads automatically when the page starts.

### Option 2 — Run with a local development server

If you use VS Code, you can open the repository folder and run the HTML file with the Live Server extension. Alternatively, from the project directory:

```bash
python -m http.server 8000
```

Then open:

```text
http://localhost:8000/
```

If the HTML file is named `index (1).html`, open `http://localhost:8000/index%20(1).html`.

## Use Your Own Dataset

1. Open RetentionIQ in your browser.
2. Use the CSV upload control in the dashboard.
3. Select a valid CSV file with a header row and customer-level records.
4. Explore the recalculated KPIs, charts, filters, and customer table.
5. Apply the filters you need and use the CSV export control to download the filtered records.

The dashboard processes uploaded data locally in the browser. It does not upload the CSV to a server.

## Repository Structure

```text
BUSINESS-DASHBOARD/
├── README.md
└── index (1).html
```

The HTML file currently contains the dashboard markup, styles, JavaScript logic, and embedded dataset in one self-contained file.

## Project Goals

- Make customer churn patterns easier to understand.
- Identify customer segments with comparatively high churn.
- Explore relationships between service usage, contract attributes, billing, and churn.
- Support evidence-based customer retention analysis.
- Provide an accessible dashboard that can be opened without a complex setup.

## Limitations

- The current project is a client-side analytics dashboard, not a production customer data platform.
- The embedded dataset is the default analysis input; uploading another CSV replaces the active in-memory dataset for that browser session.
- Insights and associations shown by the dashboard are descriptive. They do not, by themselves, establish causation or predict future churn.
- No authentication, role-based access, server-side storage, or automated data synchronization is implemented in the current single-file application.
- Uploaded customer data remains in the browser session; use appropriately anonymized data when sharing or demonstrating the dashboard.

## Future Improvements

- Add a documented data dictionary and validation report for uploaded datasets.
- Add cohort-based retention analysis and churn trends over time when reliable date fields are available.
- Add exportable charts and a downloadable analysis report.
- Add optional churn prediction with a separately validated machine-learning model.
- Improve accessibility and add automated tests for CSV parsing and analytical calculations.

## Author

**Manikanta Balaga**

GitHub: [@manikantakarthik30-blip](https://github.com/manikantakarthik30-blip)

---

**RetentionIQ — Explore customer behavior. Understand churn. Support better retention decisions.**
