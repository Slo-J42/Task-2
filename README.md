# Task-2
# 📧 Phishing Email Analysis – Task 2  
> **Objective:** Identify and document phishing characteristics in a suspicious email sample.

![Status](https://img.shields.io/badge/Status-Completed-brightgreen) ![License](https://img.shields.io/badge/License-MIT-blue)

---

## 🗂️ Table of Contents
1. [Overview](#overview)  
2. [Sample Email](#sample-email)  
3. [Methodology](#methodology)  
4. [Key Phishing Indicators](#key-phishing-indicators)  
5. [Results](#results)  
6. [Reproducing the Analysis](#reproducing-the-analysis)  
7. [Tools Used](#tools-used)  
8. [Author](#author)  

---

## Overview
This task demonstrates a structured approach to **phishing-email analysis**.  
We inspect sender details, headers, links, attachments, and language cues to prove the email is malicious, and we summarize the findings in a concise report.

> 📄 **Full PDF Report:**  
> [Phishing_Email_Analysis_Report.pdf]([./Phishing_Email_Analysis_Report.pdf](https://github.com/Slo-J42/Task-2/blob/main/Phishing_Email_Analysis_Report%20(2).pdf))

---

## Sample Email
```
From: support@micr0s0ft-updates.com
Subject: Urgent: Your Microsoft Account Has Been Suspended
Date: Mon, 17 Jun 2025 09:35:12 -0500
Attachment: Account_Verification_Form.docm
Link: https://micr0s0ft-updates.com/verify
```
*Notice the zeroes (“0”) substituting for the letter “o”, the urgent language, and the macro-enabled `.docm` attachment.*

---

## Methodology
| Step | Action |
|------|--------|
| 1 | **Header Analysis** – Upload raw headers to [MxToolbox Header Analyzer]. |
| 2 | **Sender & Domain Check** – Verify the domain spelling (`micr0s0ft-updates.com`) and SPF/DKIM failures. |
| 3 | **Link Inspection** – Hover to reveal mismatched URL; inspect with an isolated browser/VM. |
| 4 | **Attachment Review** – Flag macro-enabled document `.docm` as high-risk. |
| 5 | **Content Review** – Look for urgency, threats, generic greetings, and spelling errors. |
| 6 | **Document Findings** – Record each indicator in the report and rank severity. |

---

## Key Phishing Indicators
| # | Indicator | Evidence |
|---|-----------|----------|
| 1 | **Spoofed Address** | `support@micr0s0ft-updates.com` – fake Microsoft domain. |
| 2 | **Suspicious Link** | URL contains typo and redirects off Microsoft. |
| 3 | **Urgency & Threats** | “Failure to act within 24 hours…” |
| 4 | **Malicious Attachment** | `.docm` file likely contains macros. |
| 5 | **Header Failures** | SPF & DKIM checks = **FAIL**. |
| 6 | **Spelling Tricks** | “micr0s0ft” with zeroes. |
| 7 | **Generic Greeting** | “Dear Customer” instead of real name. |
| 8 | **Impersonation** | Uses Microsoft brand elements with no legitimacy. |

---

## Results
The email is a **confirmed phishing attempt** aimed at harvesting credentials and/or delivering macro-based malware. Immediate deletion and reporting are recommended.

---


## Tools Used
- **Email Client / .eml Viewer** – Thunderbird  
- **Header Analyzer** – MxToolbox  
- **Sandbox Browser / VM** – Kali Linux in VirtualBox  

---

## Author
**Shlok Jadhav** – <beastridershlok@gmail.com>
[LinkedIn](https://www.linkedin.com/in/shlokjadhav)

---

