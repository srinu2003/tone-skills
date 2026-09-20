---
name: formal-technical-tone
description: "Guidelines and templates for authoring formal, enterprise-grade technical specifications, architecture whitepapers, RFCs, client-facing system designs, and executive leadership documents with authoritative third-person precision."
---

# Formal Technical Specification & Architecture Style Guide

This skill governs the creation of **official, enterprise-grade technical documentation, architecture specifications, client-facing proposals, and RFCs**.

The core goal: **Deliver rigorous, authoritative, and professionally structured documentation suitable for executive review, client sign-offs, and enterprise engineering standards.**

---

## 1. Core Principles

### 1. Authoritative Third-Person Voice

- Write with formal engineering rigor (_"The architecture implements...", "The system evaluates...", "Data integrity is enforced via..."_).
- Maintain an objective, professional tone without informal colloquialisms, first-person pronouns (_"I"_, _"we"_), or subjective editorializing.

### 2. Comprehensive Technical Architecture

- Provide formal component breakdowns, system context diagrams/flows, and interaction lifecycles.
- Explicitly detail security boundaries, cross-origin communication policies (CORS, CSP, TLS), and state management.

### 3. Formal Decision Matrices & Compliance

- Present exhaustive evaluation criteria (Licensing, Telemetry/Privacy, Performance, SLA, Security Boundaries).
- Document compliance against enterprise standards (SOC2, GDPR, ISO 27001, security boundaries, and zero-trust policies).

### 4. Structured & Polished Presentation

- Use standardized formal document headers, executive summaries, risk mitigation tables, and rollout roadmaps.

---

## 2. Standard Specification Template

When generating formal architecture documents or RFCs, utilize the following structural standard:

```markdown
# [Project / Component Name] — Technical Architecture & Feasibility Specification

**Document Version:** 1.0  
**Target Platform:** [Target Environment / Cloud Provider / Runtime Stack]  
**Classification:** Technical Architecture Specification

---

## 1. Executive Summary & Decision Matrix

| Evaluation Dimension       | Primary Recommendation                   | Secondary Alternative | Deprecated Option |
| :------------------------- | :--------------------------------------- | :-------------------- | :---------------- |
| **Component**              | **[Recommended Option]**                 | **[Alternative]**     | **[Deprecated]**  |
| **Licensing**              | MIT (Open Source, Commercial $0)         | Apache 2.0            | Proprietary       |
| **Security & Telemetry**   | Zero external telemetry (Self-contained) | Sandboxed isolation   | Unverified CDN    |
| **Platform Compatibility** | Native Runtime Compliant                 | Containerized / Proxy | Incompatible      |

---

## 2. Architectural Design & Integration Patterns

### 2.1 Component Architecture & Lifecycles

- Description of component mounting, dependency bundling, and service lifecycles.

### 2.2 Security Sandboxing & Isolation

- Description of authorization models, token exchange mechanisms, and boundary isolation.

---

## 3. Risk Assessment & Compliance

| Risk Category                     | Potential Impact | Mitigation Strategy                                                              |
| :-------------------------------- | :--------------- | :------------------------------------------------------------------------------- |
| **Runtime & Security Boundaries** | Medium           | Isolate untrusted third-party dependencies within sandboxed workers/containers.  |
| **Data Privacy & Telemetry**      | Low              | Package all dependencies locally in private artifact registries; zero CDN calls. |

---

## 4. Implementation Roadmap & Rollout Strategy

1. **Phase 1: Foundation & Asset Packaging** (Private artifact onboarding & integrity validation)
2. **Phase 2: Component Integration & Event Wiring**
3. **Phase 3: Security & Governor/Performance Limits Validation**
```
