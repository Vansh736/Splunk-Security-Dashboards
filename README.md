# Splunk Security Dashboards

This project demonstrates how to create security monitoring dashboards in **Splunk SIEM** to analyze system and network logs. The dashboards help identify suspicious activity such as SSH brute-force attacks and abnormal web traffic behavior.

The goal of this project is to practice **log analysis, detection queries, and security visualization using Splunk**.


## Project Overview

Security analysts rely on SIEM dashboards to monitor systems and detect attacks in real time.  
In this project, multiple dashboards were created using Splunk queries to analyze:

- SSH authentication logs
- Web traffic logs
- Failed login attempts
- Client and server errors
- Suspicious activity patterns

These dashboards help security teams quickly detect and investigate potential threats.



## Tools Used

- **Splunk Enterprise** – SIEM platform for log analysis and dashboards  
- **Linux Logs** – Authentication and system logs  
- **Web Traffic Logs** – HTTP access logs  
- **SPL (Search Processing Language)** – Query language used in Splunk  



## Dashboards Implemented

### 1️⃣ SSH Security Dashboard

This dashboard analyzes SSH authentication logs to detect suspicious login activity.

It includes visualizations for:

- Failed SSH login attempts
- Invalid user login attempts
- Successful SSH logins
- Attack frequency over time
- Targeted usernames

Queries used in this dashboard are available in:

- [SSH Dashboard Queries](ssh_dashboard_queries.md)

### SSH Security Dashboard

![SSH Dashboard](ssh_dashboard.png)


### 2️⃣ Web Traffic Monitoring Dashboard

This dashboard analyzes HTTP logs to monitor abnormal web activity.

It includes panels for:

- Web traffic logs
- Client errors (4xx)
- Server errors (5xx)
- Successful responses
- Traffic patterns

Queries used in this dashboard are available in:

- [Web Traffic Dashboard Queries](web_traffic_dashboard_queries.md)


### Web Traffic Dashboard

![Web Traffic Dashboard](web_traffic_dashboard.png)



## Key Learning Outcomes

- Understanding how SIEM dashboards work
- Writing SPL queries for security monitoring
- Detecting suspicious login activity
- Monitoring web traffic behavior
- Visualizing security events in dashboards

---

## Author

Vansh Tiwari  
Cybersecurity Student | SOC Analyst Learner
