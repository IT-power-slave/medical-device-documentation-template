# 001 — Template Foundation

## Document Control
- **Document ID:** 001
- **Area:** 00-governance
- **Title:** Template Foundation
- **Status:** Draft
- **Owner:** Repository Maintainer
- **Reviewers:** Quality / Regulatory / System Architecture representatives
- **Version:** 0.1.0
- **Last Updated:** 2026-06-03

---

## 1. Purpose

This document defines the foundational assumptions, boundaries, structure, and governance rules for the repository **`medical-device-documentation-template`**.

The repository provides a **baseline documentation framework** for medical software projects and medical systems that may:
- operate as standalone medical software,
- cooperate with medical or non-medical hardware devices,
- run on desktop, mobile, cloud, edge, or mixed environments,
- communicate locally or remotely,
- include multilingual and region-specific behavior,
- include AI-supported development processes and/or AI-related product functions.

This document is intended to ensure that all future template documents are created in a **consistent, modular, traceable, and certification-oriented** way.

---

## 2. Repository Objective

The objective of this repository is to provide a reusable, adaptable, and certification-oriented **documentation starting point** for projects involving:
- software with a medical purpose,
- software influencing or driving the use of a medical device,
- software cooperating with external devices,
- telemedicine and remote monitoring solutions,
- connected and IoT-enabled medical systems,
- multilingual and multi-region medical software products,
- products developed with controlled use of AI.

