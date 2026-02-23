# 🛡️ Wazuh SIEM Lab: Manager & Agents Deployment with Sysmon Installation

This repository documents a **Wazuh Security Information and Event Management (SIEM) lab**, built to simulate a corporate cybersecurity monitoring environment.  
It includes a **Wazuh Manager** deployment, multiple **agents** on Windows and Linux, and a complete logging, alerting, and dashboard setup.

---

## 📌 Lab Overview

- **Wazuh Manager** (central SIEM for log aggregation and alerting)  
- **Wazuh Agents** deployed on Windows and Linux endpoints  
- Real-time monitoring for system events, authentication, file integrity, and network activity  
- Dashboards for visualizing security alerts and trends  
- Safe environment for **Red Team / Blue Team exercises**  

---

## 🏗️ Lab Architecture
[Windows/Linux Agents] ---> [Wazuh Manager] ---> [Elasticsearch + Kibana] ---> [Dashboard]


- **Agents**: Collect logs and monitor endpoints  
- **Manager**: Aggregates logs, applies rules, triggers alerts  
- **Elasticsearch**: Stores event data  
- **Kibana**: Visualizes logs and alerts  

---

## ⚙️ Deployment Details

### Wazuh Manager
- OS: Ubuntu 22.04  
- Components: Wazuh Manager, Filebeat, Elasticsearch, Kibana  
- Installed via automated script (`install-wazuh-manager.sh`)  
- Handles log collection, alerting, and dashboard visualization
<img src='https://i.imgur.com/BVp8MFB.png' alt='Wazuh Manager'>

### Wazuh Agents
- OS: Windows 10 / Windows Server / Linux  
- Configured to connect to Wazuh Manager  
- Monitors system logs, security events, and network activity  
- Installed via automated script (`install-wazuh-agent.sh`)
<img src='https://i.imgur.com/zZrrsYo.png' alt='Wazuh Agent'>
<img src='https://i.imgur.com/qISQDmo.png' alt='Wazuh Agent'>


### Sysmon
- OS: Windows 10 
- Configured to connect to Wazuh Manager  
- Monitors system logs, security events, and network activity  
- Downloaded sysmon, sysmon conf xml file from SwiftOnSecurity

<img src='https://i.imgur.com/A1o177G.png' alt='sysmon xml file'>
<img src='https://i.imgur.com/c6FwBgM.png' alt='sysmon xml file'>

###Configuring to Forward Sysmon Logs to Wazuh Manager
- Configured the ossec.conf file in Windows 10 creating an event channel to forward the sysmon logs
- Restarted the wazuh agent
<img src='https://i.imgur.com/YZZCB2K.png' alt='ossec'>

---


## 🔐 Security Features Practiced

- Real-time endpoint monitoring and alerting  
- Custom rule creation for log analysis  
- Incident detection and investigation  
- Visualization of security metrics in dashboards  
- Centralized management of endpoints  

---

## 🚀 Future Enhancements

- Integrate with Active Directory lab for domain event monitoring  
- Forward alerts to Slack/Teams  
- Automate deployment with Ansible  
- Deploy IDS/IPS for proactive security  
- Correlate alerts with MITRE ATT&CK framework  

---

## 🛠️ Tools & Technologies

- **Wazuh Manager & Agents**  
- **Elasticsearch & Kibana**  
- **Windows 10 / Windows Server / Linux**  
- **Sysmon** (for Windows log monitoring)  
- **Filebeat** (log forwarding)  

---

## 🎯 Learning Objectives

- Implement and deploy a full SIEM solution  
- Monitor endpoints for security threats  
- Customize detection rules  
- Analyze logs and visualize alerts  
- Practice Red Team and Blue Team exercises in a safe lab  

