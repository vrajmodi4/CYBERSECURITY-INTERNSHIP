# CYBERSECURITY-INTERNSHIP
Task 3  : Perform a Basic Vulnerability Scan on Your PC

# Vulnerability Scan Report
**Target IP:** 192.168.1.10  
**Scan Date:** 2025-09-26 10:11:14 (IST)  
**Scanner used:** OpenVAS / Nessus Essentials (replace with what you used)  
**Prepared by:** [VRAJ MODI]

---

## 1. Executive Summary
This document contains the results of a basic vulnerability scan performed against the target IP **192.168.1.10**. The scan was performed using a community/free vulnerability scanner (OpenVAS or Nessus Essentials). The goal was to identify common misconfigurations, missing patches, and high/critical vulnerabilities affecting a typical personal computer or local server.

**Key findings (high level):**
- Number of critical/high severity issues: 0-5 (example)
- Number of medium severity issues: 2-8 (example)
- Number of low severity issues: 5-15 (example)

> Note: Replace the summary numbers above with actual counts from your scan results.

---

## 2. Scan Details
- **Scan Type:** Full system scan
- **Scan Duration:** (example: 00:40:12)
- **Scan Policy:** Default/Full/Authenticated (specify)
- **Credentials used:** None / Local credentials (if authenticated scanning was used)
- **Target:** 192.168.1.10 (single host)
- **Ports scanned:** Top 65535 / default TCP+UDP (specify)
- **Notes:** Scanning a live system may trigger IDS/IPS alerts. Ensure you have permission to scan.

---

## 3. How I ran the scan (commands / steps)
### OpenVAS (Greenbone) - quick steps
1. Install Greenbone/OpenVAS following official docs.
2. Add target: 192.168.1.10
3. Create and run a Full and Fast scan task.
4. Export results as PDF/CSV.

### Nessus Essentials - quick steps
1. Install Nessus Essentials and register.
2. Add a new scan -> Basic Network Scan.
3. Set target to 192.168.1.10 and run.
4. Export report as PDF/CSV.

## 4. Findings (sample template — replace with your actual findings)
| ID | Vulnerability Title | Port/Service | Severity | CVSS v3 | Description | Recommended Remediation |
|----|---------------------|--------------|----------:|--------:|-------------|-------------------------|
| V-001 | Outdated OpenSSH version | 22/tcp (ssh) | High | 7.5 | OpenSSH version is outdated and may be vulnerable to known exploits. | Update OpenSSH to latest stable release; apply vendor patches. |
| V-002 | SMB Signing not required | 445/tcp (smb) | Medium | 5.3 | SMB server allows unsigned sessions which may enable man-in-the-middle attacks. | Enable SMB signing and apply strict SMB policies. |
| V-003 | SMBv1 enabled | 445/tcp (smb) | High | 8.1 | Legacy SMBv1 is enabled; it is vulnerable to multiple historic exploits (e.g., WannaCry). | Disable SMBv1 and enable SMBv2/v3. |
| V-004 | Missing Windows Security Updates | N/A | Medium | 6.0 | Several critical patches not applied. | Apply latest OS security updates and reboot. |
| V-005 | Weak TLS ciphers | 443/tcp (https) | Medium | 5.0 | Server allows weak ciphers (RC4, SSLv3). | Disable weak ciphers; enable TLS 1.2/1.3 only. |

> Replace the table above with the real vulnerabilities and exact CVSS scores from your scanner export.

---
## 5. Most Critical Vulnerabilities (detailed)
**V-001: Example - SMBv1 enabled**  
- **Severity:** High (CVSS 8.1)  
- **Affected Service:** SMB on port 445  
- **Description:** SMBv1 is deprecated and has multiple critical vulnerabilities that allow remote code execution.  
- **Proof / Evidence:** (paste scanner output or screenshots)  
- **Remediation Steps:**  
  1. Disable SMBv1 on the host   
  2. Test connectivity for required clients.  
  3. Apply latest OS patches and verify.

(Repeat for each critical issue)
