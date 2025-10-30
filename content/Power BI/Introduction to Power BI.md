
Title: Introduction to Power BI-Class Transcript and Study Notes

Date: 2025-10-29 11:50

Status: Child

Tag: [[Power BI]] [[data modeling]] [[data transformation]] [[data analysis]]

## Session Overview
This document captures the key discussions, explanations, and demonstrations from the first Power BI class in the Data Analytics Job Ready Program. The session focuses on foundational concepts, data flow, installation, and a mini-project demo. Participants include professionals from finance, IT, sales, HR, and students.

## Participant Introductions
Participants shared brief introductions via chat, including names, organizations, departments, and roles. Highlights include:
- Students from various universities and subjects.
- Professionals from finance, sales, IT, and consulting.
- Examples: Momo Sambartholeja (Minister of Finance and National Consultant), Mohammad Najbul Munir (Microsoft Certified Trainer, ACBixim Co. Pharmaceuticals Limited, Accordion Finance).

The instructor, Mohammad Najbul Munir, introduced the program as a progression from Microsoft Excel and SQL Server to Power BI, emphasizing database concepts for easier adoption.

## Power BI Fundamentals
Power BI is a reporting tool for connecting to various data sources, transforming data, creating visualizations, and sharing reports online.

### Key Features and Comparisons
- **Data Visualization**: Builds dashboards with multiple tables and sheets, similar to Excel but with dynamic drilling (e.g., category to subcategory).
- **Dynamic Reporting**: Allows interaction, such as filtering by year or region, updating the entire report.
- **Relation to Excel**: 
  - Uses Power Query (data transformation) and Power Pivot (data modeling) from Excel.
  - Advanced Excel features like Pivot Tables, Power Map, and DAX are shared.
- Participants' Views:
  - Excel-like for data visualization.
  - Supports multiple tables and dynamic drilling.

### Components of Power BI
Power BI includes:
- [[Power Query]]: For data cleaning and transformation.
- [[Power Pivot]]: For data modeling and relationships.
- **Power View**: For visualizations.
- [[Power BI]] Desktop: Main tool for building reports.
- **Power BI Service**: For publishing and sharing.
- **Power BI Mobile**: For access on devices.
- **Q&A**: Natural language queries (e.g., "Show sales by continent" generates a map).

## Data Flow in Power BI
The core process is: **Connect → Transform → Model → Visualize → Publish/Share**.

### Step-by-Step Data Flow
1. **Connect Data Sources**:
   - Databases: SQL Server, SAP, Oracle.
   - Files: CSV, Excel, Text, PDF.
   - Example: Raw sales data with invoice date, chain, country, category, unit price, cost price.

2. **Transform Data (Power Query)**:
   - Clean and reshape: Handle upper/lower case inconsistencies, trim spaces, calculate fields (e.g., profit = sales - cost).
   - Why needed: Raw data from 20+ tables may have inconsistencies; transform for accurate reporting (e.g., proper case product names).

3. **Model Data (Power Pivot/DAX)**:
   - Create relationships between tables (e.g., fact table: sales; dimension tables: country mapping, date mapping).
   - Add calculated columns/measures using DAX (Data Analysis Expressions).
   - Example: Map countries to continents (Bangladesh → Asia) for continent-wise sales.

4. **Visualize and Report**:
   - Create dashboards with charts (column, bar, pie, treemap), scorecards (totals, percentages), and slicers (filters).
   - Interactive: Click category to drill to products; filter by financial year.
   - Examples:
     - Continent-wise sales bar chart.
     - Quarter-wise sales/profit combo chart.
     - Category-wise treemap.

5. **Publish and Share**:
   - Upload to Power BI Service for online access.
   - Requires Pro license ($10/user/month) for sharing; Free for local work.
   - Supports collaboration across locations (e.g., CFO in New York views report from Chittagong).

### Visual Data Flow Diagram (Conceptual)
```
Connect Data → Transform (Power Query) → Model (Power Pivot/DAX) → Visualize Dashboard → Publish/Share
```

## Pricing and Licensing
| Plan          | Cost (per user/month) | Features |
|---------------|-----------------------|----------|
| **Free**     | $0                   | Desktop app, local reports, no publishing. |
| **Pro**      | $10                  | Publish and share reports online. |
| **Premium**  | $20                  | Advanced features for large datasets. |
| **Premium Per User** | Variable | For enterprises with bulk usage. |

- Download: Microsoft website, Microsoft Store, or Office suite (auto-updates).

## Installation Guide
1. Download from [Power BI Desktop](https://powerbi.microsoft.com/desktop/).
2. Run installer: Next → Next → Install.
3. Launch: Select "Blank Report" to start.
- System Requirements: Standard Windows setup; no complex configurations.

## Mini-Project Demonstration: Sales Dashboard
Used an Excel file with three tables: Sales (fact), Country Mapping (dimension: country → continent), Date Mapping (dimension: date → financial year/quarter).

### Steps in Power BI Desktop
1. **Connect Data**:
   - Home → Get Data → Excel Workbook.
   - Select file → Choose sheets/tables (Sales, Country Mapping, Date Mapping).
   - Transform Data → Opens Power Query Editor.

2. **Transform in Power Query**:
   - Select Sales table.
   - Add Column → Custom Column:
     - **Total Units**: `= [Quantity]` (or count logic).
     - **Profit**: `= [Sales] - [Cost]`.
   - Close & Apply → Loads to Power BI.

3. **Data Modeling**:
   - Model View → Drag to create relationships:
     - Sales[Country] → Country Mapping[Country] (one-to-many).
     - Sales[Invoice Date] → Date Mapping[Date] (one-to-many).
   - Ensures continent and quarter calculations propagate.

4. **Build Visualizations (Report View)**:
   - **Column Chart**: Axis = Continent, Values = Sales (from Country Mapping).
   - **Combo Chart**: Axis = Quarter (from Date Mapping), Column = Sales, Line = Profit.
   - **Treemap**: Group = Continent, Values = Sales.
   - **Slicer**: Field = Financial Year (filters entire report).
   - **Bar Chart**: Axis = Category, Values = Sales (legend = Chain for breakdown).

5. **Interactivity**:
   - Slicer filters update all visuals (e.g., select FY 23-24 → Quarters Q1-Q4 appear).
   - Drill-down: Click continent → Shows country breakdown.

### Challenges Addressed
- **Continent-Wise Sales**: No direct column; used mapping table for lookup.
- **Financial Year/Quarter**: Derived from date mapping; no raw column.
- **Profit Calculation**: Added via Power Query (Sales - Cost).
- **Chain Breakdown**: Legend in charts for Readymade vs. Accessories.

### Sample Visuals Created
- High-level KPIs: Total Sales, Profit %.
- Continent/Quarter trends.
- Category treemap.

## Q&A and Common Questions
- **Multiple Excel Sheets**: Yes, connect multiple files/sheets as separate tables.
- **Permissions Issues**: Check tenant settings; use organizational account (not Gmail).
- **Mapping Tables**: Create in Excel/SQL; connect as dimensions. Update via IT for live data.
- **Certifications**: Covers 70%+ for PL-300 (Microsoft Power BI Data Analyst).
- **Finance/HR Dashboards**: Examples include receivables aging, employee turnover, invoice analysis.
- **Advanced Topics**: Next classes: Deep Power Query, DAX, modeling, publishing.

Follow up

References