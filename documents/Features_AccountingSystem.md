# Accounting System - Product Backlog & Features Document

[cite_start]**Institución:** UNIVERSIDAD DE LAS FUERZAS ARMADAS ESPE [cite: 2, 3]
[cite_start]**Departamento:** Computer Science - Software Engineering [cite: 4]
[cite_start]**Materia:** ADVANCED WEB DEVELOPMENT [cite: 5]
[cite_start]**Integrantes:** Esteban Quiroga, Angel Sabando, David Rodriguez [cite: 6]
[cite_start]**NRC:** 30716 [cite: 7]
[cite_start]**Fecha:** May 13, 2026 [cite: 8]

---

## 1. Features Summary Table

| ID | Feature Name | Primary Module | Sprint(s) | Lead(s) | Effort |
| :--- | :--- | :--- | :--- | :--- | :--- |
| FT-01 | User Identity & Secure Access | Mod 1 | 1 | D.R / E.Q | 7 hrs |
| FT-02 | Workspace & Project Isolation | Mod 1 | 1 | A.S | 7 hrs |
| FT-03 | SRI Service Handshake | Mod 2 | 2-3 | E.Q | 7 hrs |
| FT-04 | Automated Invoice Retrieval | Mod 3 | 4 | E.Q | 4 hrs |
| FT-05 | Fiscal Data Timeline Filtering | Mod 3 | 5 | D.R | 4 hrs |
| FT-06 | Local Import & Ownership Integrity | Mod 3 | 5-6 | A.S / D.R | 6 hrs |
| FT-07 | ATS XLSM Generation Engine | Mod 4 | 7-8 | E.Q / A.S | 12 hrs |
| FT-08 | XLSM Structural Diagnostics | Mod 5 | 9 | E.Q / A.S | 7 hrs |
| FT-09 | Official XML Encoding (DIMM SRI) | Mod 6 | 10-11 | E.Q / A.S / D.R | 14 hrs |
| FT-10 | Workflow Traceability Dashboard | Mod 7 | 12 | E.Q / A.S | 14 hrs |

[cite_start][cite: 13, 17]

---

## 2. Feature Details & Specification

### FT-01 - User Identity & Secure Access
* [cite_start]**Description:** Handles taxpayer registration, login, and data protection via encrypted sessions[cite: 23].
* [cite_start]**Objective:** Secure the system and ensure data belongs to the authenticated RUC[cite: 23].
* [cite_start]**Module:** Module 1 Configuration & Setup[cite: 23].
* [cite_start]**Associated RFs:** RF-01[cite: 23].
* [cite_start]**Business Rules:** RN-02 (Ownership validation)[cite: 23].

**User Story:**
* [cite_start]**US-01:** As a user, I want to register and log in to protect my information (High Priority)[cite: 29].

**Technical Tasks:**
| Task ID | Task | Responsible | Sprint | Hrs |
| :--- | :--- | :--- | :--- | :--- |
| T-01-01 | Implement registration and login interface | David Rodriguez | Sprint 1 | 5 |
| T-01-03 | Apply data protection for saved documents | Esteban Quiroga | Sprint 1 | 2 |
[cite_start][cite: 31]

---

### FT-02 - Workspace & Project Isolation
* [cite_start]**Description:** Creation of isolated local directories based on specific taxpayer RUCs and tax years[cite: 32].
* [cite_start]**Objective:** Prevent cross-contamination between different fiscal periods[cite: 32].
* [cite_start]**Module:** Module 1 Configuration & Setup[cite: 37].
* [cite_start]**Associated RFs:** RF-02, RF-03[cite: 37].
* [cite_start]**Business Rules:** RN-01 (Tax periods)[cite: 37].

**Technical Tasks:**
| Task ID | Task | Responsible | Sprint | Hrs |
| :--- | :--- | :--- | :--- | :--- |
| T-01-04 | Implement directory creation and file path mapping | Angel Sabando | Sprint 1 | 7 |
[cite_start][cite: 38]

---

### FT-03 - SRI Service Handshake
* [cite_start]**Description:** Secure connection and authentication with the SRI online portal[cite: 40].
* [cite_start]**Objective:** Establish a functional link to the external government database[cite: 49].
* [cite_start]**Module:** Module 2 - SRI Connectivity[cite: 51].
* [cite_start]**Responsible:** Esteban Quiroga[cite: 53].

**Technical Tasks:**
| Task ID | Task | Responsible | Sprint | Hrs |
| :--- | :--- | :--- | :--- | :--- |
| T-02-01 | Connect the system with the SRI portal | Esteban Quiroga | Sprint 2 | 7 |
[cite_start][cite: 50]

---

### FT-04 - Automated Invoice Retrieval
* [cite_start]**Description:** Automated download of electronic invoices (XML/PDF) directly from SRI[cite: 55].
* [cite_start]**Objective:** Eliminate manual document gathering[cite: 61].
* [cite_start]**Module:** Module 3 - Data Acquisition[cite: 63].
* [cite_start]**Associated RFs:** RF-03[cite: 67].

**Technical Tasks:**
| Task ID | Task | Responsible | Sprint | Hrs |
| :--- | :--- | :--- | :--- | :--- |
| T-03-01 | Automate the download of invoices from the portal | Esteban Quiroga | Sprint 4 | 4 |
[cite_start][cite: 66]

