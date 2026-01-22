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


## Investigation Methodology

##  Email & Header Analysis
1. Reviewed sender address, reply-to fields, and message structure.
2. Identified spoofed domains and social engineering indicators.
##  Email Authentication Validation
1. Conducted SPF, DKIM, and DMARC checks.
2. Confirmed authentication failures indicating message forgery.
## URL, Domain & IP Analysis
1. Analysed embedded URLs for credential harvesting behaviour.
2. Enriched domains and IPs using multiple threat intelligence sources.
## SIEM Log Correlation
1. Analysed proxy logs to confirm user interaction with phishing URLs.
2. Reviewed firewall logs to identify outbound connections to malicious IPs.
3. Examined authentication logs for suspicious login attempts and geolocation anomalies.
## Indicator of Compromise (IOC) Development
1. Compiled malicious IPs, domains, and URLs.
2. Structured IOCs for use in detection and blocking controls.


  ## Key Findings
1. SPF, DKIM, and DMARC checks failed, confirming sender spoofing
2. Malicious domains and URLs were linked to credential harvesting activity
3. SIEM logs confirmed user interaction and outbound connections to attacker infrastructure
4. Authentication logs showed suspicious login attempts from foreign locations

### Incident Response Actions

## Containment
1. Blocked malicious domains, URLs, and IP addresses
2. Disabled affected user accounts and enforced password resets
3. Isolated impacted endpoints
## Eradication
1. Performed full malware scans on affected systems
2. Removed phishing emails from mailboxes
3. Cleared browser sessions and cached credentials
## Recovery
1. Restored cleaned endpoints to production
2. Enforced multi-factor authentication and geolocation-based controls
3, Monitored systems for 72 hours post-incident
## Post-Incident Improvements
1. Updated SIEM detection rules using identified IOCs
2. Documented lessons learned
3. Delivered phishing awareness training to staff


### Indicators of Compromise (IOCs)
A structured list of malicious IP addresses, domains, and URLs identified during the investigation is available in the IOCs/ directory and can be used for detection rule creation and blocking controls.


### Repository Structure

├── Incident-Report/      # Full investigation report (PDF)
├── Screenshots/          # Evidence from analysis and SIEM logs
├── IOCs/                 # Indicators of Compromise
├── Detection-Notes/      # SIEM and detection logic notes
└── README.md

## Disclaimer
This project was conducted in a simulated environment for portfolio purposes only. No real organisation, systems, or personal data were involved.


## Author
Abubakar Yusuf
| SOC Analyst | Cybersecurity Analyst


## Why This Project Matters
This case study demonstrates hands-on SOC analyst skills in phishing detection, investigation, and response, with a strong focus on structured analysis, documentation, and real-world tooling.
