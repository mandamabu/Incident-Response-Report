# Incident-Response-Report
Incident Response report following NIST SP 800-61, documenting detection and analysis of simulated MITRE ATT&amp;CK techniques (T1110, T1059, T1078) via Wazuh SIEM and Atomic Red Team.

## Overview
This repository contains a complete Incident Response report following the NIST SP 800-61 framework, documenting detection and analysis of simulated MITRE ATT&CK techniques (T1110, T1059, T1078) executed via Atomic Red Team and detected through a custom Wazuh SIEM deployment done in an isolated lab environment.

## Contents
- Incidence Response Report Project — Full incident response report
- Attack timeline file — Attack timeline reconstruction, sourced directly from Wazuh Discover logs
- Wazuh alert screenshots
  
## Report Structure
1. **Incident Summary** — What happened, when detected, systems affected, severity
2. **Detection & Analysis** — How the incident was identified and initial investigation findings
3. **Attack Timeline** — Chronological table of events, sourced from Wazuh logs
4. **Containment & Eradication** — Actions to stop and remove the threat
5. **Lessons Learned** — Honest self-assessment of what worked and what was missed
6. **Recommendations** — Concrete security improvements to prevent recurrence

## Key Findings
- **T1110 (Brute Force):** Detected via Wazuh — `unix_chkpwd` and PAM login failure alerts (rule level 5), 23 July 2026
- **T1078 (Valid Accounts):** Detected via Wazuh — PAM session opened via `su` (rule level 3), 24 July 2026
- **T1059 (Command and Scripting Interpreter):** Detected via Wazuh

## Environment
- **SIEM:** Wazuh manager (Ubuntu Server, 192.168.56.103)
- **Target agent:** Kali Linux, agent ID 001 (192.168.56.101)
- **Attack simulation:** Atomic Red Team (installed via PowerShell 7)
- **Framework:** NIST SP 800-61 (Computer Security Incident Handling Guide)

## Related Repositories
- [Wazuh-SIEM-Lab-Custom-Detection-Rules](#) 
- [MITRE-ATT&CK-Simulation-with-Atomic-Red-Team-and-Detection-with-Wazuh](#) 
