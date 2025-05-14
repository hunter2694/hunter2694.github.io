---
layout: post
title: "TryHackMe: Pen Testing Fundamentals"
date: 2025-05-14
categories: [TryHackMe, Penetration Testing]
---

## Room Name: Pen Testing Fundamentals

### Stage Description

#### Information Gathering
Collects publicly accessible info about target/organization.

#### Enumeration/Scanning
Discovering applications & services running on the system.

#### Exploitation
Leveraging vulnerabilities discovered in the system.

#### Privilege Escalation (PE)
Once we successfully exploit the system, we try to expand our access.

- **Horizontal**: Access another user with the same permissions.
- **Vertical**: Access a user with higher privileges.

#### Post-exploitation
It involves:
- What other things we can exploit.
- Getting important information if accessible.
- Covering tracks.
- Reporting.

---

## Pentesting Methodologies

### OSSTMM (Open Source Security Testing Methodology Manual)
A detailed framework of testing strategies for system, software, application, communication & human aspects.

**Focuses on**:
- Telecommunications (VoIP etc.)
- Wired Networks
- Wireless Communications

**Advantages**:
- Covers various testing strategies in-depth.
- Includes testing strategies for specific targets (i.e: telecom).
- Flexible framework based on org. needs.
- Sets standards for systems & applications.

**Disadvantages**:
- Difficult to understand, very detailed.
- Lacks real-world case studies.
- Inconsistent updates.
- Time-consuming.

---

### OWASP (Open Web Application Security Project)
Community-driven and frequently updated framework for web apps & services.

**Advantages**:
- Easy to understand.
- Actively maintained.
- Covers all stages from testing to remediation.
- Web-focused.

**Disadvantages**:
- Vulnerabilities may overlap.
- No suggestions for specific SDLCs.
- Not formally certified.
- Developer-centric, not enterprise-focused.

---

### NIST Cybersecurity Framework 1.1
Improves cybersecurity standards and risk management from critical infrastructure to commercial use.

**Advantages**:
- Extremely detailed standards.
- Frequently updated.
- Accreditation available.
- Works with other frameworks.

**Disadvantages**:
- Many iterations—hard to choose one.
- Weak auditing policies.
- Doesn't consider cloud computing.
- Resource-intensive.

---

### NSCS CAF (National Cyber Security Centre Cyber Assessment Framework)
A UK-centric framework of 14 principles to assess and defend against threats.

**Focuses on**:
- Data Security & System Security
- Identity & Access Control
- Resiliency, Monitoring
- Response & Recovery

**Advantages**:
- Backed by government agency.
- Provides accreditation.
- Covers wide scope.

**Disadvantages**:
- Principle-based, not rule-based.
- UK-focused.
- Lacks technical implementation.

---

## Black Box vs White Box vs Grey Box Testing

| Type        | Description | Pros | Cons |
|-------------|-------------|------|------|
| **Black Box** | No internal knowledge. Tester acts like a regular user. | Validates full attack surface. No programming skills needed. | Time-consuming for enumeration. |
| **Grey Box**  | Partial knowledge of internal components. | Saves time. | Not full visibility. |
| **White Box** | Full access to internal systems. | Validates all possible attack paths. | Very time-consuming. Requires programming skills. |