The repository is designed as **EU-first, FDA-ready**:
- **EU-first** means that the baseline structure is aligned primarily to European medical device documentation needs under MDR/IVDR-oriented software projects. MDR establishes the framework for placing medical devices on the EU market, including conformity assessment and post-market obligations. [1](https://eur-lex.europa.eu/eli/reg/2017/745/oj/eng)[2](https://eur-lex.europa.eu/legal-content/EN/LSU/?uri=CELEX%3A32017R0745)
- **FDA-ready** means that the structure should be extensible so that software documentation and cybersecurity documentation can be augmented for U.S. submissions when needed. FDA provides dedicated guidance for device software functions and separate cybersecurity premarket documentation expectations. [3](https://www.fda.gov/regulatory-information/search-fda-guidance-documents/content-premarket-submissions-device-software-functions)[4](https://www.fda.gov/regulatory-information/search-fda-guidance-documents/cybersecurity-medical-devices-quality-management-system-considerations-and-content-premarket)

---

## 3. Scope

### 3.1 In Scope

This template framework supports documentation for systems such as:
- **Medical Device Software (MDSW)** and software functions that may qualify as medical devices depending on intended purpose. Qualification and classification of software depend strongly on the manufacturer-defined intended purpose. [5](https://health.ec.europa.eu/document/download/b45335c5-1679-4c71-a91c-fc7a4d37f12b_en?filename=mdcg_2019_11_en.pdf)[1](https://eur-lex.europa.eu/eli/reg/2017/745/oj/eng)
- **Software operating on general computing platforms**, including desktop, mobile, cloud, and other platforms. MDCG guidance explicitly covers apps and software operating on mobile phones, in the cloud, or on other platforms. [5](https://health.ec.europa.eu/document/download/b45335c5-1679-4c71-a91c-fc7a4d37f12b_en?filename=mdcg_2019_11_en.pdf)
- **Health software products** placed on the market without dedicated hardware, including lifecycle concerns such as design, validation, installation, maintenance, and disposal. IEC 82304-1 addresses health software on general computing platforms across the full lifecycle. [6](https://www.iso.org/standard/59543.html)
- **Software cooperating with devices**, including software that drives or influences the use of a device, software accessories, and software interacting with external sensors, instruments, or connected systems. MDCG guidance explicitly addresses software driving or influencing the use of a device and software accessories. [5](https://health.ec.europa.eu/document/download/b45335c5-1679-4c71-a91c-fc7a4d37f12b_en?filename=mdcg_2019_11_en.pdf)
- **Remote, connected, and telemedicine-related systems**, including communication systems and home-care or remote monitoring scenarios. MDCG guidance includes telemedicine systems and home-care monitoring examples. [5](https://health.ec.europa.eu/document/download/b45335c5-1679-4c71-a91c-fc7a4d37f12b_en?filename=mdcg_2019_11_en.pdf)
- **Cybersecurity-relevant medical software**, especially where communication, remote access, interoperable interfaces, or field updates are present. FDA’s cybersecurity guidance and FDA recognition of IEC 81001-5-1 confirm that secure lifecycle activities are relevant for medical software products. [4](https://www.fda.gov/regulatory-information/search-fda-guidance-documents/cybersecurity-medical-devices-quality-management-system-considerations-and-content-premarket)[7](https://www.accessdata.fda.gov/scripts/cdrh/cfdocs/cfStandards/detail.cfm?standard__identification_no=43889)
- **AI-related systems**, including systems that contain AI components or are subject to AI-specific obligations in addition to sectoral medical device requirements. The EU AI Act establishes harmonized rules for AI systems, including high-risk use contexts, and is intended to complement existing sectoral regulation. [8](https://eur-lex.europa.eu/eli/reg/2024/1689/oj/eng)

### 3.2 Out of Scope

This repository does **not** provide:
- legal advice,
- binding regulatory interpretation,
- product-specific classification decisions,
- notified body strategy,
- clinical strategy for a specific product,
- market-specific submission packages as complete and final deliverables,
- replacement for a formal QMS,
- replacement for expert regulatory, clinical, cybersecurity, privacy, or usability review.

This repository provides **templates and structure**, not certification by itself.

---

## 4. Foundational Principles

The repository shall follow these principles:

1. **Modularity**  
   The framework shall consist of a mandatory **core** and optional **add-ons** so that projects can adopt only the documents relevant to their product type, deployment model, and regulatory profile.

2. **Traceability**  
   All critical artifacts should be linkable across the lifecycle: intended purpose, claims, requirements, architecture, risks, controls, tests, evidence, release decisions, and post-market inputs.

3. **Product Perspective**  
   Documentation shall describe the **whole product lifecycle**, not only source code. IEC 82304-1 covers design, development, validation, installation, maintenance, and disposal of health software products. [6](https://www.iso.org/standard/59543.html)

4. **Intended Purpose First**  
   The intended purpose shall drive scope, qualification, classification, requirements, validation strategy, and claims. MDCG emphasizes that a clear intended purpose is essential for qualification, classification, and compliance of MDSW. [5](https://health.ec.europa.eu/document/download/b45335c5-1679-4c71-a91c-fc7a4d37f12b_en?filename=mdcg_2019_11_en.pdf)

5. **Platform-Neutral Qualification Logic**  
   Software shall not be documented as non-medical or low-impact merely because it runs in cloud, on mobile, or on a general-purpose platform. MDCG explicitly notes that qualification depends on intended purpose regardless of location or platform. [5](https://health.ec.europa.eu/document/download/b45335c5-1679-4c71-a91c-fc7a4d37f12b_en?filename=mdcg_2019_11_en.pdf)

6. **Security by Design**  
   Cybersecurity shall be addressed from the beginning of the lifecycle, not as a late-stage annex. FDA’s current cybersecurity guidance expects design, labeling, and premarket documentation to address cybersecurity risk. [4](https://www.fda.gov/regulatory-information/search-fda-guidance-documents/cybersecurity-medical-devices-quality-management-system-considerations-and-content-premarket)

7. **AI as a Cross-Cutting Concern**  
   AI-related functionality shall be documented through dedicated governance, validation, change control, and monitoring mechanisms where applicable. The EU AI Act introduces obligations that may coexist with medical device requirements. [8](https://eur-lex.europa.eu/eli/reg/2024/1689/oj/eng)

8. **Localization as a Safety Concern**  
   Multilingual and regional differences shall be treated as controlled product behavior where they influence usability, interpretation, warnings, clinical content, or safe operation.

9. **Evidence-Oriented Structure**  
   The template shall make it easier to demonstrate compliance, design rationale, test coverage, and decision history.

---

## 5. Supported Product and Solution Categories

The template is intended to support documentation for one or more of the following categories:

### 5.1 Product Categories
- Standalone medical software
- Software as part of a medical system
- Software accessory to a device
- Software driving or influencing a device
- Remote monitoring solution
- Telemedicine solution
- Mobile medical application
- Desktop clinical software
- Health software product on general platforms
- Hybrid local/cloud medical solution

### 5.2 Platform Categories
- Windows
- Linux
- macOS
- Android
- iOS
- Cloud-hosted environments
- Edge or gateway environments
- Mixed-platform systems

### 5.3 Connectivity Categories
- Wired communication
- Wireless communication
- Local network communication
- Internet-based communication
- Remote / telemedicine communication
- IoT communication patterns
- Intermittent / degraded connectivity scenarios

### 5.4 AI Categories
- AI used in the development process
- AI used in verification, analysis, or quality activities
- AI included in product functionality
- AI influencing recommendations, outputs, prioritization, or decisions

### 5.5 Localization Categories
- Single-language product
- Multi-language product
- Multi-region product
- Region-configurable product
- Product with market-specific content or restrictions

---

## 6. Documentation Architecture

The repository shall be organized into:
- **Core documents** — expected for most projects,
- **Add-on documents** — applied only when relevant,
- **Records and logs** — evidence of execution and decisions,
- **Traceability artifacts** — linking requirements, risks, design, tests, and evidence.

### 6.1 Core Documents
Core documents are expected to include at least:
- Documentation Plan
- Intended Purpose / Intended Use
- Product Scope and System Context
- Regulatory Profile and Classification Rationale
- Requirements Specification
- Architecture Description
- Risk Management Plan
- Verification and Validation Plan
- Traceability Matrix

### 6.2 Add-On Documents
Add-on documents may include:
- Device Interoperability Addendum
- Connectivity and Communication Addendum
- Telemedicine / Remote Operation Addendum
- Mobile Platform Addendum
- Cloud / Hosting Addendum
- AI Governance Addendum
- Cybersecurity Addendum
- Localization and Regionalization Addendum
- Post-Market Operations Addendum

### 6.3 Records and Logs
Records and logs may include:
- design decision logs,
- change assessment records,
- risk review records,
- test execution records,
- localization verification records,
- AI change records,
- release approval records,
- incident and CAPA-related records.

---

## 7. Regulatory Orientation

This repository is structured to remain compatible with documentation needs commonly associated with:
- EU MDR/IVDR-oriented software projects, including software qualification/classification logic and conformity-related evidence expectations. MDR defines the EU medical device framework, and MDCG 2019-11 Rev.1 provides software-specific guidance for qualification and classification under MDR/IVDR. [1](https://eur-lex.europa.eu/eli/reg/2017/745/oj/eng)[5](https://health.ec.europa.eu/document/download/b45335c5-1679-4c71-a91c-fc7a4d37f12b_en?filename=mdcg_2019_11_en.pdf)
- Health software product lifecycle expectations reflected in IEC 82304-1. IEC 82304-1 applies to health software products on general computing platforms and covers lifecycle activities from design through disposal. [6](https://www.iso.org/standard/59543.html)
- FDA documentation expectations for device software functions. FDA’s 2023 guidance describes recommended documentation for premarket submissions involving device software functions. [3](https://www.fda.gov/regulatory-information/search-fda-guidance-documents/content-premarket-submissions-device-software-functions)
- FDA cybersecurity expectations for devices with cybersecurity risk. FDA’s February 2026 cybersecurity guidance addresses design, labeling, and recommended premarket cybersecurity documentation. [4](https://www.fda.gov/regulatory-information/search-fda-guidance-documents/cybersecurity-medical-devices-quality-management-system-considerations-and-content-premarket)
- Secure lifecycle practices for health software, including IEC 81001-5-1. FDA recognizes IEC 81001-5-1 for health software and health IT security lifecycle activities, while also clarifying that additional FDA cybersecurity expectations may still apply. [7](https://www.accessdata.fda.gov/scripts/cdrh/cfdocs/cfStandards/detail.cfm?standard__identification_no=43889)
- Additional AI-related obligations where AI functionality is in scope. The EU AI Act establishes harmonized AI rules and is intended to complement existing Union law, including sectoral product legislation. [8](https://eur-lex.europa.eu/eli/reg/2024/1689/oj/eng)

This repository shall therefore be maintained so that project teams can:
- start with a common baseline,
- add market-specific layers when needed,
- keep evidence aligned across regulations and standards,
- avoid mixing product-neutral templates with product-specific decisions.

---

## 8. Traceability Policy

The template shall support traceability across the following artifact chain:

**Intended Purpose / Claims**  
→ **Regulatory Qualification / Classification Rationale**  
→ **User / System / Safety / Security Requirements**  
→ **Architecture and Design Decisions**  
→ **Hazards, Hazardous Situations, Harms, Risks, and Controls**  
→ **Verification and Validation Activities**  
→ **Objective Evidence / Records**  
→ **Release Decision**  
→ **Post-Market Feedback and Change Control**

### 8.1 Minimum Traceability Expectations
At minimum, each project using this template should be able to trace:
- each major product claim to supporting requirements and evidence,
- each safety- or security-relevant requirement to verification,
- each risk control to implementation and verification evidence,
- each product variant or regional variant to its governing configuration source,
- each AI-specific control to validation and monitoring evidence where applicable.

---

## 9. Document Status Model

Each document in the repository shall use one of the following statuses:
- **Draft** — actively being prepared
- **In Review** — under formal review
- **Approved** — accepted for use
- **Released** — frozen for a defined repository release or baseline
- **Obsolete** — superseded and no longer to be used
- **Template Only** — generic pattern not yet instantiated for a specific project

If needed, project repositories derived from this template may refine the status model, but shall preserve the meaning of these baseline states.

---

## 10. Versioning Rules

### 10.1 Repository Versioning
The repository should use semantic-style versioning for template releases where practical:
- **Major** — incompatible structural changes
- **Minor** — new documents, new sections, or significant template extension
- **Patch** — editorial fixes, corrections, formatting improvements, minor clarifications

### 10.2 Document Versioning
Each template document should contain:
- version,
- status,
- last updated date,
- owner,
- change summary where relevant.

### 10.3 Change Management
Any meaningful change to a template shall consider impact on:
- linked documents,
- traceability references,
- regulatory mappings,
- optional add-ons,
- downstream project repositories using the template.

---

## 11. Roles and Responsibilities

### 11.1 Repository Maintainer
Responsible for:
- maintaining structure and consistency,
- approving template-level changes,
- managing naming and governance rules,
- ensuring cross-document coherence.

### 11.2 Quality / Regulatory Reviewer
Responsible for:
- reviewing regulatory alignment,
- checking terminology consistency,
- identifying missing compliance-related artifacts,
- reviewing change impact on certification-oriented use.

### 11.3 System / Software Architect Reviewer
Responsible for:
- validating architectural completeness,
- reviewing system boundary assumptions,
- checking interface and communication documentation needs.

### 11.4 Security Reviewer
Responsible for:
- ensuring cybersecurity-related sections and templates are adequate for connected and remotely accessible products.

### 11.5 AI Governance Reviewer
Responsible for:
- assessing whether AI-specific controls, records, and validation expectations are covered where applicable.

---

## 12. Naming and Numbering Rules

### 12.1 Directory Prefixes
Top-level directories shall use numeric prefixes to preserve navigation order, for example:
- `00-governance`
- `01-scope-and-intended-purpose`
- `02-regulatory-and-classification`

### 12.2 Document Numbering
Documents should use the format:

`NNN-short-kebab-case-title.md`

Examples:
- `001-template-foundation.md`
- `002-document-control-rules.md`
- `010-intended-purpose-template.md`

### 12.3 Language Rule
The canonical language of this repository shall be **English**.

If local-language working notes are ever created, they shall:
- not replace canonical English artifacts,
- be clearly marked as non-authoritative unless explicitly approved,
- remain traceable to the canonical English source.

---

## 13. AI Usage Policy for This Repository

This repository may be developed with AI assistance, but AI assistance shall not replace:
- accountable authorship,
- expert review,
- regulatory judgement,
- architecture decisions,
- risk acceptance decisions,
- approval authority.

Where AI is used to generate or revise documentation:
- the output should be reviewed by a human owner,
- factual and regulatory claims should be verified,
- repository decisions should remain attributable to named maintainers,
- project teams should define whether AI-assisted content generation must be logged.

This rule exists because AI may assist drafting, but regulated documentation still requires controlled review and accountable ownership.

---

## 14. Localization and Regionalization Policy

Localization and regionalization shall be treated as controlled product dimensions when they affect:
- user interface meaning,
- safety messaging,
- warnings and contraindications,
- units, date/time formats, or numeric conventions,
- user workflows,
- market-restricted functionality,
- legally required content,
- support, deployment, or maintenance instructions.

Projects using this template should therefore define, where relevant:
- supported languages,
- supported regions / markets,
- translation ownership,
- verification rules for safety-critical text,
- configuration rules for market-specific differences.

---

## 15. Connectivity and Device Cooperation Policy

Projects using this template shall document device cooperation and communication behavior when relevant, including:
- device and system boundaries,
- interface contracts,
- communication mechanisms,
- loss-of-connection behavior,
- degraded operation modes,
- data integrity checks,
- synchronization assumptions,
- update and compatibility assumptions,
- remote operation constraints.

This is particularly important for connected, remote, and home-care scenarios, which are explicitly reflected in software guidance examples for telemedicine and home monitoring. [5](https://health.ec.europa.eu/document/download/b45335c5-1679-4c71-a91c-fc7a4d37f12b_en?filename=mdcg_2019_11_en.pdf)

---

## 16. Initial Repository Structure

The initial target structure of the repository is:

```text
medical-device-documentation-template/
├── 00-governance/
├── 01-scope-and-intended-purpose/
├── 02-regulatory-and-classification/
├── 03-requirements/
├── 04-architecture/
├── 05-interfaces-and-communication/
├── 06-risk-management/
├── 07-usability/
├── 08-ai-governance/
├── 09-cybersecurity/
├── 10-verification-and-validation/
├── 11-localization-and-regionalization/
├── 12-deployment-and-release/
├── 13-post-market/
├── 14-traceability/
├── templates/
└── README.md