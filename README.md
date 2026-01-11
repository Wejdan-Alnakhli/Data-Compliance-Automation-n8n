#  Automated Data Compliance & Governance Monitor

##  Project Overview
This project demonstrates an end-to-end automated system for monitoring organizational data compliance. It identifies policy violations based on **NDMO** and **PDPL** standards within a PostgreSQL database and triggers automated, professional email notifications to the concerned personnel.

##  Tech Stack & Skills
* **Database Management**: PostgreSQL (hosting HR and governance records).
* **Data Retrieval**: SQL ( CASE statements and Views).
* **Automation**: n8n (designing  data workflows).
* **Communication**: SMTP/Gmail (automated corporate notifications).
* **Compliance Standards**: NDMO (National ID validation) and PDPL (Privacy notice tracking).

##  Key Features
* **Compliance Logic**: A custom SQL View (`v_compliance_alerts`) was built to automatically flag invalid IDs (NDMO) and missing privacy signatures (PDPL).
* **Automated Workflow**: An n8n pipeline that fetches "Pending" alerts and processes them into individual reports.
* **Dynamic Reporting**: Send email  for each employee based on their specific violation.

##  Visual Proof

### 1. Database Compliance Status
<img width="701" height="427" alt="final result2" src="https://github.com/user-attachments/assets/92383314-71c8-4bb3-8456-76f6c7ac3825" />

*Monitoring data quality and compliance flags directly from the PostgreSQL database.*

### 2. Workflow Automation Design
<img width="926" height="401" alt="workflow_automation_design png" src="https://github.com/user-attachments/assets/547b1f70-342c-4a99-b9e4-ffd3970bbba5" />

*The automated pipeline architecture in n8n connecting data sources to communication channels.*

### 3. Email Notification Logs
<img width="773" height="117" alt="email_notification_logs png" src="https://github.com/user-attachments/assets/48d71c65-dbae-42f9-b8ed-eac16f06f426" />

*Evidence of successful automated delivery for multiple compliance alerts.*

### 4. Professional Compliance Alert Sample

<img width="732" height="287" alt="compliance_alert_sample png" src="https://github.com/user-attachments/assets/998eeddb-5966-4fb9-85df-0563c2b87b55" />

*The final high-fidelity notification received by the employee, formatted with HTML/CSS.*

##  How to Use
1. Import the `compliance_logic_view.sql` into your PostgreSQL instance.
2. Import `n8n_compliance_workflow.json` into your n8n environment.
3. Configure your SMTP credentials in n8n and execute.
