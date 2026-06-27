# Wazuh SIEM Deployment Lab

A cybersecurity home lab demonstrating Wazuh SIEM deployment, endpoint agent configuration, Sysmon log collection, and security monitoring workflows.

## Project Summary

This project documents the deployment of a Wazuh-based SIEM lab designed to simulate a small corporate monitoring environment. The lab includes a Wazuh manager, endpoint agents, Windows Sysmon telemetry, log forwarding, and dashboard-based alert review.

The goal is to practise blue-team fundamentals: endpoint visibility, log collection, alerting, and basic detection engineering.

## Skills Demonstrated

- Wazuh manager deployment
- Wazuh agent installation and enrollment
- Windows endpoint monitoring
- Linux endpoint monitoring
- Sysmon installation and configuration
- Security log forwarding
- SIEM dashboard review
- Alert analysis and documentation
- Lab-based blue-team practice

## Lab Architecture

```text
Windows Endpoint   Linux Endpoint
      |                 |
      v                 v
  Wazuh Agents ---> Wazuh Manager ---> Dashboard / Alert Review
```

## Tools and Technologies

| Area | Tools |
|---|---|
| SIEM | Wazuh Manager and Wazuh Agents |
| Endpoint telemetry | Sysmon |
| Operating systems | Ubuntu, Windows 10, Windows Server, Linux endpoints |
| Log forwarding | Wazuh agent configuration |
| Visualisation | Wazuh dashboard stack |

## Deployment Walkthrough

### 1. Wazuh Manager Deployment

The Wazuh manager was deployed as the central system for log collection, rule processing, and alert generation.

<img src="https://i.imgur.com/BVp8MFB.png" alt="Wazuh Manager">

### 2. Wazuh Agent Deployment

Agents were installed on endpoint systems so logs and security events could be sent to the Wazuh manager.

<img src="https://i.imgur.com/zZrrsYo.png" alt="Wazuh Agent">

<img src="https://i.imgur.com/qISQDmo.png" alt="Wazuh Agent">

### 3. Sysmon Installation

Sysmon was installed on the Windows endpoint to improve process and event visibility.

<img src="https://i.imgur.com/A1o177G.png" alt="Sysmon configuration">

<img src="https://i.imgur.com/c6FwBgM.png" alt="Sysmon configuration">

### 4. Forward Sysmon Logs to Wazuh

The endpoint configuration was updated so Sysmon event logs could be forwarded to the Wazuh manager for monitoring and analysis.

<img src="https://i.imgur.com/YZZCB2K.png" alt="Wazuh log forwarding configuration">

## Security Concepts Practised

- Centralised log collection
- Endpoint visibility
- Event correlation basics
- Alert review
- Windows telemetry collection
- SIEM deployment fundamentals
- Blue-team lab documentation

## Key Takeaways

- SIEM tools are only useful when endpoints are properly configured to send useful logs.
- Sysmon improves Windows visibility beyond default event logs.
- Agent deployment and log forwarding are foundational SOC skills.
- Documentation helps explain security lab work clearly to recruiters.

## Future Improvements

- Integrate with the Active Directory lab for domain event monitoring.
- Add MITRE ATT&CK mapping for selected alerts.
- Add example alerts with investigation notes.
- Add a detection rule tuning section.
- Add screenshots showing dashboard alerts and event timelines.