---

### FT-05 - Fiscal Data Timeline Filtering
* [cite_start]**Description:** Filter logic to ensure invoices match the monthly or semiannual reporting range[cite: 71].
* [cite_start]**Objective:** Exclude invoices outside the selected fiscal period[cite: 80].
* [cite_start]**Module:** Module 3 - Data Acquisition[cite: 82].
* [cite_start]**Business Rules:** RN-01[cite: 85].

**Technical Tasks:**
| Task ID | Task | Responsible | Sprint | Hrs |
| :--- | :--- | :--- | :--- | :--- |
| T-03-03 | Develop temporal filter based on XML "fechaEmision" tags | David Rodriguez | Sprint 5 | 4 |
[cite_start][cite: 81]

---

### FT-06 - Local Import & Ownership Integrity
* [cite_start]**Description:** Manual import of external XMLs with RUC validation[cite: 97].
* [cite_start]**Objective:** Allow inclusion of local files while maintaining identity integrity[cite: 98, 99].
* [cite_start]**Module:** Module 3 - Data Acquisition[cite: 100].
* [cite_start]**Business Rules:** RN-02[cite: 106].

**Technical Tasks:**
| Task ID | Task | Responsible | Sprint | Hrs |
| :--- | :--- | :--- | :--- | :--- |
| T-03-02 | Implement manual upload and RUC validation | Angel Sabando | Sprint 6 | 4 |
[cite_start][cite: 105]

---

### FT-07 - ATS XLSM Generation Engine
* [cite_start]**Description:** Mapping of invoice data into a standardized XLSM spreadsheet[cite: 114, 115].
* [cite_start]**Objective:** Transform raw XML data into an editable accounting format[cite: 116, 117].
* [cite_start]**Module:** Module 4 - Core Transcription[cite: 120].

**Technical Tasks:**
| Task ID | Task | Responsible | Sprint | Hrs |
| :--- | :--- | :--- | :--- | :--- |
| T-04-01 | Implement Excel transcription logic | Esteban Quiroga | Sprint 7 | 6 |
| T-04-02 | Map XML tags to XLSM headers | Angel Sabando | Sprint 8 | 8 |
[cite_start][cite: 125, 129]

---

### FT-08 - XLSM Structural Diagnostics
* [cite_start]**Description:** Scanning the generated XLSM for errors before XML export[cite: 130].
* [cite_start]**Objective:** Reduce final export failures[cite: 130].
* [cite_start]**Module:** Module 5 - Validation[cite: 130].

**Technical Tasks:**
| Task ID | Task | Responsible | Sprint | Hrs |
| :--- | :--- | :--- | :--- | :--- |
| T-05-01 | Develop XLSM file validation | Esteban Quiroga | Sprint 9 | 5 |
| T-05-02 | Design log system for error notifications | Angel Sabando | Sprint 9 | 2 |
[cite_start][cite: 137]

---

### FT-09 - Official XML Encoding (DIMM SRI)
* [cite_start]**Description:** Conversion of XLSM data into SRI-compliant XML (DIMM format)[cite: 138].
* [cite_start]**Objective:** Generate the official legal file for submission[cite: 138].
* [cite_start]**Module:** Module 6 - XML Generation[cite: 138].

**Technical Tasks:**
| Task ID | Task | Responsible | Sprint | Hrs |
| :--- | :--- | :--- | :--- | :--- |
| T-06-01 | Develop XML creation from validated XLSM | Esteban Quiroga | Sprint 10 | 5 |
| T-06-02 | Validate against SRI DIMM schema | Angel Sabando | Sprint 11 | 5 |
| T-06-03 | Implement secure XML file download | David Rodriguez | Sprint 11 | 4 |
[cite_start][cite: 143]

---

### FT-10 - Workflow Traceability Dashboard
* [cite_start]**Description:** Visual status tracking of the entire ATS generation process[cite: 145].
* [cite_start]**Objective:** Provide real-time monitoring of the workflow stages[cite: 152, 156].
* [cite_start]**Module:** Module 7 - Traceability[cite: 158].

**Technical Tasks:**
| Task ID | Task | Responsible | Sprint | Hrs |
| :--- | :--- | :--- | :--- | :--- |
| T-07-01 | Create status widget (completed/pending/blocked) | Esteban Quiroga | Sprint 12 | 7 |
| T-07-02 | Connect widget to all modules for updates | Angel Sabando | Sprint 12 | 7 |
[cite_start][cite: 157]

---

## 3. Effort Distribution Summary

| Team Member | Assigned Tasks | Estimated Total |
| :--- | :--- | :--- |
| **Esteban Quiroga** | T-01-03, T-02-01, T-03-01, T-04-01, T-05-01, T-06-01, T-07-01 | 36 hrs |
| **Angel Sabando** | T-01-04, T-03-02, T-04-02, T-05-02, T-06-02, T-07-02 | 34 hrs |
| **David Rodriguez** | T-01-01, T-01-02, T-03-03, T-06-03 | 30 hrs |
| **Total Project** | **Full Backlog Implementation** | **100 hrs** |
[cite_start][cite: 166]