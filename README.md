# SOC & Network Security Laboratory

## 📌 Project Overview
This repository documents a fully functional, locally hosted **Security Operations Center (SOC)** and network security lab. Due to limited physical infrastructure, I engineered this virtual environment on my local machine to gain enterprise-grade experience in firewall configurations, log management, and active intrusion detection systems (IDS).

---

## 🛠️ Lab Architecture & Technologies
The lab simulates a secure corporate network environment using three core pillars:
*   **Firewall & Gateway:** OPNsense Virtual Appliance
*   **SIEM & Detection:** Wazuh (Security Information and Event Management)
*   **Target Endpoint:** Hardened Linux Deployment (Ubuntu/Kali)

### Network Topology
`[Internet] ──> [OPNsense Firewall] ──> [Internal LAN] ──> [Linux Endpoint + Wazuh Agent]`
*   All traffic leaving the Linux endpoint must route securely through the OPNsense gateway.
*   The Wazuh Agent monitoring the endpoint actively ships system logs to the central SIEM manager.

---

## 🔒 Implemented Security Capabilities

### 1. Network Segmentation & Firewall Rules (OPNsense)
I configured strict firewall policies within OPNsense to enforce the principle of least privilege.
*   Blocked all unauthorized inbound WAN traffic.
*   Configured port forwarding and basic network address translation (NAT).
*   *Add your screenshot here:* `![OPNsense Rules Dashboard](path/to/your/opnsense-screenshot.png)`

### 2. Log Aggregation & SIEM Monitoring (Wazuh)
I deployed a centralized Wazuh manager to monitor endpoint security metrics in real time.
*   **Authentication Tracking:** Monitored brute-force SSH attempts on the Linux machine.
*   **System Integrity Monitoring:** Enabled file integrity checking (FIM) to watch for unauthorized changes in critical Linux system files (`/etc/passwd`).
*   *Add your screenshot here:* `![Wazuh Security Alerts Dashboard](path/to/your/wazuh-screenshot.png)`

### 3. Vulnerability Management
Using Wazuh's vulnerability detection engine, I run routine audits against the Linux machine to identify missing software patches and common vulnerabilities and exposures (CVEs).
*   *Add your screenshot here:* `![Wazuh Vulnerability Scan Results](path/to/your/vulnerability-screenshot.png)`

---

## 🎯 Key Learning Outcomes
Through building this lab entirely from scratch, I mastered:
1. Managing traffic logs and detecting network anomalies.
2. Reading and triaging SIEM alerts to mitigate potential cyber threats.
3. Hardening Linux systems based on industry-standard security frameworks.
