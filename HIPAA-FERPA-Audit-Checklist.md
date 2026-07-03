# Public Sector Data Privacy & Compliance Audit Checklist
**Framework Focus:** HIPAA (Health Insurance Portability and Accountability Act) & FERPA (Family Educational Rights and Privacy Act)  
**Author:** Kamaljeet Sharma, MS in Information Security & Assurance  

---

## 📌 Overview
This compliance audit checklist translates complex federal statutory requirements into actionable technical validation checkpoints for system administrators and business analysts. It ensures that internal software workflows handling Protected Health Information (PHI) and Personally Identifiable Information (PII) maintain strict data confidentiality and integrity.

---

## 🔒 Section 1: Identity & Access Management (IAM) Enforcements
*   [ ] **Enforce Least Privilege:** Verify that role-based access control (RBAC) schemas restrict system permissions so users only access data necessary for their specific job duties.
*   [ ] **Unique User Identification:** Ensure every employee utilizes an individual network account. Generic or shared team accounts accessing PII/PHI are strictly prohibited.
*   [ ] **Multi-Factor Authentication (MFA):** Confirm MFA is active and mandatory for all local and remote authentications to systems housing sensitive data.
*   [ ] **Automated Session Timeouts:** Verify that application and workstation sessions automatically lock or log out after 15 minutes of inactivity.

---

## 🖥️ Section 2: Technical & Data Security Controls
*   [ ] **Data-at-Rest Encryption:** Confirm all endpoint storage volumes and backend database tiers housing PII/PHI utilize AES-256 bit encryption.
*   [ ] **Data-in-Transit Encryption:** Audit network data flows to guarantee that all sensitive data transmissions use secure cryptographic protocols (e.g., HTTPS via TLS 1.3, secure SFTP).
*   [ ] **Message-Recall & Outbound Email Rules:** Ensure corporate email transport rules intercept, flag, or require manual authorization if data elements matching SSNs or case file patterns are detected in outbound mail to unverified domains.
*   [ ] **Immutable Audit Logging:** Verify that system logging engines track all user events (logins, logouts, data modifications, data exports) and that these logs are stored in an unalterable, centralized server.

---

## 👥 Section 3: Administrative & Workflow Governance
*   [ ] **Security Awareness Training:** Confirm all onboarding personnel complete mandatory data-handling privacy modules covering secondary trauma, HIPAA boundaries, and phishing identification.
*   [ ] **Incident Notification Flow:** Validate that clear, documented escalation pathways exist to report suspected or confirmed data exposures within statutory timelines.
*   [ ] **Authorized Material Storage:** Verify that training resources, manuals, and templates are maintained in secure, centralized shared folders with restricted write access to prevent unauthorized modification.
