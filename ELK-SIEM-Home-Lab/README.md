# ELK SIEM Home Lab

## Project Overview

I built this ELK home lab to get hands-on experience with SIEM, log monitoring, and security investigation.

I used Windows 11, Ubuntu, Kali Linux, Elasticsearch, Kibana, and Elastic Agent.

## Simulation 1: Failed Login

I created a failed Windows login and investigated the event in Kibana.

- Event ID: 4625
- Action: Logon Failed
- MITRE Tactic: Credential Access
- MITRE Technique: Brute Force

## Simulation 2: Nmap Scan

I used Kali Linux and Nmap to scan my Windows VM.

- Protocol: TCP
- Action: DROP
- MITRE Tactic: Discovery
- MITRE Technique: Network Service Discovery

I found the activity in Kibana and confirmed that Windows Firewall blocked the connection.

## Simulation 3: PowerShell Activity

I created PowerShell activity on my Windows VM and investigated it in Kibana.

- Event ID: 4104
- Severity: Low
- MITRE Tactic: Execution
- MITRE Technique: PowerShell

I confirmed that the activity came from my authorized home lab test.

## Skills Practiced

- ELK SIEM
- Kibana
- Log Analysis
- Security Monitoring
- Nmap
- PowerShell
- MITRE ATT&CK
- Incident Investigation

## Conclusion

This project helped me practice how to detect, investigate, and document security events using ELK SIEM.
