# 🧪 Preclinical SAS Analysis: Body Weight Study (CDISC + ANCOVA)

This project demonstrates a **CDISC-compliant SAS clinical programming analysis** performed on preclinical (animal model) body weight data across seven treatment groups.  
It includes **SDTM and ADaM dataset creation, statistical testing (ANCOVA)**, and **final TLF output generation** — all written in base SAS.

---

## 📘 Project Overview

### 🎯 Objective
To analyze **body weight changes in 42 rats** across **7 treatment groups** to find the most effective drug combination in preventing weight loss in a disease model.

### 🧫 Study Design
| Parameter | Description |
|------------|-------------|
| Subjects   | 42 rats (6 per group) |
| Groups     | NC, DC, STD, HECLD, HECHD, STDHECLD, STDHECHD |
| Timepoints | Day 0 (Baseline) and Final |
| Endpoint   | Change in body weight (grams) from baseline |
| Analysis   | ANCOVA (Change ~ Baseline + Treatment Group) |

---

## 🧩 Data Flow / CDISC Workflow
Raw Data → SDTM.VS (Vital Signs) → ADaM.ADVS → TLFs (Tables, Listings, Figures)



---

## ⚙️ Technologies Used
- **SAS Studio / SAS 9.4**  
- **PROC MEANS**, **PROC REPORT**, **PROC GLM**, **PROC SGPLOT**  
- **CDISC SDTM / ADaM standards**  
- **Statistical Test**: ANCOVA adjusted for baseline

---

## 📊 Key Statistical Findings

| Treatment Group | Mean Change (g) | p-value (vs NC) | Interpretation |
|-----------------|-----------------|-----------------|----------------|
| DC              | -44.4 | <0.0001 | Maximum weight loss - Disease progression |
| HECHD           | -41.9 | <0.0001 | High dose effect |
| HECLD           | -38.1 | <0.0001 | Low dose effect |
| STD             | -41.1 | <0.0001 | Standard treatment |
| STDHECLD        | -32.8 | <0.0001 | Combined low dose |
| **STDHECHD**    | **-16.8** | **0.0108** | **Best combined treatment (effective)** |
| NC (Ref)        | -3.0 | — | Normal control |

✅ **Model Fit:** R² = 0.86  
✅ **Significance:** Treatment effect p < 0.0001

---

## 📂 Repository Structure
preclinical-sas-analysis/
├── README.md # Project overview (this file)
├── LICENSE # MIT open-source license
├── raw_data.csv # Input data (body weight per rat)
├── SAS_Program_Final.sas # Complete SAS code with SDTM + ADaM + ANCOVA
│
├── outputs/
│ └── SAS_Program_2-result.html # Full results and visualizations (open in browser)
│
└── docs/
├── project_report.md # Brief executive summary of analysis
└── data_dictionary.md # Variable definitions and metadata



---

## 🧮 Analysis Pipeline Highlights

1. **Raw dataset creation**
   - Input rat body weights at Day 0 and Final.
2. **SDTM.VS dataset**
   - Converts wide → long format following CDISC structure.
3. **ADaM.ADVS dataset**
   - Derives *BASE*, *CHG*, and *PCHG* (Change & Percent Change).
4. **Statistical Analysis**
   - PROC GLM performing ANCOVA (baseline adjusted).
5. **Reporting**
   - Summary tables, graphs, and data interpretation sections.

---

## 📈 Figures and Tables

- **Table 1:** Mean Body Weight by Treatment and Visit  
- **Table 2:** Change from Baseline (Final Visit)  
- **Figure 1:** Mean Body Weight per Group  
- **Figure 2:** Mean Change from Baseline (ANCOVA)  

👉 View here: [outputs/SAS_Program_2-result.html](outputs/SAS_Program_2-result.html)

---

## 🧬 Interpretation Summary

| Group | Observation |
|--------|--------------|
| **DC** | Severe weight loss (disease progression) |
| **STDHECHD** | Least weight loss; best treatment |
| **HECHD** | Strong high-dose drug effect |
| **NC** | Slight gain — healthy control stability |

---

## 👨‍💻 Author
**PRASHANTH.E**  
B.PHARMA ,MSC-BIOINFIRMATIC
prashantheprashanth584@gmail.com
  

---

## 📄 License
  [MIT License](./LICENSE).  


---

## 🧠 Summary
This project demonstrates **real-world clinical data handling** and **statistical analysis workflow** in SAS using **CDISC standards (SDTM + ADaM)** — a must-have for CRO, pharma, and bioinformatics roles.
