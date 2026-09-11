Week 2 – Vulnerability Assessment Lab
Overview

This project documents a controlled vulnerability assessment performed as part of a cybersecurity lab.

The objective of this task was to build on the reconnaissance skills developed during Week 1 by performing structured vulnerability scanning against a deliberately vulnerable lab target, analyzing the results, ranking identified vulnerabilities by risk, and preparing a professional findings report.

The assessment was conducted in an isolated lab environment using Kali Linux and a vulnerable target VM such as Metasploitable2.

Disclaimer: All scanning and testing documented in this repository was performed against systems within an authorized lab environment. The techniques and tools should only be used against systems for which you have explicit permission to test.

Objectives

The main objectives of this assessment were to:

Configure and verify a vulnerability scanning tool.
Confirm connectivity between the Kali Linux attacker VM and the target VM.
Perform a vulnerability scan against the authorized target.
Save the raw scanner output.
Identify at least five distinct vulnerabilities.
Determine the severity and affected service/port for each vulnerability.
Identify CVE references where available.
Rank vulnerabilities according to risk.
Provide practical remediation recommendations.
Produce a professional vulnerability findings report.
Lab Environment
Component	Details
Attacker VM	Kali Linux
Target VM	Metasploitable2 / authorized vulnerable VM
Scanner	Nikto
Network Analysis	Nmap / Wireshark
Scan Type	Vulnerability assessment
Environment	Isolated cybersecurity lab
Tools Used
Kali Linux

Kali Linux was used as the attacker/security assessment platform.

Nikto

Nikto was used as the vulnerability scanner for identifying common web server vulnerabilities, insecure configurations, and potentially dangerous files or server components.

Nmap

Nmap was used during reconnaissance to identify reachable hosts, open ports, and services on the target.

Wireshark

Wireshark was used during the lab to observe and analyze network traffic.

Metasploitable2

Metasploitable2 was used as the intentionally vulnerable target system for the assessment.

Methodology

The assessment followed a basic vulnerability-assessment workflow:

Lab Setup
   ↓
Target Connectivity Verification
   ↓
Reconnaissance
   ↓
Service Identification
   ↓
Vulnerability Scanning
   ↓
Result Collection
   ↓
Vulnerability Analysis
   ↓
Risk Ranking
   ↓
Remediation Recommendations
   ↓
Final Findings Report

1. Scanner Verification

The scanner installation was first verified from Kali Linux.

Example:

nikto -Version


Nikto help/options were also reviewed:

nikto -h

2. Target Connectivity

Before scanning, connectivity between Kali Linux and the authorized target VM was verified.

Example:

ping <TARGET-IP>


The target's available services could also be reviewed using Nmap:

nmap -sV <TARGET-IP>


Only the authorized lab target was scanned.

3. Vulnerability Scan

Nikto was executed against the authorized web service.

Example:

nikto -h http://<TARGET-IP>


The raw output was saved for later analysis.

Example:

nikto -h http://<TARGET-IP> -o nikto-report.html -Format htm

Scan Results

The scan results were reviewed to identify security weaknesses affecting the target.

At least five distinct vulnerabilities/findings were selected for detailed analysis.

#	Vulnerability / Finding	Severity	Service / Port	CVE
1	Finding 1	Critical/High	TCP/PORT	CVE-XXXX-XXXX
2	Finding 2	High	TCP/PORT	CVE-XXXX-XXXX
3	Finding 3	Medium	TCP/PORT	CVE-XXXX-XXXX
4	Finding 4	Medium	TCP/PORT	CVE-XXXX-XXXX
5	Finding 5	Low/Medium	TCP/PORT	CVE-XXXX-XXXX

Replace the placeholder values above with vulnerabilities actually identified in your scan. Do not invent CVE numbers or severity ratings.

Risk Ranking

The identified vulnerabilities were prioritized according to their potential impact and likelihood of exploitation.

Priority 1 – Critical / High

These findings should receive immediate attention because exploitation could potentially result in significant compromise of the target system or sensitive information.

Recommended action: Remediate as soon as possible.

Priority 2 – Medium

These findings represent meaningful security weaknesses but generally have lower impact or require additional conditions for exploitation.

Recommended action: Remediate during the next planned security maintenance cycle.

Priority 3 – Low

These findings generally represent hardening or configuration improvements.

Recommended action: Address as part of routine security hardening.

Vulnerability Analysis

For every selected finding, the following information was recorded:

Vulnerability name
Severity
Affected service
Affected port
CVE identifier, where available
Description
Potential impact
Risk priority
Recommended remediation

Detailed findings are available in:

findings/vulnerability-findings.md

Remediation Recommendations

General remediation recommendations include:

Apply current security patches and updates.
Remove or disable unnecessary services.
Restrict access to services that do not need to be publicly reachable.
Replace outdated or unsupported software.
Configure secure HTTP response headers where applicable.
Remove unnecessary files and default content from web servers.
Use secure authentication mechanisms and strong credentials.
Regularly perform vulnerability assessments.
Monitor systems for suspicious or unauthorized activity.
Follow the principle of least privilege.

Specific remediation actions should be based on the individual vulnerabilities identified during the scan.

Evidence

Screenshots and supporting evidence are stored in:

screenshots/


Raw scanner output is stored in:

evidence/


The final assessment report is stored in:

reports/

Deliverables

This repository contains the following deliverables:

 Vulnerability scanner configured and verified
 Lab target connectivity verified
 Vulnerability scan performed
 Raw scan output saved
 Minimum of five vulnerabilities analyzed
 Severity and affected service/port documented
 CVE references documented where available
 Vulnerabilities ranked by risk
 Remediation recommendations provided
 Final findings report prepared
Ethical and Legal Notice

This project was performed for educational purposes within an authorized cybersecurity laboratory.

Vulnerability scanners can generate significant network traffic and may affect vulnerable systems. Scanning systems without authorization may violate organizational policies or applicable laws.

Only perform vulnerability scanning against systems that you own or have explicit authorization to assess.

Author

Syed Mujtaba Hussain

Cybersecurity Intern

Week 2 – Vulnerability Assessment
