# Splunk-analysis
Performed end-to-end investigations of multiple simulated cyber incidents within Splunk SIEM.
# SOC Alert Investigation using Splunk SIEM

## Overview

This project simulates the daily responsibilities of a Tier 1 Security Operations Center (SOC) Analyst by investigating multiple security alerts within a Splunk SIEM environment. The investigation covers Linux authentication attacks, Windows persistence techniques, and web application compromise, following the SOC incident triage process used by Managed Security Service Providers (MSSPs).

The objective was to analyze security logs, validate alerts, distinguish between true positives and false positives, identify attacker behaviour, and determine when incidents should be escalated to higher-level analysts.

---

## Objectives

* Investigate security alerts using Splunk SIEM.
* Perform log analysis across Linux, Windows, and Web environments.
* Identify Indicators of Compromise (IOCs).
* Detect attacker tactics, techniques, and procedures (TTPs).
* Classify alerts as True Positive or False Positive.
* Produce incident findings suitable for escalation to SOC Level 2.

---

## Environment

* Splunk Enterprise SIEM
* Linux Authentication Logs (SSH)
* Windows Security Event Logs
* Web Server Access Logs
* Simulated Enterprise Environment
* MITRE ATT&CK Mapping
* Threat Intelligence Validation

---

# Scenario 1 – Linux Brute Force Investigation

### Alert

Brute Force Activity Detection

### Investigation Activities

* Examined Linux SSH authentication logs.
* Identified failed and successful authentication attempts.
* Used SPL queries to extract usernames, source IP addresses, and authentication status.
* Determined attack duration.
* Confirmed successful compromise of a user account.
* Identified privilege escalation to the root account.
* Investigated persistence mechanisms created after compromise.

### Key Findings

* Over 500 failed authentication attempts against a single user.
* Successful login following brute force attack.
* Privilege escalation to root.
* Attacker created a new local account for persistence.
* Confirmed incident as a True Positive.
* Recommended immediate escalation to SOC Level 2 and Incident Response.

---

# Scenario 2 – Windows Persistence Investigation

### Alert

Suspicious Scheduled Task Creation

### Investigation Activities

* Investigated Windows Event ID 4698.
* Examined scheduled task configuration.
* Identified malicious PowerShell execution.
* Detected abuse of CertUtil for payload download.
* Traced process creation chain.
* Identified parent process responsible.
* Investigated lateral movement source.
* Reviewed attacker discovery activities.

### Key Findings

* Malicious scheduled task created for persistence.
* Payload downloaded using CertUtil.
* PowerShell executed downloaded malware.
* Parent process identified as cmd.exe.
* Attacker enumerated the local Administrators group.
* Identified remote workstation used during compromise.
* Classified activity as a True Positive.

---

# Scenario 3 – Web Shell Investigation

### Alert

Potential Web Shell Upload

### Investigation Activities

* Investigated web server access logs.
* Identified brute force activity against WordPress login.
* Detained suspicious User-Agent (Hydra).
* Investigated unusual POST requests.
* Identified access to the b374k PHP web shell.
* Validated attacker infrastructure using threat intelligence.
* Reviewed attacker interaction with uploaded web shell.

### Key Findings

* Hydra used for credential brute forcing.
* Multiple successful POST requests through b374k.php.
* Confirmed active web shell usage.
* Identified malicious external IP.
* Classified activity as a True Positive.
* Recommended escalation for full incident response.

---

# Skills Demonstrated

* Security Monitoring
* Security Operations Center (SOC)
* Splunk SIEM
* Log Analysis
* Security Event Investigation
* Linux Security
* Windows Security Monitoring
* Web Security Monitoring
* Threat Hunting
* Incident Triage
* Digital Forensics Fundamentals
* Threat Intelligence
* MITRE ATT&CK Mapping
* IOC Identification
* SSH Authentication Analysis
* Windows Event Log Analysis
* Web Server Log Analysis
* PowerShell Analysis
* Process Tree Investigation
* Scheduled Task Analysis
* Persistence Detection
* Privilege Escalation Analysis
* Incident Escalation
* Cyber Threat Detection

---

# Outcome

Successfully investigated three independent cyber attack scenarios, validated malicious activity through log analysis, identified attacker techniques, documented findings, and produced incident summaries aligned with SOC analyst responsibilities. The project demonstrates practical experience performing Tier 1 SOC investigations using Splunk SIEM across Linux, Windows, and web environments.
