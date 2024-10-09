# SecureAuth-AD NIST 800-53 Compliance Audit Report

## Audit Overview
**Audit Focus:**  
NIST 800-53 Audit – Account Lockout Policy Control

**Objective:**  
Evaluate SecureAuth-AD settings based on the NIST 800-53 framework, specifically focusing on the enforcement of account lockout policies within the Access Control (AC) family.

---

## 1. Scope Definition
The audit scope includes reviewing the SecureAuth-AD Group Policy Objects (GPOs) to determine the presence and effectiveness of account lockout settings.

---

## 2. Audit Focus: AC-7 Control

### Control Family: Access Control (AC)
**Control:** AC-7 (Unsuccessful Logon Attempts)

### Evaluation Against NIST AC-7 Requirements:
- **Requirement:** Systems must enforce a limit on the number of failed logon attempts within a defined period and automatically lock the account after the limit is reached.
- **Expected Control:** SecureAuth-AD should have a GPO that enforces account lockout after a specified number of failed login attempts.

---

## 3. Audit Findings
During the review, **no account lockout policy** was implemented within the SecureAuth-AD environment.

### Key Findings:
- **Risk Exposure:** The absence of this control leaves the system vulnerable to brute force attacks.
- **Compliance Impact:** Non-compliance with NIST AC-7 access control requirements.

---

## 4. Recommendations

To mitigate this risk and align SecureAuth-AD with NIST 800-53 guidelines:

- **Policy Implementation:**  
  Create a Group Policy to enforce an account lockout after **5 unsuccessful login attempts** within a **15-minute** window.
  
- **Reset Duration:**  
  Set a **lockout duration** to automatically reset after a defined period (e.g., 30 minutes) to prevent denial of service (DoS) attacks.

---

## 5. Conclusion
The failure to implement the AC-7 control for account lockout policies results in non-compliance with the NIST 800-53 framework. Immediate action is recommended to ensure compliance and enhance system security.

**Next Steps:**  
1. Implement the recommended Group Policy changes.
2. Conduct a follow-up audit to confirm compliance.

---


