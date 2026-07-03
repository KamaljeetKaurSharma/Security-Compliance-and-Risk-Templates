# Incident Response Plan (IRP) Phase Playbook
**Framework Alignment:** NIST SP 800-61 Rev. 2 (Computer Security Incident Handling Guide)  
**Classification:** Internal Security Document  

---

## Phase 1: Preparation
*   Maintain updated system configuration baselines and network topology maps.
*   Conduct regular security awareness and data integrity training sessions across business units.
*   Ensure centralized logging solutions actively collect and correlate host telemetry.

## Phase 2: Detection & Analysis
*   **Triage Ingestion:** Helpdesk agents and system coordinators monitor incoming alerts for anomalies (unauthorized account changes, bulk data exports, configuration bypasses).
*   **Severity Categorization:**
    *   *Low:* Single workstation anomaly; no data exposure.
    *   *Medium:* Multiple hosts affected; potential internal PII data movement.
    *   *High:* Active data breach; ransomware behavior; unauthorized exposure of HIPAA/FERPA protected data.

## Phase 3: Containment, Eradication, & Recovery
*   **Immediate Containment:** 
    *   Isolate compromised hosts from the local and wireless network immediately to halt lateral threat propagation.
    *   Do **not** restart or power down endpoints if ransomware or active memory exploits are suspected, preserving volatile RAM for forensics.
*   **Eradication:** Revoke compromised user access tokens, force global enterprise password resets, and run clean anti-malware definition updates across the environment.
*   **Recovery:** Re-image affected infrastructure using verified, secure gold-standard images. Restore data from immutable backup tiers using the 3-2-1 backup methodology.

## Phase 4: Post-Incident Activity (Lessons Learned)
*   Convene an post-incident analysis meeting with technical leads and business analysts within 72 hours of closure.
*   Document what happened, why the breakdown occurred, and update existing technical controls or checklists to prevent future exploits.
