# Introduction to Vulnerability Management - Course Challenge Report

---

## Name of Individual Conducting Scanning:
**MSP2_basic**

## Nessus Scanner IP (IP of Kali VM):
**192.168.64.22**

## Date & Time Scan Started:
**28 Jun 2025, 10:04 PM**

## Date & Time Scan Finished:
**28 Jun 2025, 10:24 PM**

## Security Issues Identified:
**71**

---

# Overview

**Provide an overview of the results from the scan. How vulnerable is this system?**

The vulnerability scan revealed a total of **71 vulnerabilities**, including **11 Critical**, **7 High**, and the remaining are Medium or Low.

This indicates the system is in a **highly vulnerable** state. Immediate action is needed to mitigate the critical and high-risk threats to prevent potential compromise, data loss, or unauthorized access.

---

# Top 5 Most Serious Security Issues  
*(In priority order - most important first)*

**What are the 5 most critical issues with the scanned system? Talk about each one, and what could happen if an attacker exploits the vulnerability**

1. **Backdoors: Remote IRC Server Detected**  
   - **Impact:** A remote Internet Relay Chat (IRC) service is running, which is often used by attackers to control compromised systems as part of a botnet.  
   - **Risk:** Could allow attackers to send remote commands and execute arbitrary actions.

2. **Canonical Ubuntu Linux EOL 8.04.x**  
   - **Impact:** This operating system version is no longer supported and does not receive security patches.  
   - **Risk:** Vulnerabilities in core OS components remain unpatched, creating multiple entry points for attackers.

3. **VNC Server with Weak Password**  
   - **Impact:** The Virtual Network Computing (VNC) server is configured with a weak or default password.  
   - **Risk:** Unauthorized users could remotely control the system without much effort.

4. **SSL/TLS Support for Insecure Versions (SSL v2 & v3)**  
   - **Impact:** The system supports outdated SSL protocols that are known to be insecure.  
   - **Risk:** Susceptible to attacks like POODLE, potentially allowing man-in-the-middle interception of encrypted data.

5. **Blind Shell Backdoor Detected**  
   - **Impact:** A known backdoor was detected that allows shell access without proper authentication.  
   - **Risk:** Full control over the system could be obtained by an attacker without triggering alerts.

---

# Top 5 Remediations  
*(In priority order - most important first)*

**What are the suggested remediation actions to address the top 5 most critical security flaws? Re-worded from Nessus suggestions**

1. **Remove or disable the IRC backdoor**  
   Immediately stop and remove any unauthorized IRC services. Investigate system compromise and restore from a known-clean backup if necessary.

2. **Upgrade the operating system**  
   Replace Ubuntu 8.04.x with a supported version to ensure the system receives security updates and patches.

3. **Secure VNC with strong authentication**  
   Enforce strong passwords for VNC access or, ideally, disable VNC if not in use. Use encrypted VNC sessions with additional layers of authentication.

4. **Disable outdated SSL/TLS protocols**  
   Reconfigure all services to use only modern, secure protocols (e.g., TLS 1.2 or TLS 1.3), and disable SSL v2/v3 entirely.

5. **Remove the Blind Shell backdoor**  
   Investigate and remove any unauthorized shell scripts or listeners. Conduct a forensic review and scan other systems for lateral movement.

---
