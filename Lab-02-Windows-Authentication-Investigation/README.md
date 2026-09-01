
# Lab 02 – Windows Authentication Event Investigation

## Overview

This lab demonstrates the investigation of Windows Security Event ID 4625, which records failed logon attempts.

The objective was to generate controlled failed authentication events on a Windows 11 endpoint and investigate the events using Windows Event Viewer.

The investigation focused on identifying the affected account, logon type, failure reason, source information, and determining whether the activity was benign or suspicious.

---

## Objectives

- Identify Windows Event ID 4625
- Investigate failed authentication attempts
- Understand Windows Logon Type 2
- Identify the affected user account
- Analyze authentication failure information
- Identify the source IP address
- Assess repeated failed logon activity
- Apply a basic SOC investigation and classification process

---

## Lab Environment

| Component | Configuration |
|---|---|
| Hypervisor | VMware Workstation |
| Virtual Machine | Security-Endpoint-01 |
| Operating System | Windows 11 Pro |
| Environment | Isolated Home Lab |
| Log Source | Windows Security Event Log |
| Event Investigated | Event ID 4625 |

---

## Investigation Process

### 1. Identify Failed Logon Events

Windows Event Viewer was used to filter the Security log for:

`4625`

Event ID 4625 represents a failed logon attempt.

The initial investigation showed one failed logon event.

---

### 2. Generate Controlled Failed Logons

Three additional failed interactive logon attempts were intentionally generated using the Admin account.

The resulting events occurred within approximately 17 seconds.

This created a small burst of authentication failures for investigation.

---

### 3. Initial Triage

The repeated failed logons were initially classified as:

🟡 **Suspicious / Needs Investigation**

Multiple failed authentication attempts within a short period can require investigation.

However, the presence of multiple failures alone does not prove malicious activity.

Possible explanations can include:

- Incorrect password
- User error
- Caps Lock being enabled
- Brute-force activity
- Password spraying
- A service or application using an outdated password

---

## Event Analysis

The investigated Event ID 4625 contained the following information:

| Field | Finding |
|---|---|
| Event ID | 4625 |
| Target Account | Admin |
| Logon Type | 2 |
| Failure Reason | Unknown user name or bad password |
| Status | 0xC000006D |
| SubStatus | 0xC000006A |
| Workstation | LABADMIN |
| IP Address | 127.0.0.1 |
| IP Port | 0 |
| Authentication Package | Negotiate |
| Logon Process | User32 |

---

## Security Analysis

### Logon Type

The event contained:

`LogonType = 2`

Logon Type 2 represents an interactive logon.

### Authentication Failure

The SubStatus value was:

`0xC000006A`

This indicated that the authentication failure was associated with an incorrect password.

### Source Investigation

The event contained:

`IpAddress = 127.0.0.1`

The address represents localhost, indicating that the activity originated from the same machine in this lab environment.

---

## SOC Assessment

The repeated failures initially warranted investigation because they occurred within a short period.

After examining the event details and correlating the activity with the controlled actions performed during the lab, the activity was determined to be:

🟢 **Benign / Expected – Controlled Lab Activity**

The events were intentionally generated to simulate failed authentication activity and practice security event investigation.

---

## Key SOC Lessons

This exercise demonstrated that a security alert should not automatically be treated as a confirmed security incident.

The investigation followed the process:

**Detect → Investigate → Correlate → Classify**

A single Event ID 4625 indicates a failed authentication attempt, but additional context is required to determine whether the activity is benign, suspicious, or malicious.

---

## Evidence

Screenshots documenting the investigation are stored in the `screenshots` directory.

Evidence includes:

- Event ID 4625 filter results
- Event 4625 General view
- Event 4625 XML details
