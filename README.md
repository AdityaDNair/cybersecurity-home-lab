# OpenVAS Vulnerability Assessment Lab

## Project Overview

This project demonstrates a hands-on vulnerability assessment performed using **OpenVAS (Greenbone Vulnerability Manager)** and **Nmap** within a virtual lab environment. The assessment targeted a deliberately vulnerable machine, **Metasploitable2**, to identify exposed services, outdated software, and critical security weaknesses.

The lab simulates a real-world vulnerability scanning workflow used by security analysts and penetration testers.


# Tools & Technologies

* OpenVAS / Greenbone Vulnerability Manager (GVM)
* Nmap
* Kali Linux
* Metasploitable2
* VirtualBox


# Lab Environment

| Component       | Purpose                     |
| --------------- | --------------------------- |
| Kali Linux      | Attacker / Scanning Machine |
| Metasploitable2 | Vulnerable Target Machine   |
| VirtualBox      | Virtualization Platform     |
| OpenVAS         | Vulnerability Scanner       |
| Nmap            | Service Enumeration         |


# Reconnaissance & Enumeration

Initial service discovery was performed using Nmap:
in bash : nmap -sV 192.168.56.103

## Open Ports & Services Identified

* FTP (vsftpd 2.3.4)
* SSH
* Telnet
* SMTP
* Samba
* MySQL
* PostgreSQL
* Apache Tomcat
* UnrealIRCd
* VNC
* NFS


# Vulnerability Assessment

An OpenVAS “Full and Fast” scan was conducted against the Metasploitable2 target.

## Critical Findings Identified

* vsftpd Backdoor Vulnerability
* Apache Tomcat Ghostcat Vulnerability
* MySQL Default Credentials
* TWiki Multiple XSS / Command Execution Vulnerabilities
* Ingreslock Backdoor Detection
* Outdated End-of-Life Operating System
* Passwordless Remote Login Services

#Scan Results Summary

| Severity | Count |
| -------- | ----- |
| Critical | 13    |
| High     | 9     |
| Medium   | 39    |
| Low      | 5     |
| Log      | 89    |

Maximum Severity Detected:

10.0 (Critical)


# Project Structure

OpenVAS-Vulnerability-Assessment-Lab/
│
├── README.md
├── reports/
│   └── openvas-report.pdf
│
├── screenshots/
│   ├── task-overview.png
│   ├── dashboard-summary.png
│   ├── results-overview.png
│   └── critical-vulnerability.png
│
└── notes/
    └── findings.md


# Screenshots

## Task Overview
Shows completed vulnerability assessment task and severity distribution.

![]()

## Results Overview
Displays detected vulnerabilities, CVSS scores, and affected services.

![]()

## Critical Vulnerability Details
Shows detailed analysis of a critical finding including:

* CVE references
* Impact
* Detection results
* Recommended remediation

![Critical-Vulnerability](https://github.com/AdityaDNair/cybersecurity-home-lab/blob/main/screenshots/critical-vulnerability.png?raw=true)

## Dashboard Summary
Visual representation of vulnerability severity statistics.

![Dashboard-Summary](https://github.com/AdityaDNair/cybersecurity-home-lab/blob/main/screenshots/dashboard-summary.png?raw=true)

# Key Skills Demonstrated

* Vulnerability Assessment
* Network Service Enumeration
* Security Scanning
* CVE Analysis
* Risk Severity Analysis
* Virtual Lab Deployment
* OpenVAS Configuration
* Nmap Enumeration

# Conclusion

This project demonstrates the process of identifying vulnerabilities within a controlled lab environment using industry-standard tools. The assessment revealed multiple critical security flaws commonly found in outdated or misconfigured systems, reinforcing the importance of continuous vulnerability management and system hardening.

# Disclaimer

This project was performed in an isolated virtual lab environment for educational and defensive security purposes only.
