### Phishing Incident Investigation – SOC Case Study

## Overview
This repository documents a phishing incident investigation conducted within a simulated Security Operations Centre (SOC) environment. The project demonstrates end-to-end incident handling, including email header analysis, authentication validation (SPF, DKIM, DMARC), malicious URL and domain analysis, SIEM log correlation, indicator of compromise (IOC) development, and incident response actions aligned with SOC best practices.

The investigation follows a structured SOC methodology and reflects real-world phishing response workflows commonly used in enterprise and healthcare environments.

## Incident Summary
In November 2025, a phishing campaign impersonating Microsoft and a medical supplier targeted a healthcare organisation. The emails contained spoofed sender domains, malicious URLs, and attempted credential harvesting techniques. Two users interacted with the phishing links, resulting in limited outbound connections to attacker-controlled infrastructure.
The incident was promptly identified, contained, and remediated. No successful account compromise or data loss occurred.

## Objectives
1. Identify phishing indicators through email header and content analysis
2. Validate sender authenticity using SPF, DKIM, and DMARC checks
3. Analyse URLs, domains, and IP addresses using threat-intelligence platforms
4. Correlate SIEM logs to confirm user interaction and attacker activity
5. Contain, eradicate, and recover from the incident using SOC incident response procedures
6. Document findings and enhance organisational phishing awareness


## 🛠️Tools & Technologies
1. Splunk Cloud (Free Edition) – SIEM log analysis and event correlation
2. MXToolbox – SPF, DKIM, and DMARC validation
3. Email Header Analysis Tools – Message header parsing and inspection
4. VirusTotal – URL, domain, and IP reputation analysis
5. Hybrid Analysis – Sandbox analysis of suspicious URLs
6. AbuseIPDB – IP reputation and threat intelligence enrichment


