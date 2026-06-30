# CRAPI (Completely Ridiculous API) Penetration Testing Report

## Overview

This repository contains a professional penetration testing report for **CRAPI (Completely Ridiculous API)**, a deliberately vulnerable API application designed by the **OWASP** community for learning and practicing modern API security testing.

The objective of this project was to simulate a real-world API security assessment by identifying, exploiting, documenting, and reporting security vulnerabilities using industry-standard penetration testing methodologies.

The assessment was performed manually using tools such as **Burp Suite**, **Postman**, and **JWT analysis tools**, following the **OWASP API Security Top 10 (2023)** and **OWASP Web Security Testing Guide (WSTG)**.

---

# What is CRAPI?

CRAPI (Completely Ridiculous API) is an intentionally vulnerable API platform created to help security professionals, penetration testers, developers, and students learn API security through hands-on practice.

Unlike traditional vulnerable web applications, CRAPI focuses primarily on REST API vulnerabilities commonly found in modern applications, including broken authentication, authorization flaws, mass assignment, business logic vulnerabilities, insecure API design, and information disclosure.

Official Project:
https://github.com/OWASP/crAPI

---

# Installation

## Clone the repository

```bash
git clone https://github.com/OWASP/crAPI.git
```

## Navigate to the Docker deployment folder

```bash
cd crAPI/deploy/docker
```

## Start the application

```bash
sudo docker-compose --compatibility up -d
```

## Verify containers

```bash
sudo docker ps
```

## Access the application

```
https://localhost:8888
```

---

# Objectives

The purpose of this assessment was to:

* Perform a complete API penetration test.
* Identify high-impact vulnerabilities.
* Assess authentication and authorization controls.
* Evaluate business logic flaws.
* Document findings in a professional penetration testing report.
* Recommend practical remediation measures.

---

# Vulnerabilities Covered

This report demonstrates practical exploitation and documentation of the following vulnerability classes.

## Broken Object Level Authorization (BOLA)

Occurs when an API fails to verify whether an authenticated user is authorized to access a specific object or resource.

Example:

* Accessing another user's reports
* Viewing another user's orders

---

## Broken Function Level Authorization (BFLA)

Occurs when privileged API functions are accessible to users without the required permissions.

Example:

* Deleting videos using administrative endpoints
* Updating another user's order status

---

## Mass Assignment

Occurs when the API automatically binds user-controlled parameters to sensitive backend properties without proper validation.

Example:

* Changing product prices
* Assigning privileged properties

---

## Broken Authentication

Weak authentication mechanisms allow attackers to compromise user accounts.

Example:

* OTP brute force
* Account takeover
* Authentication bypass

---

## Business Logic Vulnerabilities

Application workflows fail to enforce intended business rules.

Example:

* Negative quantity resulting in account credit
* Manipulating financial calculations

---

## Information Disclosure

Sensitive information is exposed to unauthorized users.

Example:

* Downloading another user's reports
* Accessing internal application data

---

# Report Contents

The accompanying penetration testing report includes:

* Executive Summary
* Testing Methodology
* Scope of Assessment
* Risk Rating
* Detailed Findings
* Proof of Concept (PoC)
* HTTP Requests & Responses
* Screenshots
* Business Impact
* Root Cause Analysis
* Remediation Recommendations
* OWASP Mapping

Each finding follows a professional reporting format similar to those used during real-world security assessments.

---

# Tools Used

* Burp Suite Professional
* Postman
* Docker
* JWT Tools
* Browser Developer Tools
* Linux (Kali)
* Manual API Testing

---

# Skills Demonstrated

* API Penetration Testing
* REST API Security Assessment
* Authentication Testing
* Authorization Testing
* Business Logic Testing
* HTTP Request Manipulation
* Burp Suite Professional
* API Enumeration
* Vulnerability Reporting
* Risk Assessment

---

# Disclaimer

CRAPI is an intentionally vulnerable application developed for educational and security research purposes. All testing documented in this repository was performed in a controlled laboratory environment. Do not perform similar testing against systems without proper authorization.
