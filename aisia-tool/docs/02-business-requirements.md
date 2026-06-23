# AISIA — Business Requirements Document

---

| Document specification | |
|---|---|
| **AI System Impact Assessment Tool Version:** | 0.1 |
| **Author:** | Dorota Wasiak |
| **Document type:** | Business Requirements Document |
| **Last updated:** | June 2026 |
| **Status:** | Draft |

---

## Table of Contents

1. [Purpose of this Document](#1-purpose-of-this-document)
2. [Business Objectives](#2-business-objectives)
3. [Stakeholders](#3-stakeholders)
4. [Scope](#4-scope)
5. [Assumptions](#5-assumptions)
6. [Constraints](#6-constraints)
7. [Business Requirements](#7-business-requirements)
8. [Stakeholder Requirements](#8-stakeholder-requirements)
9. [High-Level Acceptance Criteria](#9-high-level-acceptance-criteria)
10. [Traceability Matrix](#10-traceability-matrix)
11. [Glossary Reference](#11-glossary-reference)

---

## 1. Purpose of this Document

This Business Requirements Document (BRD) outlines the business's requirements for the AISIA tool in sufficient detail to inform the design of the solution, while not prescribing the technical implementation.

It is based directly on the strategic rationale set out in the Business Case, which addresses the question, "Should this be built?" This BRD addresses the next question: "What specifically does the business require?"

This design-agnostic document describes business needs and outcomes rather than screen layouts, field names or technical architecture. Detailed functional specifications, field-level requirements and acceptance criteria are documented separately in the Functional Requirements Document (FRD), which is linked back to the business requirements defined here.

This BRD is intended for:

- Business sponsors and decision-makers, to validate that the solution will meet organisational needs;
- Business analysts, to translate these requirements into detailed functional specifications;
- Compliance and risk reviewers (legal, DPO and risk leads), to confirm that organisational risk and compliance boundaries have been correctly captured before technical design begins.

This BRD is written from the perspective of a hypothetical organisational sponsor, simulating the structure and rigor of a formal BRD as would be produced for an enterprise AI governance initiative. It reflects requirements independently identified and authored by the tool's initiator (see Section 3: Stakeholders), based on analysis of applicable regulatory frameworks and AI governance best practice.

---

## 2. Business Objectives

Business objectives represent the high-level outcomes that the organisation seeks to achieve through AISIA. Each objective is derived from the strategic context and identified benefits of the business case.

| ID | Business Objective | KPI / Success Measure |
|---|---|---|
| **BO-001** | Enable structured, consistent, and auditable assessment of AI system impacts across the organisation | 100% of registered internal AI systems undergo the same structured workflow. |
| **BO-002** | Demonstrate compliance readiness against ISO/IEC 42001:2023, the EU AI Act, and GDPR requirements relevant to AI systems | Zero non-conformances identified during external ISO 42001 / AI Act pre-audits. |
| **BO-003** | Reduce reliance on ad hoc, inconsistent, or undocumented AI risk evaluation practices | Discontinuation of any pre-existing ad hoc tracking methods (e.g. spreadsheets) within 3 months of launch. |
| **BO-004** | Provide decision-makers with sufficient, well-organised information to approve, condition, or reject AI system deployments | <10% of submitted assessments are returned/rejected by decision-makers due to missing baseline information (reducing RFI loops). |
| **BO-005** | Establish a defensible audit trail of AI governance decisions to support regulatory inquiry, internal audit, or external review | 100% of finalized governance decisions generate an immutable, exportable log containing user IDs, exact timestamps, and decision rationales. |
| **BO-006** | Support cross-functional collaboration between business, legal, technical, and data protection stakeholders in AI governance | 100% of "High-Risk" AI systems reflect documented, system-enforced sign-offs from Legal, Technical, and Business leads prior to deployment. |

---

## 3. Stakeholders

This section outlines the key stakeholders within the AISIA ecosystem and defines their core interests, which will directly inform the functional access layers and user experience designs of the solution.

| Stakeholder | Interest in AISIA |
|---|---|
| **AI Governance Lead / Business Analyst** | Co-ordinates organization-wide assessments, updates regulatory mapping templates, and ensures compliance methodologies are consistently applied. |
| **System Owner** | Responsible for the ultimate risk profile of the AI system; requires clear and defensible assessment outcomes in order to make and justify deployment decisions with confidence. |
| **Data Protection Officer (DPO)** | Seeks alignment with GDPR/DPIA workflows; requires confirmation of scope overlap between data protection laws and AI governance to eliminate redundant assessments. |
| **Legal / Compliance Reviewer** | Requires assurance that EU AI Act classifications and related strict regulatory obligations are accurately captured and fully traceable. |
| **AI Ethics Board** | Demands high-quality, well-structured, and granular information to either approve, condition, or reject complex AI system deployment plans. |
| **End Users (Assessors)** | Require an intuitive, high-usability interface that minimizes operational friction and fits naturally within existing AI governance review cycles. |
| **IT Security** | Require absolute assurance that data handling practices (underlying infrastructure, data storage localization, and report exports) strictly comply with internal corporate security baselines. |
| **Initiator & AI Governance Lead** | Self-sponsored initiative based on independent analysis of regulatory obligations. |

---

## 4. Scope

### 4.1 In Scope

- **Local Sequential Workflow:**
  A guided, step-by-step assessment wizard covering system description, trigger identification, impact analysis, deployment decision-making (approve, condition, reject), GDPR/DPIA synchronization, and a formal sign-off screen.

- **Static Risk Matrix Scoring:**
  Algorithmic calculation of risk severity based on user-inputted impact likelihood and consequence weightings.

- **Framework Mapping:**
  Inline structural mapping linking assessment query points to specific clauses in ISO/IEC 42001:2023, the EU AI Act, and GDPR.

- **File-Based Lifecycle Management:**
  Full capability to export the complete assessment state into a portable JSON format and import it back to resume work or review.

- **Audit-Ready Document Export:**
  Generation of a clean, standardised plain text report capturing all answers, timestamps, and entered rationales, suitable for formal record-keeping and audit trail purposes.

- **Strict Client-Side Isolation:**
  100% client-side execution within the user's browser web session. Absolutely no server-side storage, database hosting, or outbound data transmission of assessment content.

### 4.2 Out of Scope

- **Centralized Database & Hosting:**
  No centralized server-side registry of assessments or user accounts.

- **Real-Time Collaborative Editing:**
  Simultaneous multi-user editing or live workspace sharing (e.g., Google Docs style).

- **Automated Workflow Notifications:**
  In-app chat, automated system emails, or native routing tasks between users. (Workflows are managed manually by exporting/sharing files via existing corporate communication channels).

- **External Integrations:**
  Active API integrations with enterprise GRC platforms, external corporate AI System Registers, or automated legal filings to regulatory bodies.

---

## 5. Assumptions

Assumptions represent factors that are accepted as true for the duration of the project lifecycle without immediate proof. They establish the operational and organizational baseline required for the AISIA tool to deliver its intended value.

| ID | Assumption | Impact if proven false |
|---|---|---|
| **AS-001** | Users have a foundational understanding of AI governance terminology and the purpose of impact assessments | Higher rate of inaccurate classifications or user confusion during data entry. |
| **AS-002** | The organisation has, or is developing, an AI Management System (AIMS) policy that defines roles, responsibilities, and escalation paths referenced by the assessment process | Assessment outcomes will lack an authoritative organisational framework to enforce compliance actions. |
| **AS-003** | Assessments are conducted by or in co-ordination with individuals authorised to make or recommend AI deployment decisions | Without operational impact on actual product rollouts, the tool merely becomes theoretical. |
| **AS-004** | Users have access to a modern web browser capable of supporting local storage and client-side JavaScript execution | The application will fail to run or export files correctly due to technical infrastructure limitations. |
| **AS-005** | The organisation has an existing or planned AI System Register against which individual assessments can be cross-referenced | Loss of clear traceability between the individual impact assessment and the broader corporate IT inventory. |
| **AS-006** | Where personal data is involved, a Data Protection Officer or equivalent function is available for consultation | Delays in completing assessments when personal data processing complexities exceed standard wizard thresholds. |

---

## 6. Constraints

Constraints are non-negotiable boundaries or restrictions imposed on the solution by the project's operating environment, budget or resource availability. These must be strictly adhered to during the design phase.

| ID | Constraint | Architectural / Design Impact |
|---|---|---|
| **CO-001** | The solution must operate entirely client-side, with no backend server or database, due to the absence of dedicated hosting infrastructure or budget for this initiative | All application logic, routing, risk calculation, and UI rendering must execute within the user's browser. |
| **CO-002** | Data persistence is limited to browser local storage; no cross-device or cross-browser synchronisation is available | Users must rely on manual file export/import features to transfer assessment data across different devices or browsers. |
| **CO-003** | The solution must be deliverable and maintainable by a single contributor without dedicated development resourcing | The technical stack must prioritize maintainability and simplicity to avoid technical debt. |
| **CO-004** | The solution must remain accessible via static web hosting (GitHub Pages), without server-side processing capabilities | The tool cannot utilize server-side APIs, server-side authentication, or dynamic server rendering. |
| **CO-005** | Regulatory frameworks referenced (EU AI Act, ISO/IEC 42001:2023) are subject to ongoing official guidance and amendment; the solution must be maintainable as these frameworks evolve | Questionnaire logic, clauses, and weights must be decoupled from the core codebase—ideally structured in modular configuration files (e.g., local JSON maps) for easy updates. |

---

## 7. Business Requirements

Business requirements represent the high-level goals, operational capabilities, and outcomes the organisation needs from AISIA, independent of how the solution implements them. Each requirement is prioritised using the MoSCoW framework (Must have / Should have / Could have) and traced to its originating business objective.

### 7.1 Regulatory Compliance Requirements

| ID | Requirement | Priority | Traces to |
|---|---|---|---|
| **BR-001** | The business requires the ability to classify AI systems according to EU AI Act risk tiers as part of the assessment process. | Must | BO-002 |
| **BR-002** | The business requires each assessment section to be traceable to specific ISO/IEC 42001:2023, EU AI Act, and GDPR provisions. | Must | BO-002, BO-005 |
| **BR-003** | The business requires a mechanism to identify when a planned or deployed AI system constitutes an unacceptable risk under the EU AI Act, such that deployment can be halted. | Must | BO-002, BO-004 |
| **BR-004** | The business requires co-ordination between AI impact assessment and GDPR Data Protection Impact Assessment (DPIA) processes where personal data is involved. | Must | BO-002, BO-006 |

### 7.2 Assessment Structure Requirements

| ID | Requirement | Priority | Traces to |
|---|---|---|---|
| **BR-005** | The business requires a consistent, repeatable structure for conducting AI impact assessments across different systems and assessors. | Must | BO-001, BO-003 |
| **BR-006** | The business requires impacts to be evaluated using a standardised scoring method that produces comparable results across assessments. | Must | BO-001 |
| **BR-007** | The business requires an overall impact rating to be derived from individual impact findings to support a single deployment decision. | Must | BO-004 |
| **BR-008** | The business requires the ability to define post-deployment monitoring requirements as part of the assessment outcome. | Should | BO-001, BO-005 |
| **BR-009** | The business requires the ability to identify conditions that would trigger a new or repeated assessment for an existing system. | Should | BO-001, BO-003 |

### 7.3 Decision and Accountability Requirements

| ID | Requirement | Priority | Traces to |
|---|---|---|---|
| **BR-010** | The business requires a formal, recorded deployment decision (approved, conditional, or not approved) for each assessed system. | Must | BO-004, BO-005 |
| **BR-011** | The business requires named accountability for system ownership, technical review, compliance review, and final governance approval. | Must | BO-004, BO-005, BO-006 |
| **BR-012** | The business requires the ability to record formal acceptance of residual risk by an accountable system owner. | Must | BO-004, BO-005 |

### 7.4 Data and Record-Keeping Requirements

| ID | Requirement | Priority | Traces to |
|---|---|---|---|
| **BR-013** | The business requires the ability to produce a complete, exportable record of each assessment for audit and regulatory purposes | Must | BO-005 |
| **BR-014** | The business requires the ability to save and resume an in-progress assessment without loss of data | Should | BO-001, BO-003 |
| **BR-015** | The business requires assessment data to remain under the organisation's control, without third-party storage or transmission | Must | CO-001, BO-005 |

### 7.5 Usability Requirements

| ID | Requirement | Priority | Traces to |
|---|---|---|---|
| **BR-016** | The business requires the assessment process to be usable by individuals without specialist technical or legal training, supported by clear guidance | Should | BO-001, BO-006 |
| **BR-017** | The business requires the tool to be accessible without installation or organisational procurement overhead, to support adoption | Should | BO-003 |

---

## 8. Stakeholder Requirements

Stakeholder requirements describe the specific needs of individual stakeholder groups identified in Section 3. Each stakeholder requirement is derived from one or more business requirements but reflects the particular perspective and responsibility of the stakeholder concerned. Stakeholder requirements form the bridge between organisational business requirements and the detailed functional requirements to be defined in the FRD.

| ID | Stakeholder | Requirement | Traces to |
|---|---|---|---|
| **SR-001** | AI Governance Lead / Business Analyst | Needs the ability to co-ordinate a multi-section assessment over time, including pausing and resuming work. | BR-005, BR-014 |
| **SR-002** | System Owner | Needs a clear summary of identified impacts and their severity before being asked to accept residual risk. | BR-007, BR-012 |
| **SR-003** | System Owner | Needs visibility into which conditions must be satisfied before a conditionally approved system can be deployed | BR-010 |
| **SR-004** | Data Protection Officer | Needs a clear signal within the assessment of whether a DPIA is required, to avoid duplicated or missed data protection review | BR-004 |
| **SR-005** | Data Protection Officer | Needs to understand which aspects of the assessment fall within DPIA scope versus broader AI governance scope | BR-004 |
| **SR-006** | Legal / Compliance Reviewer | Needs assurance that the EU AI Act risk classification selected for a system is consistent with the system description provided | BR-001, BR-002 |
| **SR-007** | Legal / Compliance Reviewer | Needs the ability to review the complete regulatory mapping for a given assessment without cross-referencing external documents | BR-002 |
| **SR-008** | AI Ethics Board | Needs a consolidated view of overall impact rating, deployment recommendation, and outstanding conditions to make a single governance decision | BR-007, BR-010 |
| **SR-009** | End Users (Assessors) | Need the ability to complete an assessment without losing entered data due to accidental navigation or browser closure | BR-014 |
| **SR-010** | End Users (Assessors) | Need sufficient guidance on regulatory terminology to complete the assessment without requiring constant external reference | BR-016 |
| **SR-011** | IT Security | Needs confirmation that no assessment data, including data relating to vulnerable individuals, is transmitted to or stored on third-party servers | BR-015 |

---

## 9. High-Level Acceptance Criteria

The following high-level criteria define, from an organisational perspective, the conditions that must be met to confirm that each group of business requirements has been successfully satisfied. These criteria establish the baseline for business sign-off; granular, testable acceptance criteria are defined per functional requirement within the FRD.

| ID | Requirement Group | High-Level Acceptance Criteria |
|---|---|---|
| **AC-001** | **Regulatory Compliance (BR-001 to BR-004)** | A completed assessment clearly states the system's EU AI Act risk classification, references applicable ISO/IEC 42001:2023 and GDPR provisions, and flags unacceptable risk systems for escalation |
| **AC-002** | **Assessment Structure (BR-005 to BR-009)** | Two different assessors completing assessments for comparable systems produce consistent scoring outcomes using the same evaluation criteria |
| **AC-003** | **Decision and Accountability (BR-010 to BR-012)** | Every completed assessment contains a named deployment decision, named accountable roles, and an explicit residual risk acceptance statement |
| **AC-004** | **Data and Record-Keeping (BR-013 to BR-015)** | A completed assessment can be exported, stored externally, and re-imported without loss of information; no assessment data leaves the user's device other than through explicit export |
| **AC-005** | **Usability (BR-016 to BR-017)** | A first-time user with no prior exposure to the tool can complete an assessment using only in-tool guidance, without external training |

---

## 10. Traceability Matrix

This matrix demonstrates bidirectional traceability across the entire business lifecycle. It ensures that every business requirement (**BR**) and stakeholder requirement (**SR**) can be mapped directly back to a defined business objective (**BO**), guaranteeing that no requirement is introduced without explicit organisational justification.

| Business Objective | Business Requirement(s) | Stakeholder Requirement(s) | Primary Stakeholder(s) |
|---|---|---|---|
| **BO-001** — Structured, auditable assessment | BR-005, BR-006, BR-008, BR-009, BR-014, BR-016 | SR-001, SR-009, SR-010 | AI Governance Lead, End Users |
| **BO-002** — Compliance readiness | BR-001, BR-002, BR-003, BR-004 | SR-004, SR-005, SR-006, SR-007 | DPO, Legal/Compliance |
| **BO-003** — Reduce ad hoc practices | BR-005, BR-009, BR-017 | SR-001 | AI Governance Lead, End Users |
| **BO-004** — Inform decision-makers | BR-007, BR-010, BR-011, BR-012 | SR-002, SR-003, SR-008 | System Owner, AI Ethics Board |
| **BO-005** — Defensible audit trail | BR-002, BR-008, BR-011, BR-012, BR-013, BR-015 | SR-002, SR-007, SR-008, SR-011 | Legal/Compliance, IT Security |
| **BO-006** — Cross-functional collaboration | BR-004, BR-011, BR-016 | SR-004, SR-005 | DPO, multiple stakeholders |

---

## 11. Glossary Reference

For definitions of regulatory and technical terms used throughout this document (including AI Ethics Board, DPIA, EU AI Act risk classifications, Material Change, and others), refer to the Glossary section of the AISIA Functional Documentation.

---

*AISIA Business Requirements Document v1.0 | Dorota Wasiak | AI Governance Portfolio | June 2026*
*Related: [01-business-case.md](01-business-case.md) | Functional Requirements Document (forthcoming)*
