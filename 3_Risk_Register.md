# CORPORATE RISK REGISTER & CONTRACTUAL SAFEGUARDS
**Project:** CloudVibe Analytics Onboarding  
**Tracking Status:** OPEN / AWAITING VENDOR SIGN-OFF  

| Risk ID | Vulnerability | Severity | Required Technical Fix (AWS) | Required Legal Contract Clause |
| :--- | :--- | :--- | :--- | :--- |
| **RISK-01** | Public Database | **HIGH** | Move database to a private VPC subnet. Restrict access using AWS Security Groups. | **Data Protection Exhibit:** Vendor agrees to isolate all corporate data from public internet networks. |
| **RISK-02** | Static Encryption Key | **MEDIUM** | Implement AWS KMS with automated annual key rotation. | **Cryptographic Standards Clause:** Vendor must utilize AES-256 encryption with automated rotation keys. |
| **RISK-03** | Missing Admin MFA | **HIGH** | Enforce global MFA for all AWS accounts via AWS IAM Identity Center. | **Access Control SLA:** Mandatory Multi-Factor Authentication required for all personnel handling data. |

## FINAL AUTHORIZATION DETERMINATION
**Status:** CONDITIONALLY APPROVED  
**Condition:** The vendor is blocked from receiving any live corporate data until production configurations explicitly confirm the technical fixes above have been deployed.
