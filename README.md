# Enterprise Data Governance Sandbox: End-to-End Asset Lineage & Data Quality in Microsoft Purview

**Author:** Ogbonnaya Nzie Ezichi — [LinkedIn]() · [GitHub]() · [Google Scholar]()

---

### 📌 Project Executive Summary
This project demonstrates an enterprise-grade execution of modern **Data Governance, Asset Lineage, and Metadata Management** utilizing the **Microsoft Purview Unified Catalog**. 

Built to simulate the data challenges faced by strictly regulated industries (Banking and Healthcare), this sandbox moves past theoretical frameworks to deploy real-world implementations. The project is split into a **Two-Phase Governance Lifecycle Framework** designed to stress-test Purview’s behavioral object model—specifically evaluating the structural relationship between **Domains, Data Products, Data Assets, Business Glossaries, and Automated Classification Engines**.

### 🗂️ Strategic Architecture: The Two-Phase Lifecycle



## Phase 1 — Synthetic data, first pass at the object model

[`case-study-phase-1-synthetic.md`](case-study-phase-1-synthetic.md)

A single placeholder patient-discharge row, used to learn Purview's basic shape: Data Map vs. Unified Catalog, where business metadata attaches versus technical metadata, and Draft/Published as an actual governance gate rather than cosmetic status. Surfaces a likely false-positive classification (a diagnosis code auto-tagged as a personal health identifier) and a self-corrected misdiagnosis along the way. Explicitly scoped as a toy case — no realistic data, no access policy, no data quality rules.

## Phase 2 — Real CIHI data, at actual scale

[`case-study-phase-2-real-cihi-data.md`](case-study-phase-2-real-cihi-data.md)

A real, published Canadian Institute for Health Information table (injury/trauma emergency department hospitalizations), taken through a documented raw-to-curated pipeline — encoding fixes, suppression handling, validation against CIHI's own published totals — then registered in Purview. Surfaces three real platform issues at real scale: a silent resource-set misdetection bug that broke schema parsing, an intentional raw-layer schema limitation documented rather than engineered around, and a reproducible defect in the asset-level glossary-term linking picker, diagnosed with elimination evidence and resolved by linking at the data-product layer instead — a legitimate path through Purview's own object model, not a workaround.

## Why two phases

Phase 1 answered "how does the object model fit together" with a toy input designed to be predictable. Phase 2 answers the harder question — what actually happens when the input is a real government publication with real structural mess (a title row, an embedded footer, statistical suppression, non-UTF-8 encoding) — and treats every platform surprise as something to diagnose with evidence, not something to route around silently. Read together, they're meant to show the same habit applied twice: don't trust an assumption about how a vendor's tool behaves until you've tested it.
