# API Security Risk Analysis

## Overview

This repository contains a professional security assessment of a publicly accessible REST API.  
The objective of this assessment was to evaluate authentication controls, authorization mechanisms, data exposure risks, and API security posture in alignment with industry standards.

The assessment was conducted using controlled and ethical testing methodologies.

---

## Assessment Scope

- Target: JSONPlaceholder Public API
- Focus Areas:
  - Authentication enforcement
  - Object-level authorization
  - Data exposure
  - HTTP method handling
  - Rate limiting controls

No service disruption, exploitation, or malicious activity was performed during testing.

---

## Key Findings

1. **Broken Object Level Authorization (BOLA)**
   - User ID manipulation allows unauthorized access to other user records.

2. **Lack of Authentication Enforcement**
   - Endpoints accessible without any authentication mechanism.

3. **Excessive Data Exposure**
   - API responses return full user objects without data filtering.

4. **Improper HTTP Method Handling**
   - POST requests accepted without validation or authentication.

5. **Absence of Rate Limiting**
   - No restriction on repeated API requests.

---

## Risk Classification Framework

Findings were evaluated based on:

- Likelihood (Low / Medium / High)
- Impact (Low / Medium / High)
- Overall Risk Severity

The vulnerabilities were mapped against the OWASP API Security Top 10 framework.

---

## Business Impact

If present in a production environment, these vulnerabilities could lead to:

- Exposure of sensitive customer data
- Regulatory compliance violations
- Financial penalties
- Loss of customer trust
- Legal and reputational damage

---

## Remediation Recommendations

Immediate Actions:
- Enforce authentication on all endpoints
- Implement object-level authorization checks

Short-Term Improvements:
- Apply response filtering
- Introduce API rate limiting

Long-Term Controls:
- Centralized API gateway security
- Periodic security assessments
- CI/CD-integrated security testing

---

## Ethical Statement

This assessment was conducted solely on publicly available demonstration endpoints for academic and internship evaluation purposes.  
All activities adhered to responsible security research practices.

---

## Author

Karthikeya Dama  
Cybersecurity Intern  
2026
