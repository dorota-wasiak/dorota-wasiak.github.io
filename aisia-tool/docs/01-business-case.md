# Business Case - AISIA Interactive Tool
*v1.0 | Dorota Wasiak | AI Governance Portfolio*

## Table of Contents

1. [Executive Summary](#1-executive-summary)
2. [Background and Strategic Context](#2-background-and-strategic-context)
3. [Business Need](#3-business-need)
4. [Proposed Solution and Scope](#4-proposed-solution-and-scope)
5. [Security and Compliance Considerations](#5-security-and-compliance-considerations)
6. [Development Phases](#6-development-phases)
7. [Benefits and Impact](#7-benefits-and-impact)
8. [Performance Metrics](#8-performance-metrics)
9. [Risks and Limitations](#9-risks-and-limitations)
10. [Conclusion](#10-conclusion)


## 1. Executive Summary

The AISIA Interactive Tool is a structured assessment instrument designed to support organisations in evaluating AI systems before deployment. It addresses not only the potential benefits of AI adoption, but also the risks, harms, and broader impacts on all parties affected by the system, including those who may be harmed if the AI produces biased outputs or operates in an uncontrolled manner.

The tool is based on the requirements of ISO/IEC 42001:2023, Annex A.5, and is aligned with the obligations of the EU AI Act. It provides organisations with a governance framework that is grounded in internationally recognised standards, rather than internal assumptions.

Organisations using the tool are guided through a comprehensive process that ensures full alignment with EU AI Act requirements. This includes identifying and documenting all affected stakeholders, assessing each risk by severity and likelihood, assigning clear ownership and response procedures, and establishing monitoring mechanisms to track risk over time.

For high-risk AI systems under EU AI Act Annex III, the tool addresses additional obligations: ensuring that training data is anonymised, free from bias, and appropriately secured against unauthorised access; and implementing continuous output monitoring to verify that model performance does not degrade over time and that decisions remain grounded in objective data rather than bias.

The tool is designed for existing business roles, such as business owners, product owners, data protection officers and business process managers. It enables organisations to conduct structured AI impact assessments without the need for a dedicated AI officer or specialist governance expertise.

Organisations can gain documented evidence of due diligence, a clear audit trail for regulatory purposes and a structured basis for ongoing AI risk management by completing an AISIA assessment. This reduces their exposure to the legal, regulatory and reputational consequences of uncontrolled AI deployment.

## 2. Background and Strategic Context

Organisations across industries are accelerating AI adoption, integrating AI components into recruitment, customer service, forecasting, supply chain management and decision-support processes. However, the pace of deployment has consistently outpaced the development of governance frameworks to support it.

In practice, many organisations deploy AI tools without establishing mechanisms to monitor output quality, detect bias in model behaviour, or measure whether results remain reliable over time. Governance procedures for AI systems are frequently absent, not because organisations are unaware of the risks, but because the path to implementing them is unclear.

Several barriers contribute to this gap:

 - Capability gap – most organisations do not have dedicated AI governance expertise within their teams. Responsibility for AI oversight is often distributed across existing roles without clear ownership, structured processes, or appropriate tools.

 - Absence of accessible standards-based tools – while internationally recognised frameworks such as ISO/IEC 42001:2023 and the EU AI Act provide clear requirements, translating these into operational processes remains a significant challenge for organisations without specialist knowledge.

 - Limited awareness – many business stakeholders are not yet familiar with what structured AI governance requires in practice, or how it differs from general IT risk management.

 - Governance perceived as cost rather than investment – without a visible regulatory consequence or internal incident, AI governance is frequently deprioritised in favour of deployment speed and commercial objectives.

 - Absence of internal accountability – without a dedicated AI Officer or equivalent role, no single function holds formal responsibility for AI governance, which means the topic consistently falls below the threshold of organisational priority.

This context creates a clear and immediate need for structured, accessible tools that enable existing business roles to conduct meaningful AI impact assessments without requiring specialist expertise. Organisations that establish governance frameworks proactively will be significantly better positioned to adapt when regulatory obligations come into full effect, avoiding the cost and disruption of reactive compliance.


## 3. Business Need

Organisations deploying AI systems without a structured impact assessment process are exposed to consequences that extend well beyond regulatory non-compliance.

***Absence of audit trail and legal exposure***

Where an AI system influences decisions affecting individuals, such as recruitment, credit scoring, or access to services, organisations must be able to demonstrate on what basis those decisions were made. Without documented evidence of how the system was configured, what data it was trained on, and how outputs were monitored, organisations cannot conduct a meaningful investigation when a decision is challenged. In legal proceedings, the inability to produce this documentation significantly weakens the organisation's position and may be interpreted as evidence of negligence.

***Regulatory consequences***

EU AI Act obligations apply to both providers and deployers of AI systems. Organisations that cannot demonstrate compliance, including maintaining logs, conducting impact assessments, and implementing human oversight for high-risk systems, face significant financial penalties. The absence of governance documentation does not reduce liability; it compounds it.

***Reputational damage***

Incidents involving biased or unexplainable AI decisions attract public attention rapidly. Negative coverage and commentary spread quickly and have a lasting effect on organisational reputation, customer trust, and the ability to attract talent and partners. Reputational damage of this kind is difficult to quantify and harder to reverse than a regulatory fine.

***The cost of reactive compliance***

Organisations that delay governance investment until a regulatory deadline or incident forces action face significantly higher costs than those who establish frameworks proactively. Reactive compliance requires emergency resourcing, external consultants, and accelerated implementation under pressure, often while simultaneously managing an active investigation or public scrutiny.

***What structured impact assessment provides***

Organisations that conduct a structured AI impact assessment before deployment gain documented evidence of due diligence, a clear basis for investigating incidents, defined ownership of risks and mitigations, and an audit trail that demonstrates responsible AI governance. This positions them to respond to regulatory scrutiny, legal challenges, and public questions from a position of transparency rather than exposure.

## 4. Proposed Solution and Scope

***Solution overview***

The AISIA Interactive Tool is a browser-based assessment instrument that guides users through a structured, step-by-step evaluation of an AI system prior to deployment. The tool does not passively collect information; it actively prompts users to verify that all necessary inputs are in place, consider risks across multiple dimensions, identify and assign ownership for each risk, and reach an informed deployment decision supported by complete documentation.
The tool calculates a risk score for each identified impact based on severity and likelihood ratings provided by the assessor. It highlights which AI systems carry high risk and require additional attention, more granular metrics, and enhanced monitoring arrangements. The tool does not make deployment decisions on behalf of the organisation; it presents a structured evidence base that enables the responsible person signing off on the assessment to make an informed and documented decision.

***In scope***

 - Guided completion of a full AI System Impact Assessment across seven structured sections
 - Risk scoring matrix with automatic calculation of severity and likelihood scores
 - Identification and flagging of high-risk impacts requiring mandatory mitigation before deployment
 - Assignment of risk ownership and mitigation status for each identified impact
 - Linkage to GDPR/DPIA obligations and EU AI Act Annex III classification
 - Post-deployment monitoring plan documentation
 - Formal approval and sign-off section with completion checklist
 - Export of completed assessment as JSON and plain text for manual use in other tools or systems
 - Auto-save functionality to preserve assessment progress within a browser session
 - Import of previously exported JSON to resume or review a saved assessment

***Out of scope***

 - Long-term storage of assessment data; the tool does not retain data between sessions beyond browser local storage
 - Integration with third-party systems such as JIRA, ServiceNow, or GRC platforms; export files can be manually imported into such systems
 - Automated monitoring of AI systems post-deployment; the tool documents the monitoring plan but does not execute it
 - Generation of regulatory submissions or reports formatted for direct submission to supervisory authorities
 - Legal or compliance advice; the tool supports structured documentation but does not replace the judgement of a DPO, legal counsel, or qualified compliance officer

***Future development considerations***

API integration with GRC and project management platforms is identified as a potential future development, as is a dedicated PDF export function generating a formatted assessment report. Both are outside the scope of 
the current version.



## 5. Security and Compliance Considerations

The AISIA Interactive Tool is designed to support compliance with the following regulatory and standards requirements:

***EU AI Act***

The tool directly addresses the following obligations:

 - Article 9 – Risk management system: guides organisations through establishing and documenting a structured risk management process for high-risk AI systems, including identification, assessment, and mitigation of risks across multiple dimensions
 - Article 10 – Data governance: prompts documentation of training, validation and test data sources, quality assessment, and verification that data is free from bias and appropriately secured
 - Article 13 – Transparency and provision of information: requires that high-risk AI systems are sufficiently transparent to enable deployers to interpret outputs; the tool documents explainability measures and the basis on which the system produces decisions or recommendations
 - Article 14 – Human oversight: documents human-in-the-loop arrangements for high-risk systems, including designated oversight roles and escalation procedures
 - Article 17 – Quality management system: supports documentation of policies and procedures governing AI system deployment, monitoring, and incident response
 - Article 18 – Documentation retention: completed AISIA assessments constitute part of the technical documentation required to be retained for a minimum of 10 years by providers and 3 years by deployers of high-risk AI systems after the system is taken out of service
 - Article 72 – Confidentiality: completed AISIA documents contain sensitive organisational information and must be treated as confidential, with access restricted to authorised roles
 - Annex III – High-risk AI system classification: the tool guides users through classification of AI systems against Annex III categories to determine whether high-risk obligations apply

***ISO/IEC 42001:2023***

The tool is structured around the following Annex A.5 controls:

 - A.5.2 – AI system impact assessment: the tool operationalises the pre-deployment impact assessment requirement, guiding users through all required assessment dimensions
 - A.5.3 – AI system impact assessment review: the monitoring plan section documents scheduled review dates, material change triggers, and responsibilities for post-deployment review
 - A.5.4 – Documentation of AI system impacts: all identified impacts are documented with dimension, severity, likelihood, score, mitigation measure, owner and status
 - A.5.5 – Treatment of adverse impacts: the tool requires mitigation measures for all identified impacts and flags critical impacts requiring mandatory action before deployment is authorised

***GDPR – Article 35 – Data Protection Impact Assessment***

Where an AI system processes personal data and may pose a high risk to the rights and freedoms of individuals, a DPIA is required under GDPR Article 35. The tool includes a dedicated section linking the AISIA to the DPIA process, documenting whether a joint assessment has been conducted, the DPO review status, and the relationship between data protection scope and broader AI impact scope. The tool does not itself process personal data of individuals assessed by the AI system; however, it processes organisational data including system descriptions, risk owners, and governance structures, which should be handled in accordance with the organisation's data protection policy.


***Supporting frameworks***

The following standards provide broader context for the governance approach embedded in the tool:

 - ISO 31000 – Risk management: the impact scoring methodology applies general risk management principles of likelihood and consequence assessment consistent with ISO 31000
 - ISO/IEC 27001 – Information security: assessment outputs, including exported JSON and PDF files, contain sensitive organisational information and should be classified and handled in accordance with the organisation's information security policy
 - NIST AI Risk Management Framework: referenced as a complementary framework for organisations operating globally; while not a European regulatory requirement, NIST AI RMF provides additional risk categorisation and governance guidance consistent with the approach taken in AISIA


### Security considerations

***Data processed by the tool***

The AISIA tool processes sensitive organisational information including AI system descriptions, risk assessments, data governance arrangements, and named individuals in ownership and approval roles. This information should be treated as confidential throughout the assessment lifecycle.

***Access control***

Access to a completed AISIA assessment should be restricted to authorised roles only. Recommended access includes: System Owner, DPO and Legal/Compliance, AI Ethics Board or equivalent governance function, and internal or external auditors where required. Broad distribution of completed assessments is not recommended given the sensitivity of the information contained.
Local storage

The tool uses browser local storage to preserve assessment progress between sessions on the same device. Organisations should ensure that AISIA assessments are completed on dedicated corporate devices with individual user authentication. Upon completion and export, users should clear saved data using the built-in "Clear saved data" function to prevent residual data remaining accessible on shared or unattended devices. The tool does not currently implement automatic session clearance; this is a known limitation of the current version.

***Export and document management***

The tool produces two export formats:

JSON – working file for editing and reimporting; should be stored securely with access restricted to the assessment team and treated as a draft document
PDF with confidentiality watermark – final approved version for archiving, audit, and regulatory purposes; should be stored in the organisation's document management system with role-based access control

Exported files should not be stored on unmanaged personal devices, shared drives without access controls, or transmitted via unsecured channels. Retention of completed AISIA documents should comply with EU AI Act Article 18 requirements: minimum 10 years for providers of high-risk AI systems, minimum 3 years for deployers, measured from the date the system is taken out of service.
Future development

Integration with GRC platforms via API is identified as a future development that would eliminate local file export and provide centralised, access-controlled storage of assessment records with a full audit trail.

## 6. Development Phases

The AISIA Interactive Tool is developed iteratively, with each phase delivering a functional increment that builds on the previous version. This approach enables early validation of core assessment functionality before introducing integrations and advanced features.

| Phase | Version | Scope | Status |
|---|---|---|---|
| Phase 1 | v0.1 | Core assessment tool | Released |
| Phase 2 | v0.2 | PDF export with confidentiality watermark | Planned |
| Phase 3 | v0.3 | API integration with external GRC platforms | Future |
| Phase 4 | v0.4 | Internal documentation integration | Future |


### Phase 1 – v0.1 – Core assessment tool
The first release delivers a fully functional browser-based AISIA form covering all seven assessment sections defined by ISO/IEC 42001:2023 Annex A.5. The tool guides users through structured completion of all required fields, including dropdown selections for risk dimensions, severity and likelihood ratings, mitigation status, and approval sign-off.
Core functionality delivered in v0.1:

Seven-section guided assessment form with structured field validation
 - Risk scoring matrix with automatic severity × likelihood calculation
 - Automatic flagging of critical impacts requiring mandatory mitigation
 - Completion checklist with progress indicator
 - Auto-save via browser local storage to preserve session progress
 - Clear saved data function to remove residual data from shared devices
 - Export to JSON as working file for editing and reimporting
 - Export to plain text for manual use in external tools
 - Import from JSON to resume or review a previously saved assessment
 - Footer with portfolio attribution

---

### Phase 2 – v0.2 – PDF export with confidentiality watermark
The second release introduces a dedicated PDF export function generating a formatted assessment report marked as confidential. The PDF serves as the final approved version of the assessment for archiving, audit trail, and regulatory purposes.
Planned functionality in v0.2:

 - Export to PDF with confidentiality watermark including system name, assessment date, and classification marking
 - Formatted layout optimised for print and digital archiving
 - PDF suitable for manual import into external document management systems and GRC platforms

---

### Phase 3 – v0.3 – API integration with external systems
The third release introduces API connectivity enabling assessment outputs to be automatically transferred to external GRC and project management platforms, eliminating manual file handling and providing centralised, access-controlled storage of assessment records.
Planned functionality in v0.3:

 - API integration with GRC platforms such as ServiceNow, Archer, or equivalent
 - Automated transfer of completed assessment data to external systems
 - Elimination of local file export as primary output mechanism

---
<!-- 
### Phase 4 – v0.4 – Internal documentation integration
The fourth release extends integration to internal organisational documentation, enabling the tool to connect with existing governance artefacts and streamline the assessment process for organisations with established AI governance functions.
Planned functionality in v0.4:

Integration with internal documentation systems including DPIA records and risk metrics
Directory-based selection of responsible persons for assessment sign-off and mitigation ownership, replacing manual name entry
Linkage to organisational role directories to assign accountability across assessment stages
-->


## 7. Benefits and Impact

### ***Organisational benefits***

Organisations that implement AISIA as part of their AI deployment process can be confident that all necessary aspects of responsible AI governance have been addressed before a system goes live. The structured assessment process consolidates existing knowledge, identifies gaps and ensures that nothing critical is overlooked amid the complexity of a deployment project.

Instead of allowing governance knowledge and accountability to remain distributed across teams, AISIA centralises documentation in a single, traceable record. In response to a regulatory inquiry, legal challenge or internal incident, the organisation can immediately identify who is responsible for each element of the system, the decisions that have been made and the basis on which they were made, and the monitoring that is in place. This significantly reduces the time and reputational cost of responding to critical situations.

Organisations that proactively establish structured AI governance will outperform those that don't, in terms of both operational maturity and regulatory readiness. When future obligations come into full effect, organisations that have completed AISIA assessments will be able to demonstrate compliance immediately, rather than having to develop procedures at the last moment under pressure. This proactive approach signals process maturity to regulators, partners and the market, creating a genuine competitive advantage.

Under the EU AI Act, organisations that deploy non-compliant high-risk AI systems face fines of up to 3% of their global annual turnover or €15 million, whichever is higher. Penalties for prohibited AI practices reach 7% of global turnover or €35 million. These figures transform AI governance investment from an operational cost to a risk mitigation measure with clear, quantifiable financial justification.

### ***Benefits for assessment participants***

Business Owners, Product Owners, DPOs and others involved in the assessment process gain clarity and confidence that every stage of deployment, monitoring and incident response has been documented and assigned. Instead of relying on informal knowledge or assuming that others have addressed particular risks, each participant knows exactly who is responsible for which part of the process and who to contact for any deviations or incidents.

The tool clarifies governance by making ownership explicit and traceable. This protects both individuals and the organisation: when accountability is clearly documented, no single person is exposed to disproportionate liability in the event of an incident.

Demonstrating AI governance maturity also supports talent acquisition, as experienced professionals are increasingly evaluating prospective employers based on their responsible technology practices. In a competitive market, organisations that can demonstrate structured AI governance are better positioned to attract and retain senior talent.

### ***Benefits for individuals affected by AI systems***

Those whose data is processed, or whose access to services, employment or other opportunities is affected by an AI system, can benefit from the assurance that the system has been thoroughly evaluated before deployment. They can be confident that the organisation has verified the quality and integrity of the training data used, established mechanisms for human oversight and documented a process for investigating and explaining system outputs if necessary.

When questions arise about a decision influenced by AI, individuals interacting with an organisation that has completed an AISIA assessment can request an explanation and expect a structured, evidence-based response. They can trust that the system has been developed in accordance with the requirements of the EU AI Act and ISO governance standards, that their data is secure and is being handled responsibly, and that the organisation deploying the system is taking its obligations seriously.

Summarising, AISIA transforms AI governance from a compliance obligation into an operational capability that protects the organisation, empowers those responsible for AI systems and builds trust with those affected by them.

## 8. Performance Metrics

Success of the AISIA Interactive Tool is measured across two dimensions: 
the quality and completeness of the assessment process itself, and the 
governance outcomes achieved by organisations using the tool.

---

**Assessment completeness metrics**

| Metric | Target |
|---|---|
| All seven assessment sections completed before export | 100% of submitted assessments |
| Every identified impact has severity and likelihood scores assigned | 100% |
| Every critical impact (score ≥9) has a mitigation measure and named owner | 100% |
| Deployment recommendation recorded and signed off by System Owner | 100% |
| Monitoring plan completed with scheduled review date and named owner | 100% |
| DPIA linkage documented where personal data is processed | 100% of assessments involving personal data |

---

**Assessment lifecycle metrics**

| Metric | Target |
|---|---|
| AISIA assessment completed before every new AI system deployment | 100% |
| AISIA review conducted upon material change to existing system | 100% of material changes |
| Annual review completed within scheduled timeframe | 100% of deployed systems |

---

**Governance outcome metrics**

| Metric | Target |
|---|---|
| All affected parties identified - internal and external - before deployment | 100% of assessments |
| All high-risk systems classified against EU AI Act Annex III before deployment | 100% |
| Data governance documentation in place - training, validation and test data inventoried and quality-assessed | Confirmed for all high-risk systems |
| Logging and log retention policy implemented in accordance with EU AI Act Article 18 | Confirmed for all high-risk systems |
| Transparency and explainability measures documented for all AI system outputs | 100% of high-risk systems |
| Bias assessment completed confirming absence of discriminatory patterns across gender, race, origin and age | 100% of high-risk systems |
| Named accountability assigned for each risk, mitigation, and escalation path | 100% of identified risks |
| Post-deployment monitoring active and first review conducted within scheduled timeframe | Confirmed per assessment monitoring plan |

---

**Human oversight metrics**

| Metric | Target |
|---|---|
| Human oversight role named and confirmed for all high-risk systems | 100% |
| Override mechanism documented and tested before deployment | 100% of high-risk systems |

---

**Incident response readiness metrics**

| Metric | Target |
|---|---|
| Escalation path defined for all critical impacts | 100% |
| Incident response procedure documented and owner assigned | 100% of high-risk systems |
| Maximum response time defined for critical AI system deviation | Defined per system in monitoring plan |

---

**Audit readiness indicators**

An organisation using AISIA can demonstrate audit readiness when the 
following evidence is available:

- Completed and signed AISIA assessment document for each deployed AI system
- Data inventory documenting training, validation and test datasets with quality and bias assessment results
- Named owners for all risks, mitigations, and escalation procedures
- Log retention policy aligned with EU AI Act Article 18 requirements
- Transparency and explainability documentation for all high-risk system outputs
- Human oversight role confirmed and override mechanism tested for all high-risk systems
- Evidence that all affected parties - including individuals directly assessed by the AI system - have been identified and their rights considered
- Incident response procedure in place with defined response times for critical deviations
- Scheduled post-deployment review dates recorded and adhered to

## 9. Risks and Limitations

This section documents known risks to the successful adoption and use of the AISIA Interactive Tool, and structural limitations of the current version that users and organisations should understand before deployment.

---

## **Project and adoption risks**

### Risk 1: 

**Checkbox compliance**
The most significant adoption risk is that organisations complete the assessment mechanically to produce a document, without genuine consideration of the risks and impacts involved. The tool cannot technically prevent this; the quality of an AISIA assessment is directly dependent on the knowledge, honesty, and accountability of the people completing it. Mitigation relies on organisational culture, AI literacy, and clear assignment of personal accountability for each section of the assessment.

*Mitigation: AI literacy programme for all assessment participants; named accountability for each section; quality review by AI Ethics Board or equivalent before approval.*

### Risk 2: 

**Insufficient AI literacy among assessment participants**

EU AI Act Article 4 requires organisations to ensure that staff working with AI systems possess an appropriate level of AI literacy. Where Business Owners, Product Owners, or other assessment participants lack sufficient understanding of the AI system being assessed, the quality of risk identification and scoring will be compromised. Gaps in understanding lead to underestimated risks, missed impacts, and incomplete mitigation plans.

*Mitigation: mandatory AI literacy training before assessment participation; involvement of IT and Solution Architect to provide technical context; DPO and Legal review of completed assessment.*

### Risk 3: 

**Unidentified risks emerging post-deployment**

Despite thorough pre-deployment assessment, new risks may emerge after a system goes live - including risks that were not foreseeable at the time of the original assessment. A single AISIA assessment does not provide ongoing protection; it must be supplemented by active post-deployment monitoring and reviewed whenever a material change occurs or an unexpected incident is identified.

*Mitigation: post-deployment monitoring plan completed as part of Section 6 of the assessment; AISIA review triggered by material changes, incidents, or new regulatory guidance; annual scheduled review for all active high-risk systems.*

### Risk 4: 

**Regulatory and standards evolution**

The EU AI Act and ISO/IEC 42001:2023 are subject to amendment, supplementary guidance, and national implementation variations. Assessment questions, risk classifications, and compliance requirements embedded in the current version of the tool may become outdated as regulations evolve. Organisations must ensure that the tool is reviewed and updated in line with regulatory developments.

*Mitigation: designated owner responsible for monitoring regulatory changes and initiating tool updates; version history maintained in release notes; organisations using the tool should verify alignment with current regulatory requirements before each major assessment cycle.*

### Risk 5: 

**Retrospective assessment of existing systems**

EU AI Act Article 26 requires deployers of high-risk AI systems to ensure compliance even for systems deployed before the regulation came into full effect. Organisations that have not conducted an AISIA assessment for existing systems are exposed to regulatory risk. Retrospective assessments should be prioritised for all high-risk systems currently in production.

*Mitigation: organisations should conduct an AISIA assessment for all active high-risk AI systems regardless of deployment date; retrospective assessments should be treated with the same rigour as pre-deployment assessments.*

---

## **Technical limitations - current version**

### Limitation 1 

**Local storage vulnerability**

Assessment progress is saved in browser local storage. This data can be lost if the user clears browser cache, if organisational IT policies automatically clear browser data, or if the browser is updated or reinstalled. Users who have not exported a JSON file will lose all progress without warning.

*Known limitation of v0.1. Mitigation: users should export JSON regularly during long assessment sessions. A reminder to export before closing the session is identified as a v0.2 enhancement.*

### Limitation 2 

**No substantive validation of responses**

The tool validates that required fields are completed but does not validate whether responses are substantively correct or sufficient. A user may enter inadequate mitigation measures for a critical impact and the tool will accept the response. This means the quality of the assessment output is entirely dependent on the knowledge and diligence of the assessor.

*Known limitation of v0.1. Conditional validation logic - for example, blocking export when a critical impact has no documented mitigation - is identified as a v0.2 enhancement.*

### Limitation 3 

**Language**

The tool is available in English only. For organisations operating in non-English speaking environments, language may be a barrier to full comprehension of assessment questions and the implications of responses, particularly for business roles that do not work primarily in English.

*Known limitation of v0.1. Multilingual support is a potential future development.*

### Limitation 4 

**No server-side storage or access control**

Assessment data is stored in browser local storage and exported to local files. There is no server-side storage, user authentication, or role-based access control in the current version. Organisations are responsible for managing the security and access control of exported assessment files in accordance with their information security policy.

*Known limitation of v0.1. API integration with GRC platforms providing centralised, access-controlled storage is identified as a v0.3 development phase.*

## 10. Conclusion

AI systems, like all complex technical systems, require structured governance to remain trustworthy and fit for purpose over time. A system built without ongoing oversight, without the ability to introduce controlled changes, and without documented accountability will rapidly lose the trust of the people who depend on its outputs - regardless of how well it was built at the outset. The AISIA Interactive Tool exists to prevent exactly this: to ensure that organisations do not treat AI deployment as a one-time event, but as an ongoing responsibility.

The tool provides a structured, accessible, and standards-aligned process for evaluating AI systems before deployment and maintaining governance throughout their lifecycle. By guiding existing business roles through a comprehensive impact assessment - covering risk identification, stakeholder impact, data governance, human oversight, transparency, and regulatory compliance - AISIA transforms governance from an abstract obligation into a practical, documented, and auditable organisational capability.

The current version delivers core assessment functionality aligned with ISO/IEC 42001:2023 and EU AI Act requirements. Planned development phases will extend the tool with PDF export, API integration with GRC platforms, and enhanced validation logic - progressively closing the gap between assessment documentation and operational governance systems.

Organisations that invest in structured AI governance now will be better positioned to adapt as regulatory requirements evolve, to respond to incidents with confidence, and to build the kind of trust in their AI systems that makes those systems genuinely valuable - to the organisation, to the people who use them, and to the people they affect.

This project was developed as part of an AI Governance portfolio by a Senior Business Analyst with fifteen years of experience delivering digital and data solutions across automotive, logistics, supply chain, and healthcare sectors. It reflects a conviction that responsible AI governance is not a specialist function reserved for dedicated compliance teams - it is a core competency for every business and technology professional working with AI systems today.

Organisations seeking to establish or strengthen their AI governance capability are invited to use, adapt, and build upon the AISIA Interactive Tool as a starting point for their own assessment practice.
