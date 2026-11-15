# 📊 Project Management Performance & Risk Analytics Dashboard

An interactive Power BI dashboard designed to analyze project performance, financial indicators, resource utilization, project risks, and governance metrics using a dataset of 4,000 projects.

The project combines **Power BI, Power Query, DAX, Python, and AI integration** to transform raw project data into meaningful business insights.

---

## 🎯 Project Objectives

- Analyze overall project risk distribution.
- Identify projects classified as High and Critical risk.
- Monitor project budgets and estimated budget utilization.
- Analyze resource availability and vendor reliability.
- Understand the relationship between governance indicators and project risk.
- Generate AI-assisted management observations and recommendations.

---

## 🛠️ Technology Stack

| Technology | Purpose |
|---|---|
| Power BI Desktop | Interactive dashboard development |
| Power Query | Data cleaning and transformation |
| DAX | Measures, calculations and KPIs |
| Microsoft Excel | Data preparation and validation |
| Python | Exploratory data analysis |
| Pandas & NumPy | Data manipulation and numerical analysis |
| Google Colab | Python development environment |
| Google Gemini API | AI-generated project insights (integration in progress) |
| Git & GitHub | Version control and project hosting |

---

## 📂 Dataset Overview

- Total Records: 4,000
- Total Columns: 51
- Unique Project IDs: 4,000
- Data Format: CSV
- Source: Kaggle project-risk dataset

### Important Dataset Attributes

**Project Information**
- Project_ID
- Project_Type
- Project_Phase
- Project_Budget_USD
- Estimated_Timeline_Months
- Team_Size

**Risk Information**
- Risk_Level
- Complexity_Score
- Historical_Risk_Incidents
- Requirement_Stability
- Schedule_Pressure

**Financial Information**
- Project_Budget_USD
- Budget_Utilization_Rate
- Funding_Source

**Resource Information**
- Resource_Availability
- Resource_Contention_Level
- Vendor_Reliability_Score
- Team_Size

**Governance Information**
- Risk_Management_Maturity
- Change_Control_Maturity
- Documentation_Quality
- Org_Process_Maturity
- Regulatory_Compliance_Level

---

## 📈 Power BI Dashboard Pages

### 1. Executive Risk Overview

Provides a high-level overview of project risk and performance.

Key KPIs:
- Total Projects
- High Risk Projects
- Critical Risk Projects
- High & Critical Risk Percentage
- Average Budget Utilization

Visualizations:
- Project Risk Distribution
- Risk by Project Type
- Interactive project filters

### 2. Project Risk Analysis

Analyzes how project characteristics relate to risk classifications.

Visualizations:
- Risk by Methodology
- Risk by Project Type
- Risk by Complexity
- Risk by Team Experience
- Risk by Stakeholder Engagement

### 3. Financial & Resource Analysis

Focuses on project budgets and resource indicators.

Key KPIs:
- Total Project Budget
- Average Project Budget
- Average Budget Utilization
- Estimated Budget Utilized
- Estimated Budget Overrun

Visualizations:
- Budget by Project Type
- Budget Utilization by Risk Level
- Resource Availability by Risk Level
- Team Size by Risk Level
- Vendor Reliability by Risk Level

### 4. Governance & AI Insights

Examines project governance indicators and their association with risk.

Key KPIs:
- High & Critical Risk Percentage
- Average Delivery Success Rate
- Average Historical Risk Incidents
- Total Projects

Visualizations:
- Risk by Organizational Process Maturity
- Risk by Documentation Quality
- Risk by Risk Management Maturity
- Risk by Change Control Maturity

AI integration is planned to generate:
- Executive Summaries
- Major Risk Observations
- Financial Observations
- Governance Observations
- Recommended Management Actions

---

## 🧮 DAX Measures

The project uses DAX measures for dynamic calculations and KPI reporting.

Examples:

**Total Projects**
```dax
Total Projects =
DISTINCTCOUNT(
    'project_risk_raw_dataset'[Project_ID]
)
```

**High Critical Risk Percentage**
```dax
High Critical Risk % =
DIVIDE(
    [High and Critical Projects],
    [Total Projects],
    0
)
```

**Estimated Budget Utilized**
```dax
Estimated Budget Utilized =
SUMX(
    'project_risk_raw_dataset',
    'project_risk_raw_dataset'[Project_Budget_USD]
    *
    'project_risk_raw_dataset'[Budget_Utilization_Rate]
)
```

---

## 🤖 AI Integration Architecture

The planned AI workflow uses Python and Google Gemini API.

```text
Project Risk Dataset (CSV)
          |
          v
Python + Pandas
          |
          v
Exploratory Data Analysis
          |
          v
Project Statistics (JSON)
          |
          v
Google Gemini API
          |
          v
AI-Generated Management Insights
          |
          v
CSV Output
          |
          v
Power BI Dashboard
```

AI-generated insights are intended to help management interpret project statistics and identify areas requiring attention.

---

## 📁 Project Structure

```text
Project-Management-Analytics-Dashboard/
│
├── PowerBI/
│   ├── Project_Management_Dashboard.pbip
│   ├── Project_Management_Dashboard.Report/
│   └── Project_Management_Dashboard.SemanticModel/
│
├── Dataset/
│   └── project_risk_raw_dataset.csv
│
├── Python-AI/
│   └── AI_Project_Risk_Analyst.ipynb
│
├── AI_Insights/
│   └── AI_Project_Risk_Insights.csv
│
├── Screenshots/
│   ├── Executive_Overview.png
│   ├── Project_Risk_Analysis.png
│   ├── Financial_Analysis.png
│   └── Governance_AI_Insights.png
│
└── README.md
```

*Folder contents may vary depending on the current implementation.*

---

## 🚀 How to Run the Project

### Power BI

1. Clone or download this repository.
2. Open the `.pbip` file using Power BI Desktop.
3. Update the dataset file location if necessary.
4. Refresh the data.
5. Explore the four dashboard pages.

### Python and AI Integration

1. Open the Jupyter Notebook in Google Colab.
2. Upload the project dataset.
3. Configure the Gemini API key securely using Colab Secrets.
4. Install the required Python libraries.
5. Execute the notebook cells.
6. Generate the AI insights CSV.
7. Import the generated CSV into Power BI.

---

## 📌 Key Business Observations

Based on the dataset:

- 4,000 unique projects are included.
- 44.95% of projects are classified as High or Critical risk.
- Average budget utilization is approximately 94.57%.
- Average project budget is approximately $1.143 million.
- Governance and documentation categories can be compared against project risk classifications.

---

## ⚠️ Project Limitations

- Budget utilization is an estimated metric based on project budget multiplied by the utilization ratio; it is not actual expense transaction data.
- Risk comparisons represent observed associations, not proven causal relationships.
- The dataset does not provide a validated project-failure prediction target or model.
- AI recommendations are decision-support suggestions and require human review.
- Missing dataset values are treated separately rather than automatically interpreted as poor performance.

---

## 🎓 Learning Outcomes

Through this project, I developed practical skills in:

- Data cleaning and transformation using Power Query.
- Writing DAX measures and calculated metrics.
- Building interactive multi-page Power BI dashboards.
- Exploratory Data Analysis using Python.
- Working with CSV and JSON data.
- Integrating an external generative AI API.
- Version control and GitHub project management.

---

## 👨‍💻 Author

**Sumedh**

GitHub: [123sumedh](https://github.com/123sumedh)

---

*Developed as a Data Analytics portfolio project using Power BI, Python and AI technologies.*
