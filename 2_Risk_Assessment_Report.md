# VENDOR RISK ASSESSMENT REPORT (VRAR)
**Target Vendor:** CloudVibe Analytics  
**Assessor:** Lead Cybersecurity Analyst  
**Status:** PENDING REMEDIATION  

## 1. EXECUTIVE SUMMARY
A comprehensive security assessment was conducted on CloudVibe Analytics to evaluate their cloud security posture prior to onboarding. CloudVibe Analytics hosts its SaaS platform on Amazon Web Services (AWS). Based on the responses provided in the Vendor Security Questionnaire, the vendor currently exhibits critical vulnerabilities that pose a high risk to corporate data confidentiality and integrity. 

## 2. RISK ANALYSIS & CLOUD VULNERABILITIES

### FINDING 01: Publicly Accessible Production Database (HIGH RISK)
* **Vulnerability:** The vendor's production database is assigned a public IP address and resides within a public subnet rather than an isolated AWS Virtual Private Cloud (VPC) private subnet.
* **Threat/Impact:** Malicious actors can discover the database via internet scanning tools and launch targeted brute-force or exploit attacks, leading to an unauthorized data breach.

### FINDING 02: Inadequate Cryptographic Key Management (MEDIUM RISK)
* **Vulnerability:** Data-at-rest encryption relies on a static, shared cryptographic key. The vendor does not utilize automated key rotation or AWS KMS Customer Managed Keys (CMKs).
* **Threat/Impact:** Compromise of the single shared key grants permanent access to encrypted data. Lack of automated rotation violates standard compliance frameworks (Security+ / SOC 2).

### FINDING 03: Missing Multi-Factor Authentication (MFA) for Administrative Access (HIGH RISK)
* **Vulnerability:** CloudVibe administrators log into the AWS Management Console using standard single-factor password authentication. Multi-Factor Authentication (MFA) is disabled across administrative accounts.
* **Threat/Impact:** Credential stuffing, phishing, or password leakage targeting a vendor administrator would result in complete account takeover of the cloud environment.
