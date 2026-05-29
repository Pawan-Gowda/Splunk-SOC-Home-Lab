# Splunk-SOC-Home-Lab

## Overview
Built a Security Operations Center (SOC) home lab using Splunk Enterprise on Ubuntu Linux to detect and monitor brute force attacks in real time.

## Tools & Technologies
- Splunk Enterprise (SIEM)
- Ubuntu 24.04 LTS (Virtual Machine)
- SSH, Linux auth logs
- SPL (Splunk Search Processing Language)

## What I Built
- Deployed Splunk Enterprise on a Linux VM and configured live log ingestion from system authentication logs
- Simulated brute force SSH login attacks and wrote SPL queries to detect failed login attempts
- Built a SOC dashboard with visualizations tracking failed logins over time
- Created an automated alert that triggers when failed login attempts exceed a defined threshold

## Skills Demonstrated
- SIEM configuration and log management
- Threat detection and alert creation
- Linux system administration
- Incident investigation and log analysis

## Screenshots
<img width="832" height="607" alt="Failed Login Attempts" src="https://github.com/user-attachments/assets/a7e6fc06-7e64-4725-8665-308ad9d83512" />
<img width="1206" height="665" alt="Attempt Logs" src="https://github.com/user-attachments/assets/6a50e931-3c10-4482-af52-f73e28ed935a" />
<img width="1214" height="528" alt="Login Alerts" src="https://github.com/user-attachments/assets/ef893903-b2fa-45b6-a2a7-30aeedd8bbb1" />

