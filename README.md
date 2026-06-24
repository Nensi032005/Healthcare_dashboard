# 🏥 Healthcare Dashboard – Vitality Health Life

An interactive **Healthcare Analytics Dashboard** built with **Microsoft Excel** and **Power BI** to track patient flow, bed occupancy, billing, insurance and doctor workload for *Vitality Health Life – Work and Leads Workflow*.

> File: `Healthcare_dashboard.pbix`

---

## 📌 Project Overview

This project transforms raw hospital patient records (maintained in Excel) into a single-page, executive-style Power BI dashboard. It helps hospital management, doctors and operations teams quickly answer questions like:

- How many patients are currently admitted / discharged / on follow-up?
- What is the bed occupancy status across the hospital?
- Which diagnoses are most frequent?
- How much revenue is being generated vs. how much is covered by health insurance?
- Which doctors are handling the most cases?
- How are admissions trending over time?

---

## 🎯 Objectives

1. Centralize patient data from Excel into a clean data model.
2. Provide **real-time KPIs** for patients, doctors, bed occupancy and revenue.
3. Visualize trends in admissions, diagnoses and billing.
4. Enable slicing/filtering by **Patient ID** and **Admit Date** for case-level drilldown.

---

## 🗃️ Dataset

The dashboard is powered by a single fact table **`Sheet1`** loaded from Excel, with the following fields:

| Column | Description |
|--------|-------------|
| `Patient_ID` | Unique identifier for each patient |
| `Doctor` | Attending doctor's name |
| `Diagnosis` | Patient diagnosis / condition |
| `Bed_Occupancy` | Bed/ward occupancy status |
| `Admit_Date` | Date of admission |
| `Discharge_Date` | Date of discharge |
| `Followup Date` | Scheduled follow-up date |
| `Billing Amount` | Total amount billed to the patient |
| `Health Insurance Amount` | Amount covered by insurance |

---


## 📊 Dashboard Features

The report contains **one interactive page** with the following visuals:

### 🔢 KPI Cards
- **Total Patients** – `COUNT(Patient_ID)`
- **Total Doctors** – `DISTINCTCOUNT(Doctor)`
- **Total Diagnoses** – `COUNT(Diagnosis)`
- **Bed Occupancy Count** – `COUNT(Bed_Occupancy)`

### 📅 Date KPIs
- Earliest **Admit Date**
- Earliest **Discharge Date**
- Earliest **Follow-Up Date**

### 💰 Financial Visuals
- **Billing Amount** – total revenue (Sum)
- **Health Insurance Amount** – insurance coverage (Sum)
- Comparison between billing and insurance reimbursement

### 📈 Charts
| Visual | Insight |
|--------|---------|
| **Column Chart** | Patient distribution by category (e.g., diagnosis / doctor) |
| **Donut Chart** | Share of bed occupancy / diagnosis split |
| **Funnel Chart** | Patient workflow: Admitted → Discharged → Follow-up |
| **Line Chart** | Trend of admissions / billing over time |

### 🎚️ Slicers
- **Patient ID** slicer for case-level filtering
- **Admit Date** slicer for time-period filtering
