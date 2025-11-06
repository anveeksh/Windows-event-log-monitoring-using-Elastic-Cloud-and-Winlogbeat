# Elastic & Winlogbeat Centralized Logging Project  
Comprehensive SOC Logging & Monitoring Setup using Elastic Cloud

This repository contains a full documentation of setting up **Elastic Cloud**, configuring **Winlogbeat**, and creating a complete Windows logging pipeline suitable for **SOC operations**, **security monitoring**, and **incident detection**.  
The included PDF provides step-by-step screenshots and configuration details of the entire deployment process.

---

#  Project Overview

Modern Security Operations Centers (SOCs) rely heavily on centralized log monitoring to detect anomalies, security incidents, and operational issues.  
This project demonstrates the complete workflow of collecting Windows Event Logs using **Winlogbeat**, sending them to **Elastic Cloud**, and visualizing them in **Kibana**.

The goal of the assignment is to show:

- How Elastic Stack works as a cloud-based SIEM/log aggregator  
- How Windows logs can be shipped using Winlogbeat  
- How SOC analysts use dashboards and searches for investigation  
- How to build an end-to-end logging pipeline for security analysis  

---

#  Available Files

### **Elastic and Winlogbeat Assignment.pdf**  
A full assignment containing:

- Introduction to Elastic Cloud  
- Introduction to Winlogbeat  
- Complete installation steps  
- Configuration of winlogbeat.yml  
- Screenshots of setup  
- Discover and dashboard usage  
- Final conclusion  

This PDF acts as the primary project deliverable and training material.

---

#  What This Project Covers

## 1. Understanding Elastic Cloud
The PDF explains Elastic Cloud (cloud.elastic.co) which provides:

- Hosted **Elasticsearch**
- Hosted **Kibana**
- Log indexing & storage
- Visualization tools
- Dashboards & alerts
- Role-based access and secure endpoints

Elastic Cloud makes SIEM-style monitoring easy without the need for on-premise servers.

---

## 2. Introduction to Winlogbeat
Winlogbeat is a lightweight log shipper for Windows.  
It collects:

- System Logs  
- Application Logs  
- Security Logs  
- Windows Event Log Data  

The PDF shows how to:

- Install Winlogbeat  
- Configure log sources  
- Connect Winlogbeat to Elastic    
- Run the Beat as a Windows service  

---

## 3. Deployment Workflow

### **Step 1 — Create Elastic Deployment**
- Login at cloud.elastic.co  
- Create first deployment  
- Note down the Cloud ID & credentials

### **Step 2 — Install Winlogbeat on Windows**
- Download Winlogbeat  
- Extract and move to `C:\Program Files\Elastic\Winlogbeat`  
- Edit `winlogbeat.yml`  
- Configure cloud.auth & cloud.id  

### **Step 3 — Run Winlogbeat**
Commands used:

```powershell
.\winlogbeat test config
.\winlogbeat setup
Start-Service winlogbeat
```
### **Step 4 — Validate in Kibana**
nside Kibana:
-	Go to Discover
-	Select the winlogbeat-* index
- Validate incoming logs

Screenshots provided in the PDF.

## 4. Dashboard Creation
The project demonstrates how to build dashboards such as:
- Hostname distribution
- Event ID frequency
- Login activity overview
- Security alerts (failed logins, privilege changes)
- System warnings & errors

Visualizations used:
- Pie Charts
- Data Tables
- Time Series
- Filters & Queries

This replicates real SOC workflows.

# Key Learning Outcomes
By completing this assignment, you learn:

SOC Monitoring Fundamentals

Understanding how log pipelines work between endpoint → beat → cloud → SIEM.

Elastic Stack Skills
- Basic SIEM setup
- Log ingestion
- Index management
- Searching logs using KQL
- Dashboarding
- Real-time log monitoring

# Hands-on Winlogbeat Configuration

Editing YAML files, enabling modules, and starting the service.

# Event Log Interpretation

Reviewing Windows security and system events.

# Technologies Used

| Component | Purpose |
|----------|-------------|
| **Elastic Cloud** | Hosted Elasticsearch & Kiban |
| **Kibana** | Log analytics & dashboards |
| **Winlogbeat** | Windows log collection |
| **Windows OS** | Log source endpoint |
| **PowerShell** | Execution & validation |

# Testing & Validation

The following checks were performed:

Configuration Test

``` bash
.\winlogbeat test config
```

### Output Test

Ensuring Winlogbeat connects to Elastic Cloud.

### Data Ingestion Test

Verifying new log entries appear in Kibana in real-time.

### Dashboard Validation

Cross-checking visualization accuracy.

# SOC Use Cases Enabled
This pipeline supports:
- Monitoring login failures
- Detecting unauthorized access
- Tracking malware-like system behavior
- Observing system instability
- Investigating security alerts
- Watching administrative activities
- Baselining normal vs abnormal activity

# Project Architecture (Conceptual)
``` bash
Windows Machine  
     ↓  
Winlogbeat (Log Shipper)  
     ↓  
Elastic Cloud Endpoint  
     ↓  
Elasticsearch Index (winlogbeat-*)  
     ↓  
Kibana (Dashboards & Discover)
```

This is a typical enterprise log ingestion architecture.

 # Conclusion

 This project successfully demonstrates the complete setup of a log monitoring pipeline for Windows systems using Elastic Stack and Winlogbeat.

The implementation:
- Helps understand SIEM operations
- Trains SOC mindset
- Provides hands-on log ingestion experience
- Builds a foundation for threat detection
- Improves log analysis and investigation skills

The attached PDF serves as a detailed guide and can be used for training, academic submissions, or SOC practice.

# Author

## Anveeksh Mahesh Rao 
## Cybersecurity Engineer | SOC Analyst | Blue Team | Elastic Stack Learner

GitHub: https://github.com/anveeksh
LinkedIn: www.linkedin.com/in/anveekshmrao
 

