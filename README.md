# Enterprise Data Governance Sandbox: End-to-End Asset Lineage & Data Quality in Microsoft Purview

**Author:** Ogbonnaya Nzie Ezichi — [LinkedIn]() · [GitHub]() · [Google Scholar]()

---

### 📌 Project Executive Summary
This project demonstrates an enterprise-grade execution of modern **Data Governance, Asset Lineage, and Metadata Management** utilizing the **Microsoft Purview Unified Catalog**. 

Built to simulate the data challenges faced by strictly regulated industries (Banking and Healthcare), this sandbox moves past theoretical frameworks to deploy real-world implementations. The project is split into a **Two-Phase Governance Lifecycle Framework** designed to stress-test Purview’s behavioral object model—specifically evaluating the structural relationship between **Domains, Data Products, Data Assets, Business Glossaries, and Automated Classification Engines**.

### 🗂️ Strategic Architecture: The Two-Phase Lifecycle
 


## Phase 1 — Synthetic data, first pass at the object model

[`case-study-phase-1-synthetic.md`](case-study-phase-1-synthetic.md)

#### 🛡️ Phase 1 — Technical Framework & Metadata Triage
* **Core Focus:** Establishing structural mechanics and auditing Purview’s default scanning behavior.
* **The Environment:** Utilized a strategic placeholder dataset to isolate the behavioral boundaries between the **Data Map** (technical metadata metadata) and the **Unified Catalog** (business context layer).
* **Key Governance Win:** Successfully intercepted a **false-positive PII classification** where an automated Purview scan incorrectly tagged an *ICD-10-CA medical diagnosis code* as an immutable personal health identifier. 
* **The Impact:** Proved that automated governance platforms require structural semantic validation to maintain high-integrity business glossaries.
* **Deep-Dive Case Study:** [Read Phase 1 Report](case-study-phase-1-synthetic.md)

## Phase 2 — Real CIHI data, at actual scale

[`case-study-phase-2-real-cihi-data.md`](case-study-phase-2-real-cihi-data.md)

A#### 📈 Phase 2 — Production-Scale Ingestion & Platform Troubleshooting
* **Core Focus:** Scaling the framework using real, public-health institutional data from the **Canadian Institute for Health Information (CIHI)** covering injury and trauma emergency department hospitalizations.
* **The Pipeline Environment:** Implemented a raw-to-curated ETL data pipeline, executing critical data quality checks across multiple operational layers (resolving non-UTF-8 encoding issues, managing statistical data suppression, and extracting embedded footers). 
* **Data Lineage Validation:** Validated the reshaped data assets against CIHI’s published regional control totals across all 14 jurisdictions to guarantee zero data drift before Purview registration.
* **Deep-Dive Case Study:** [Read Phase 2 Report](case-study-phase-2-real-cihi-data.md)


### 🔍 Production Platform Breakthroughs & Issue Resolution
When deploying data governance at scale, platform anomalies routinely disrupt metadata scanning. This project highlights a data-driven, evidence-based approach to diagnosing and fixing three critical Microsoft Purview system bugs:

1. **The Silent Schema-Parsing Failure (Resource-Set Bug):** Identified and root-caused a platform anomaly where Purview misdetected incoming files as a consolidated resource-set, silently breaking individual schema parsing. Documented and resolved the issue by overriding default parsing behavior using Purview's underlying object model.
2. **Asset-Level Glossary Linking Defect:** Diagnosed a reproducible defect within the Purview asset-level UI picker that dropped explicit glossary-term linkages. Isolated the bug through comparative evidence and resolved it by rerouting the linkage mechanism directly through the **Data-Product layer**—ensuring absolute metadata inheritance without relying on unstable workarounds.
3. **Raw-Layer Schema Limitations:** Documented intentional cloud-storage raw schema limitations, providing a clear architecture map for downstream data stewards rather than engineering brittle, un-auditable local workarounds.

---

### 💡 Core Governance Competencies Demonstrated
* **Enterprise Architecture Mapping:** Practical application of **DAMA-DMBOK2** core dimensions (Data Quality, Metadata Management, and Data Lineage) in a modern Azure cloud environment.
* **Regulatory Readiness:** Demonstrating how to build a unified data asset fabric that satisfies modern privacy and audit requirements (**PIPEDA, BCBS 239**).
* **Vendor & Platform Expertise:** Moving past abstract software definitions to showcase genuine, production-level expertise in configuring, debugging, and maintaining **Microsoft Purview** environments.
