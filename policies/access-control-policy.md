# Access Control Policy — 02: Just-in-Time Privileged Access to Entra ID Administrative Roles

**Classification:** Internal Use - Portfolio Demonstration
**Policy Owner:** Privileged Access Management (PAM)
**Effective Date:** 2026-08-21
**Review Cycle:** Annual
**Version:** 1.0

## 1. Purpose

This policy establishes the mandatory controls governing the architecture described in "Just-in-Time Privileged Access to Entra ID Administrative Roles", in support of the compliance obligations listed in Section 6 and the risk position documented in the associated Compliance Mapping.

## 2. Scope

This policy applies to all personnel, systems, and third parties with access to the in-scope environment: Entra ID (Privileged Identity Management), Okta, Jira Cloud. It applies regardless of employment classification (employee, contractor, or third party) where such access is technically possible.

## 3. Policy Statements

1. No Entra ID administrative role designated as sensitive (User Administrator, Application Administrator, Privileged Role Administrator, or equivalent) shall be assigned on a standing/Active basis.
2. All sensitive role activation shall require Azure MFA at the moment of activation, regardless of prior session authentication state.
3. Activation shall require a written justification referencing an open Jira ticket, and shall require approval from a designated approver prior to activation taking effect.
4. Activation duration shall not exceed the configured maximum (four (4) hours) and shall expire automatically without requiring manual revocation.
5. Eligible role assignments shall be recertified via a recurring Access Review no less frequently than monthly.

## 4. Roles & Responsibilities

| Role | Responsibility |
|---|---|
| Privileged Access Management (PAM) | Owns this policy, approves exceptions, and is accountable for control testing outcomes. |
| System/Application Owner | Ensures the in-scope system is configured in accordance with this policy at all times. |
| Requesting Individual | Complies with the access request and justification process defined in this policy. |
| Internal Audit / Compliance | Independently verifies control operating effectiveness per the testing procedure in `compliance/compliance-mapping.md`. |

## 5. Exceptions

Any deviation from the policy statements in Section 3 requires a documented, time-bound exception, approved in writing by Privileged Access Management (PAM), with a defined expiry date and a compensating control where applicable. Exceptions shall be logged and reviewed at each policy review cycle.

## 6. Related Standards & Requirements

- ISO 27001 A.9.2.3 - Management of privileged access rights
- PCI-DSS Req 7 - Restrict access by business need to know

## 7. Enforcement

Non-compliance with this policy is treated as a control deficiency and shall be logged, tracked, and remediated per the Non-Conformance Handling process defined in `compliance/compliance-mapping.md`. Repeated or willful non-compliance may result in access revocation pending review.

## 8. Document Control

| Version | Date | Author | Change Summary |
|---|---|---|---|
| 1.0 | 2026-08-21 | Privileged Access Management (PAM) | Initial approved version. |

---

[⬅ Back to project README](../README.md)
