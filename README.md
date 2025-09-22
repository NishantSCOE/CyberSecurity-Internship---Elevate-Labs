# Task 1: Basic Network Scan with Nmap

This repository contains the report and findings for a basic network reconnaissance task performed using Nmap on my local network.

## 📝 Description

The goal of this project was to get hands-on experience with fundamental network scanning techniques. I scanned my local network (`192.168.43.0/24`) to discover active hosts and identify their open ports and services. This is a foundational skill in cybersecurity for understanding network topology and identifying potential attack surfaces.

## 🛠️ Tools Used

* **Nmap:** For network discovery (`-sn`) and port scanning (`-sS`).
* **Wireshark:** For live packet capture and analysis during the scans.

## 🚀 Steps Performed

1.  **Identified the local IP range** as `192.168.43.0/24`.
2.  **Ran an Nmap Ping Scan** (`-sn`) to find live hosts.
3.  **Ran an Nmap TCP SYN Scan** (`-sS`) on the live hosts to find open ports.
4.  **Captured the traffic** with Wireshark to observe the underlying process.
5.  **Analyzed the output** to identify services and potential security risks.
6.  **Compiled a detailed report** of the findings, including screenshots and analysis.

## 📄 How to View the Report

The full, detailed report of this network scan can be found in this repository:

* **`Task_1_Network_scan_22_Sep.pdf`**

## 📊 Key Findings

The scan revealed **4 active hosts**. The most notable findings were:

* Host `192.168.43.173`, identified as a probable Windows machine via its Intel MAC address.
* This host had **ports 135 (msrpc), 139 (netbios-ssn), and 445 (microsoft-ds)** open.
* These ports are associated with **SMB/NetBIOS file sharing services**, which can be a significant security risk if not properly configured and patched.

These findings highlight the importance of securing common services, even on a local network, to prevent potential unauthorized access or exploitation.
