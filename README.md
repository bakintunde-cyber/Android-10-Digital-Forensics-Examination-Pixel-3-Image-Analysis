# Android 10 Digital Forensics Examination — Google Pixel 3

## Overview

This project documents the examination of an Android 10 Google Pixel 3 forensic image.

The examination involved evidence acquisition, hash verification, filesystem examination, application package analysis, and targeted artifact searches.

## Forensic Examination Report

The complete examination, including the terminal commands, screenshots, evidence analysis, and documented findings, is available in the forensic report below.

📄 **[View the Complete Forensic Examination Report](report/Android_10_Pixel3_Forensic_Report.pdf)**

---

## Investigation Objectives

The examination focused on:

- Obtaining the Android 10 Pixel 3 image
- Calculating the evidence hash
- Examining the Android filesystem
- Reviewing the `/system` directory
- Reviewing the `/data` directory
- Examining application data
- Identifying application packages
- Conducting targeted artifact searches

---

## Evidence Information

| Category | Details |
|---|---|
| Device | Google Pixel 3 |
| Operating System | Android 10 |
| Evidence Type | Android forensic image |
| Examination Type | Filesystem and application artifact examination |

---

## Tools & Technologies

- Linux Terminal
- `wget`
- `sha256deep`
- `unzip`
- `ls`
- `grep`
- `curl`

---

## Examination Process

### 1. Evidence Acquisition

The Android 10 Pixel 3 image was downloaded to the forensic examination environment.

### 2. Evidence Hashing

A cryptographic hash was calculated for the evidence file to establish a reference value for evidence integrity.

### 3. Filesystem Examination

The extracted image was examined through the Android root filesystem, including the `/system` and `/data` directories.

### 4. Application Analysis

Application package information within the Android image was examined to identify installed applications and conduct targeted searches.

### 5. Targeted Artifact Investigation

The examination included investigation of application information associated with Twitter/X Corp and searches for applications associated with money-transfer functionality.

---

## Findings

### Android Filesystem

The examination identified the Android filesystem structure and directories associated with system and application data.

### Application Data

The `/data/data` directory contained application package information that was used for further examination.

### Twitter/X Corp

The examination identified application information associated with Twitter/X Corp.

### Money-Transfer Applications

A targeted search was conducted for applications associated with money-transfer functionality.

---

## Evidence Integrity

A cryptographic hash was calculated for the evidence file before examination.

The hash provides a reference value that can be used to verify the integrity of the evidence.

---

## Limitations

This examination focused on filesystem and application-package analysis.

The examination does not represent a complete reconstruction of all activity on the device. Additional analysis would be required to examine areas such as:

- Application databases
- Messages
- Call records
- Browser history
- Media
- Location artifacts
- System logs
- Deleted data

---

## Skills Demonstrated

- Mobile Device Forensics
- Android Filesystem Analysis
- Digital Evidence Handling
- Cryptographic Hashing
- Evidence Integrity Verification
- Linux Command-Line Analysis
- Application Package Analysis
- Artifact Searching
- Forensic Documentation
- Technical Reporting

---

## Project Structure

```text
android-10-pixel3-forensic-examination/
│
├── README.md
│
├── report/
  └── Android_10_Pixel3_Forensic_Report.pdf
