# Compliance Mapping — 02: Just-in-Time Privileged Access to Entra ID Administrative Roles

**Classification:** Internal Use - Portfolio Demonstration
**Control Owner:** Privileged Access Management (PAM)
**Testing Frequency:** Annual (or per the cadence stated in the governing policy, where more frequent)

## Control Objectives

| Requirement | Description |
|---|---|
| ISO 27001 A.9.2.3 | Management of privileged access rights |
| PCI-DSS Req 7 | Restrict access by business need to know |

## Implementation Narrative

- Converted standing/Active assignments to sensitive Entra ID roles (User Administrator, Application Administrator) into Eligible assignments under Entra ID Privileged Identity Management (PIM).
- Configured PIM role settings to require MFA re-authentication, a written justification, and human approval at the moment of activation.
- Tied every activation request to an open Jira ticket referencing the business justification, with the ticket ID captured in the PIM audit trail.

## Control Testing Procedure

The following steps constitute the minimum testing procedure to be performed by the control owner, or by internal/external audit, to assess operating effectiveness:

1. Attempt to activate a sensitive role without providing a justification; confirm the activation request is blocked.
2. Submit a valid activation request and confirm it remains in Pending status until the designated approver acts.
3. Sample five (5) completed activations from the PIM audit history and confirm each is traceable to a Jira ticket, an approver, and an automatic expiry timestamp.

## Evidence Artifacts

The following evidence shall be retained and made available on request to support control testing:

- Entra ID PIM role settings export (MFA, justification, approval requirements)
- PIM audit history log covering the review period
- Sample of linked Jira tickets correlated to PIM activation IDs

## Risk Assessment

**Inherent risk:** Standing privileged access to Entra ID administrative roles represents a critical single point of compromise; a single stolen credential could grant unrestricted directory-wide administrative access with no compensating control.

**Residual risk (control in place):** Low. Activation requires MFA, a documented business justification, and human approval, and expires automatically at the end of the configured activation window. Residual risk is limited to approval fatigue under high request volume, mitigated by periodic access-pattern review via the linked Access Review.

## Non-Conformance Handling

Any control testing result that fails one or more steps above shall be logged as a non-conformance, assigned to Privileged Access Management (PAM), and remediated on a timeline commensurate with the residual risk rating. Non-conformances open longer than thirty (30) days shall be escalated per the organization's risk acceptance process.

---

[⬅ Back to project README](../README.md)
