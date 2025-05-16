# 🔍 APK & Code Analysis Tool by Luigi Origa

I often need to perform source code reviews, and since the code is confidential, I can't use "suspicious" programs to analyze it.  
Over time, I wrote this small tool to make searching for basic patterns a bit easier.

⚠️ **Disclaimer:**  
It is not my intention to compete with professional tools dedicated to cybersecurity.  
My little program simply unpacks APKs, decompiles Java code, and tries to extract as much information as possible from what’s inside.

---

## 🔧 Features in Version 0.4

- Decompile APK files  
- Decompile Java code  
- Decompress any compressed files found inside  
- Analyze binary files using `binwalk`  
- Convert hex files to binary  
- Extract all certificate information  
- Export all collected data into SQLite3 databases  
- Extract imported/exported functions from `.so` files  
- Mount and extract contents from `squashfs` image files
- Find possible java files used for Activities, Services, Receivers, Providers
- Export the JSON data
- Decompress all XML files

---

## 📁 Output

At the end, a directory is created with lists of files containing:

- Possible execution of other programs  
- Access to local paths  
- Third-party functions  
- Authentication-related functions  
- Base64 decoding  
- Certificate access  
- Crypto functions  
- Database access  
- Usage of shared libraries (.so)  
- Logging  
- Password usage  
- Android permission accesses  
- Use of private and public keys  
- Access to resources  
- Security functions  
- Storage access  
- String initializations  
- Static string comparisons in `if` conditions  
- All URLs found
- Summary of the Java files grouped by Packages
- Short Analysis of Android XML manifest
A subdirectory is also created for the same results **only for third-party public libraries**.

---

## 🛠 Requirements

Make sure the following tools are installed and available in your system's `PATH`:

- `binwalk`  
- `openssl`  
- `exiftool`  
- `readelf`  
- `objdump`  
- `sqlite3`  
- `unsquashfs`  
- `7z`
- python `AXMLPrinter` library

---

## 📌 Note

This tool is for **personal use only** and is not meant for distribution in sensitive environments unless reviewed and approved.
