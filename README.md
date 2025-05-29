## Forensic Artifacts of Active Directory Scenario

## 🕵️‍♂️ Forensic Artifacts of Active Directory Scenario

**Course:** BS-DFCS
**Semester:** 5th
**Group Members:** Arsalan, Mihad, Atique, Faheem Azam, Ahmad
**Submitted to:** Ms. Fatima
**Section:** A
**Roll Numbers:** 002, 004, 018, 021, 027

### 📌 Description

This project investigates forensic artifacts discovered during the analysis of an Active Directory environment compromised by malicious actors. The focus was on identifying indicators of compromise (IoCs), persistence mechanisms, and security evasion techniques based on observed artifacts and logs.

### 🧩 Key Findings

* **User OMAction in `NTDS.dit`**
  Indicates presence of a possibly malicious domain/local user account.

* **Uninstallation of Security Tools**

  * Microsoft Security Client
  * Microsoft Forefront Endpoint
  * MS Endpoint Protection

  The coordinated removal suggests an intentional act to create a vulnerability window for exploiting the system.

* **Presence of `MpCmdRun.exe`**
  A legitimate Windows Defender tool, potentially used or mimicked in malicious operations. System registry showed it was unregistered in Windows Security Center—potentially due to tampering.

* **Reinstallation of Security Tools**
  Suspicious reinstallation of:

  * Microsoft Endpoint Protection Management
  * Microsoft Security Client
    Possibly used to cover tracks after exploitation.

* **Ransomware Executables Found**

  * `windows_enrypt.exe`
  * `windows32_encrypt.exe`
    These files encrypted the system and displayed a ransom note.

* **Persistence via Autorun Entry**

  * Malicious autostart entry found: `mprun`
    Used to maintain access after reboot—common malware persistence method.

### 🔐 Educational Purpose

This project was created purely for academic learning, simulating a real-world security incident for analysis. It highlights the importance of endpoint visibility, secure system configurations, and persistence detection technques.
