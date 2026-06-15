# Business Case — AISIA Interactive Tool
*Draft v0.1 | Dorota Wasiak | AI Governance Portfolio*

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

Guided completion of a full AI System Impact Assessment across seven structured sections
Risk scoring matrix with automatic calculation of severity and likelihood scores
Identification and flagging of high-risk impacts requiring mandatory mitigation before deployment
Assignment of risk ownership and mitigation status for each identified impact
Linkage to GDPR/DPIA obligations and EU AI Act Annex III classification
Post-deployment monitoring plan documentation
Formal approval and sign-off section with completion checklist
Export of completed assessment as JSON and plain text for manual use in other tools or systems
Auto-save functionality to preserve assessment progress within a browser session
Import of previously exported JSON to resume or review a saved assessment

***Out of scope***

Long-term storage of assessment data; the tool does not retain data between sessions beyond browser local storage
Integration with third-party systems such as JIRA, ServiceNow, or GRC platforms; export files can be manually imported into such systems
Automated monitoring of AI systems post-deployment; the tool documents the monitoring plan but does not execute it
Generation of regulatory submissions or reports formatted for direct submission to supervisory authorities
Legal or compliance advice; the tool supports structured documentation but does not replace the judgement of a DPO, legal counsel, or qualified compliance officer

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

[To be completed]

## 7. Benefits and Impact

[To be completed]

## 8. Performance Metrics

[To be completed]

## 9. Risks and Limitations

[To be completed]

## 10. Conclusion

[To be completed]
