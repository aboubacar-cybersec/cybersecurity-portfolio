# 🔎 Splunk SIEM Home Lab

## Project Overview

I built this home lab to gain hands-on experience with Splunk SIEM, log monitoring, and security investigation.

I created three virtual machines using VMware: Windows 11 Pro for the Splunk Enterprise server, Ubuntu as the monitored endpoint, and Kali Linux to simulate security activity.

The goal was to generate security events, collect logs in Splunk, and investigate suspicious activity.

## 🖥️ Lab Environment

- **Windows 11 Pro:** Splunk Enterprise server
- **Ubuntu Linux:** Monitored endpoint
- **Kali Linux:** Security testing machine
- **Splunk Universal Forwarder:** Sends Ubuntu logs to Splunk
- **VMware:** Virtual lab environment

## ⚙️ Splunk Configuration

I configured Splunk Enterprise on Windows to receive data on port **9997**.

I then installed Splunk Universal Forwarder on Ubuntu and connected it to the Windows Splunk server.

I configured the Ubuntu machine to send system and authentication logs to Splunk for monitoring and investigation.

## 🔬 Security Simulations

### 1. Network Reconnaissance with Nmap

I used Kali Linux to perform an Nmap scan against my Ubuntu VM.

The goal was to identify open ports and running services and then investigate the activity using Splunk.

After reviewing the logs, I found that the available system logs did not provide enough network-level information to clearly identify the Nmap scan.

This taught me an important lesson: a SIEM needs the right data sources to detect specific types of attacks.

### 2. Suspicious Web Requests

I used Kali Linux to send suspicious web requests to the Nginx web server running on Ubuntu.

I then searched the Nginx logs in Splunk and identified the activity from the Kali machine.

This confirmed that Splunk was successfully collecting and monitoring the web server logs.

### 3. SSH Login Investigation

I generated failed SSH login attempts from Kali Linux against the Ubuntu server.

I searched the authentication logs in Splunk and found the failed login events.

I also performed a successful SSH login and verified that Splunk recorded the successful authentication event.

## 🔍 Investigation Skills Practiced

- SIEM monitoring
- Log analysis
- Security event investigation
- Nmap network scanning
- SSH authentication analysis
- Web server log analysis
- Linux log monitoring
- Network reconnaissance
- Splunk searching

## 🛡️ Security Recommendations

Based on the investigation, possible security improvements include:

- Monitor repeated failed SSH login attempts
- Create alerts for suspicious authentication activity
- Restrict unnecessary ports and services
- Configure firewall rules
- Monitor web server requests
- Add network-level logging for better port scan detection
- Keep systems and services updated

## 📚 What I Learned

This project helped me understand how a SIEM works in a real lab environment.

I learned how to connect an Ubuntu endpoint to Splunk using Universal Forwarder, collect logs, search security events, and investigate suspicious activity.

I also learned that collecting the right logs is very important. Splunk can only detect activity when the necessary data is available.

My next goal is to improve this lab by creating Splunk alerts and security dashboards.

## 🛠️ Tools Used

Splunk Enterprise | Splunk Universal Forwarder | Windows 11 | Ubuntu Linux | Kali Linux | Nmap | Nginx | SSH | VMware
