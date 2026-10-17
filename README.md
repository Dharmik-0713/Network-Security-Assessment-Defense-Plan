# Enterprise Network Security Assessment

**Role:** Cyber Security Intern  
**Target Environment:** Corporate Enterprise Network (Simulated)  

## 1. Project Overview
This repository contains a comprehensive Network Security Assessment conducted for a simulated medium-sized enterprise environment (50-100 employees). The objective of this project is to evaluate existing network architecture, identify potential security misconfigurations, analyze attack surfaces, and recommend robust defensive controls to protect corporate assets against external and internal threats.

## 2. Scope of Assessment
The assessment covers the critical components of the organization's network infrastructure:
* **Perimeter & Edge:** Internet-facing routers and the primary corporate firewall.
* **Demilitarized Zone (DMZ):** Public-facing web and email servers.
* **Internal Corporate LAN:** Employee workstations, internal active directory, and file servers.
* **Wireless Networks:** Corporate employee Wi-Fi and isolated Guest Wi-Fi.

## 3. Identified Threats & Risk Analysis
* **Exposed RDP (Port 3389):** High risk of brute-force attacks and ransomware deployment.
* **Unsegmented Guest Wi-Fi:** High risk of lateral movement into the corporate network by malicious actors or infected guest devices.
* **Weak Corporate Wi-Fi Security (WPA2-Personal):** Medium risk of credential sharing and perimeter compromise.
* **Lack of Internal Monitoring:** Medium risk of undetected insider threats and malware propagation.

## 4. Defense Strategy & Recommended Controls
Implemented a defense-in-depth strategy to harden the enterprise network architecture:
* **Firewall Hardening:** Explicitly denied inbound connections to internal management ports (RDP, SSH) and enforced VPN with Multi-Factor Authentication (MFA) for remote access.
* **Network Segmentation:** Enforced strict VLAN separation between Guest and Corporate networks with Access Control Lists (ACLs).
* **Intrusion Detection (IDS/IPS):** Recommended core switch port mirroring (SPAN) to monitor internal east-west traffic for anomalies.
* **Wireless Security Upgrade:** Deprecated Pre-Shared Keys in favor of WPA3-Enterprise linked to a RADIUS server for individual employee authentication.
