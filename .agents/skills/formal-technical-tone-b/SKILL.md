---
name: formal-technical-tone-b
description: "Guidelines and templates for authoring formal, enterprise-grade technical specifications, architecture whitepapers, RFCs, client-facing system designs, and executive leadership documents with authoritative third-person precision."
---

# Formal Technical Specification & Architecture Style Guide

This skill governs the creation of **official, enterprise-grade technical documentation, architecture specifications, client-facing proposals, and RFCs**.

The core goal: **Deliver rigorous, authoritative, and professionally structured documentation suitable for executive review, client sign-offs, and enterprise engineering standards.**

---

## 1. Core Principles

### 1. Authoritative Third-Person Voice

- Write with formal engineering rigor (_"The architecture implements...", "The system evaluates...", "Data integrity is enforced via..."_).
- Maintain an objective, professional tone without informal colloquialisms.

### 2. Comprehensive Technical Architecture

- Provide formal component breakdowns, system context diagrams/flows, and interaction lifecycles.
- Explicitly detail security boundaries, cross-origin communication policies (CORS, CSP, postMessage), and state management.

### 3. Formal Decision Matrices & Compliance

- Present exhaustive evaluation criteria (Licensing, Telemetry/Privacy, Performance, SLA, Security Boundaries).
- Document compliance against enterprise standards (SOC2, GDPR, Salesforce Security Review, LWS).

### 4. Structured & Polished Presentation

- Use standardized formal document headers, executive summaries, risk mitigation tables, and rollout roadmaps.

---

## 2. Standard Specification Template

```markdown
# [Project / Component Name] — Technical Architecture & Feasibility Specification

**Document Version:** 1.0  
**Target Platform:** Salesforce Lightning Platform / Enterprise Stack  
**Classification:** Technical Architecture Specification

---

## 1. Executive Summary & Decision Matrix

| Evaluation Dimension       | Primary Recommendation                   | Secondary Alternative | Deprecated Option |
| :------------------------- | :--------------------------------------- | :-------------------- | :---------------- |
| **Component**              | **[Recommended Option]**                 | **[Alternative]**     | **[Deprecated]**  |
| **Licensing**              | MIT (Open Source, Commercial $0)         | MIT                   | Legacy MIT        |
| **Security & Telemetry**   | Zero external telemetry (Self-contained) | Sandboxed iframe      | CSP Risk          |
| **Platform Compatibility** | 100% Native LWC / LWS                    | Full (via iframe)     | Incompatible      |

---

## 2. Architectural Design & Integration Patterns

### 2.1 Native Component Architecture

- Description of DOM mounting, module bundling, and lifecycle hooks.

### 2.2 Security Sandboxing & Isolation

- Description of postMessage protocols, token exchanges, and CSP compliance.

---

## 3. Risk Assessment & Compliance

| Risk Category                | Potential Impact | Mitigation Strategy                                                      |
| :--------------------------- | :--------------- | :----------------------------------------------------------------------- |
| **Platform Security (LWS)**  | Medium           | Host Web Worker-dependent libraries inside sandboxed iframes.            |
| **Data Privacy & Telemetry** | Low              | Package all assets locally in Static Resources; zero external CDN calls. |

---

## 4. Implementation Roadmap & Rollout Strategy

1. **Phase 1: Foundation & Asset Packaging** (Static Resource configuration)
2. **Phase 2: Component Integration & Event Wiring**
3. **Phase 3: Security & Governor Limits Validation**
```
