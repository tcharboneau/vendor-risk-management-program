# VENDOR SECURITY QUESTIONNAIRE (VSQ)
**Target Architecture:** AWS Cloud-Hosted SaaS Applications  
**Classification:** Internal Corporate Use Only  

## 1. IDENTITY & ACCESS MANAGEMENT (IAM)
* **SEC-IAM-01:** Describe the authentication mechanism required for administrative access to the hosting AWS environment. (e.g., SAML 2.0 SSO, IAM Users).
* **SEC-IAM-02:** Is Multi-Factor Authentication (MFA) strictly enforced for all administrative, programmatic, and root-level accounts? Please specify token types used.
* **SEC-IAM-03:** Detail your password complexity requirements and account lockout policies for accounts accessing corporate environments.

## 2. DATA PROTECTION & CRYPTOGRAPHY
* **SEC-DAT-01:** Detail the cryptographic standards utilized for data-at-rest within your AWS environment (e.g., AES-256 via AWS KMS).
* **SEC-DAT-02:** Who manages the cryptographic keys utilized for database encryption? (Vendor-managed vs. Customer Managed Keys).
* **SEC-DAT-03:** Describe how data is encrypted while in transit across public and internal networks (e.g., TLS 1.3).

## 3. NETWORK ARCHITECTURE & BOUNDARY PROTECTION
* **SEC-NET-01:** Provide an architectural overview of how customer data environments are isolated within your AWS Virtual Private Cloud (VPC).
* **SEC-NET-02:** Are production databases hosted in public-facing subnets, or are they isolated in private subnets utilizing Network Address Translation (NAT) Gateways?
* **SEC-NET-03:** What edge-boundary protections are deployed to mitigate Layer 7 (Application) web attacks and Distributed Denial of Service (DDoS) threats?

## 4. LOGGING, AUDITING & COMPLIANCE
* **SEC-LOG-01:** Is AWS CloudTrail enabled across all AWS Regions? Describe how CloudTrail log integrity is protected against administrative tampering.
* **SEC-LOG-02:** What is your standard log retention period for security-related events, and where are these logs centrally aggregated?
* **SEC-LOG-03:** Provide a list of third-party security certifications currently held by the organization (e.g., SOC 2 Type II, ISO 27001).
