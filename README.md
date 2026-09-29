# Android-10-Digital-Forensics-Examination-Pixel-3-Image-Analysis

## 1. Overview

This project documents the examination of an Android 10 Google Pixel 3 forensic image.

The examination involved downloading the Android image, calculating its hash, extracting the image, examining the Android filesystem, reviewing system and data directories, identifying application packages, and conducting targeted application artifact searches.

The objective was to demonstrate a structured approach to examining Android digital evidence using command-line tools.

## 2. Investigation Objectives

The examination focused on the following objectives:

Obtain the Android 10 Pixel 3 image
Calculate the hash of the evidence file
Examine the extracted Android filesystem
Review the root directory
Examine the /system directory
Examine the /data directory
Examine application data
Identify installed application packages
Investigate application-related artifacts
Conduct targeted searches for applications with specific functionality

## 3. Evidence Information
Category	Details
Device	Google Pixel 3
Operating System	Android 10
Evidence Type	Android forensic image
Evidence File	Pixel 3 image/archive
Examination Type	Filesystem and application artifact examination

## 4. Tools & Technologies
Command-Line Tools
Linux Terminal
wget
sha256deep
unzip
ls
grep
curl
Forensic Techniques
Evidence acquisition
Cryptographic hashing
Evidence integrity verification
Filesystem examination
Directory enumeration
Application package identification
Targeted artifact searching

## 5. Examination Process
### 5.1 Evidence Acquisition

The Android 10 Pixel 3 image was downloaded to the forensic examination environment.

The downloaded image was retained as the original evidence file for subsequent examination.

Example command:

wget <evidence-url>
### 5.2 Evidence Hashing

A SHA-256 hash was calculated for the evidence file.

Example:

sha256deep "Pixel 3.zip"

The resulting hash was used as a reference for verifying the integrity of the evidence.

The original lab documentation records the hash-generation step before continuing with filesystem examination.

### 5.3 Evidence Extraction

The Android image was extracted so that its filesystem contents could be examined.

Example:

unzip "Pixel 3.zip"

The extracted directory provided access to the Android filesystem.

### 5.4 Root Filesystem Examination

The root directory was examined to identify the major components of the Android filesystem.

Example:

ls -l "Pixel 3"

The examination identified directories including:

apex
data
metadata
mnt
odm
product
res
system
vendor

### 5.5 System Directory Examination

The Android system directory was examined to review the contents of the system filesystem.

Command:

ls -l "Pixel 3/system"

This step provided an overview of files and directories contained within the Android system environment.

### 5.6 Data Directory Examination

The /data directory was examined because it contains application and other device data.

Command:

ls -l "Pixel 3/data"

The examination identified multiple directories associated with Android applications and system data.

The original examination documents separate review of the system and data directories.

### 5.7 Application Data Examination

The application data directory was examined to identify installed application packages.

Command:

ls "Pixel 3/data/data"

The resulting package names were used for targeted application searches.

### 5.8 Application Artifact Investigation

A targeted examination was performed on application information associated with Twitter/X Corp.

The examination showed an artifact in which Twitter was represented as X Corp. Additional application information was then examined using Google Play Store metadata.

This demonstrated how application package information can be used to investigate application identity within an Android image.

### 5.9 Money-Transfer Application Investigation

A targeted search was performed to identify applications associated with money-transfer functionality.

Application packages located within the Android application-data directory were searched against Google Play Store information.

The examination produced application matches associated with the search criteria.

## 6. Findings
#### Finding 1 — Android Filesystem

The Pixel 3 image contained an identifiable Android filesystem structure, including system and data directories.

#### Finding 2 — Application Data

The /data/data directory contained numerous application package directories that could be examined during the investigation.
 
#### Finding 3 — Twitter/X Corp

Application-related information examined during the investigation contained references connecting the application information to X Corp/Twitter.

#### Finding 4 — Money-Transfer Applications

A targeted search identified application packages associated with the investigation's money-transfer search criteria.

## 7. Evidence Integrity

Hashing was performed on the evidence file before the filesystem examination.

The resulting hash provides a reference value that can be used to verify that the evidence file has not changed.

For forensic examinations, the original evidence should be preserved and subsequent analysis should be performed against a verified copy whenever possible.

## 8. Investigation Methodology

The examination followed this workflow:

Evidence Acquisition
        ↓
Hash Calculation
        ↓
Evidence Extraction
        ↓
Root Filesystem Examination
        ↓
System Directory Examination
        ↓
Data Directory Examination
        ↓
Application Package Examination
        ↓
Targeted Artifact Searches
        ↓
Documentation of Findings

## 9. Limitations

This examination focused on filesystem and application-package analysis.

The available evidence and examination steps do not establish a complete reconstruction of the device user's activities.

Additional examination would be required to investigate artifacts such as:

- Application databases
- Messages
- Call records
- Browser history
- Media files
- Location data
- System logs
- Deleted data
- Application-specific artifacts

Therefore, findings in this project are limited to the artifacts and examination procedures documented in the investigation.

## 10. Skills Demonstrated

This project demonstrates practical experience with:

- Mobile device forensics
- Android filesystem analysis
- Digital evidence handling
- Cryptographic hashing
- Evidence integrity verification
- Linux command-line tools
- Application package analysis
- Artifact searching
- Evidence documentation
- Forensic reporting

## 11. Conclusion

This project demonstrates a structured examination of an Android 10 Google Pixel 3 forensic image.

The investigation progressed from evidence acquisition and hashing to filesystem examination and targeted application artifact analysis.

The examination provided practical experience working with Android filesystem structures, application packages, cryptographic hashing, command-line forensic techniques, and documentation of digital evidence.

