# Cloud-Based Honeypot Using Azure Sentinel

This repository documents a cybersecurity project that demonstrates the deployment and monitoring of a cloud-based honeypot using Microsoft Azure and Sentinel. The goal of the project was to simulate and detect brute-force login attempts, analyze attacker behavior, and visualize the data using SIEM tools.

## Project Summary

A Windows Virtual Machine (VM) was deployed on Microsoft Azure with exposed Remote Desktop Protocol (RDP) ports to attract unauthorized access attempts. Logs generated from failed login attempts were collected using Azure Log Analytics and analyzed within Microsoft Sentinel.

## Tools and Technologies Used

- Microsoft Azure (Virtual Machines)
- Microsoft Sentinel (Security Information and Event Management)
- Log Analytics Workspace
- Kusto Query Language (KQL)
- Sentinel Watchlists (for IP enrichment)
- Sentinel Workbooks (for dashboarding and visualization)

## Objectives

- Deploy a cloud-hosted VM to act as a honeypot
- Simulate failed login attempts (Event ID 4625)
- Forward security logs to Azure Log Analytics
- Query and analyze events using KQL
- Enrich logs using a custom geo-IP watchlist
- Visualize attacker activity using Sentinel Workbooks

## Implementation Steps

1. Deployed a Windows VM on Azure with open RDP ports
2. Enabled diagnostic settings to send logs to Log Analytics
3. Connected Microsoft Sentinel to the workspace
4. Simulated RDP brute-force attempts to generate Event ID 4625
5. Created custom KQL queries to analyze login patterns
6. Developed a geo-IP watchlist to enrich log data
7. Built a Sentinel Workbook to visualize attack origins

## Screenshots

Visual references and screenshots can be found in the [`/Screenshots`](./Screenshots) directory. These include:

- [Setting Up Windows Virtual Machine on Azure with Public RDP Access](./Screenshots/4.png)
- [Adding Inbound Security Rule to Allow All Traffic in Network Security Group (NSG)](./Screenshots/6.png)
- [Importing Geo-IP Data as a Sentinel Watchlist for Enrichment](./Screenshots/31.png)
- [Connecting VM to Sentinel via Windows Security Events (AMA) Connector](./Screenshots/15.png)
- [KQL log query outputs](./Screenshots/29.png)
- [Geo-IP visualizations](./Screenshots/44.png)

## Future Enhancements

- Automate honeypot deployment using ARM templates or Terraform
- Add reverse shell or malware drop simulations
- Integrate third-party threat intelligence feeds
- Set up email or Teams-based alerting for critical events

## License

This project is licensed under the [MIT License](./LICENSE).
