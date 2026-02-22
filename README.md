# PhyloAI FinRegOS
### Agentic Regulatory Compliance Intelligence Suite
**By Aether Software Solutions Pvt. Ltd.**

> Submitted to the **IndiaAI Financial Reporting Compliance Challenge** in partnership with the National Financial Reporting Authority (NFRA), February 2026.

---

## Overview

**PhyloAI FinRegOS** is a purpose-built agentic AI platform that automates financial reporting compliance validation, analytics, and regulatory intelligence for NFRA and India's broader financial oversight ecosystem.

It is developed by **Aether Software Solutions Pvt. Ltd.** — an Indian technology company with 11 years of experience building custom ERP systems and financial operations platforms for MSMEs across restaurants, retail chains, and property management. **PhyloAI** is Aether's AI product line: agentic financial intelligence systems built ground-up from deep domain knowledge, not retrofitted from generic AI tools.

---

## The Problem

India's financial reporting ecosystem requires simultaneous compliance across six regulatory frameworks:

| Framework | Body |
|-----------|------|
| IndAS Vol 1 & 2 + Auditing Standards | ICAI / MCA |
| Schedule III — Financial Statement Preparation | MCA |
| Disclosure Requirements | SEBI |
| Disclosure Norms for Financial Institutions | RBI |
| ESG Framework | SEBI |
| ESG Disclosures — BRSR Core | SEBI |

Manual review at scale is infeasible. PhyloAI FinRegOS replaces it with an explainable, auditable, agentic system.

---

## Solution Modules

### 1. Compliance Validation Engine
Automated extraction and provision-level validation of financial reports against all six frameworks. Every determination is traceable to a specific provision, document section, and reasoning chain.

### 2. Automated Analytics Engine
Agentic financial performance analysis — risk scoring, governance structure review, audit history — drawing on structured ERP data and unstructured filings.

### 3. Preliminary Examination Tool
Real-time monitoring of enforcement actions, news, legal cases, and whistle-blower signals. Entity resolution links external signals to NFRA's filing database automatically.

### 4. NFRA Insight Bot
RAG-powered conversational assistant over NFRA's document corpus. Supports compliance analysis, precedent retrieval, and audit finding search in English and Hindi, with strict on-premise confidentiality controls.

---

## System Architecture

```
┌─────────────────────────────────────────────────────────────────┐
│                    ① DATA INGESTION LAYER                       │
│  PDF/XBRL Parser · OCR Engine · ERP Connectors · Reg Feed APIs  │
└──────────────────────────────┬──────────────────────────────────┘
                               ↓
┌─────────────────────────────────────────────────────────────────┐
│                 ② DOCUMENT INTELLIGENCE LAYER                   │
│   Section Segmentation · Financial NER · Table Reconstructor    │
│                      Metadata Tagger                            │
└──────────────────────────────┬──────────────────────────────────┘
                               ↓
┌─────────────────────────────────────────────────────────────────┐
│               ③ REGULATORY KNOWLEDGE GRAPH (Neo4j)              │
│   IndAS · Schedule III · SEBI · RBI · SEBI ESG · BRSR Core      │
│         Provision-level nodes · Version-controlled              │
└──────────────────────────────┬──────────────────────────────────┘
                               ↓
┌─────────────────────────────────────────────────────────────────┐
│           ④ AGENT ORCHESTRATION LAYER (LangGraph)               │
│                    ┌─ Central Planner ─┐                        │
│                    ↓                   ↓                        │
│   Compliance Agent · Analytics Agent                            │
│   Signal Monitoring Agent · Insight Bot Agent                   │
└──────────────────────────────┬──────────────────────────────────┘
                               ↓
┌─────────────────────────────────────────────────────────────────┐
│                ⑤ VECTOR STORE & RAG LAYER                       │
│     Qdrant · Hybrid Retrieval (semantic + BM25) · Llama 3       │
│              GPT-4o / Gemini (non-sensitive tasks)              │
└──────────────────────────────┬──────────────────────────────────┘
                               ↓
┌─────────────────────────────────────────────────────────────────┐
│                      ⑥ OUTPUT LAYER                             │
│  Compliance Reports · Analytics Dashboard · Examination Reports │
│                    NFRA Insight Bot UI                          │
└─────────────────────────────────────────────────────────────────┘

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
      ⑦ SECURITY & GOVERNANCE LAYER  (Horizontal — all layers)
   On-Premise · AES-256 · TLS 1.3 · RBAC · DPDP Act 2023 · ISO 27001
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

## Technology Stack

| Component | Technology |
|-----------|------------|
| Agent Orchestration | LangGraph (in-house framework) |
| Primary LLM (on-premise) | Llama 3 (Meta, Apache 2.0) |
| LLM APIs (non-sensitive) | OpenAI GPT-4o · Google Gemini |
| Vector Store | Qdrant (Apache 2.0) |
| Knowledge Graph | Neo4j Community (GPL v3) |
| Document Parsing | In-house pipeline + OCR |
| ERP Connectors | Aether-built (11 years production) |
| Retrieval | Hybrid semantic + BM25 |

---

## Why Aether + PhyloAI

| Dimension | Our Approach |
|-----------|-------------|
| **Domain depth** | 11 years building financial systems for Indian MSMEs — we understand the data at its source |
| **CA partnerships** | Long-standing collaboration with Practising CAs — compliance logic is practitioner-validated |
| **ERP integration** | Production-tested connectors built in-house, not third-party dependencies |
| **Indian regulatory context** | IndAS, Schedule III, SEBI LODR, RBI Master Directions embedded in our institutional knowledge |
| **Data sovereignty** | Fully on-premise deployable — no sensitive data leaves NFRA's infrastructure |
| **Explainability** | Every determination traceable to provision + source document + agent reasoning chain |

---

## Responsible AI

- **Interpretability:** All agent decisions include source citations and reasoning chains
- **Auditability:** Immutable logs of every agent action, query, and data access event
- **Fairness:** No demographic or identity data used in compliance analysis
- **Human oversight:** Low-confidence outputs routed to human review; no suppression of uncertainty
- **Data protection:** Aligned with DPDP Act 2023, MeitY guidelines, and ISO 27001 principles
- **Regulatory alignment:** Consistent with NITI Aayog's Responsible AI for All framework

---

## Data Sources

All training and validation data is sourced exclusively from public domain, government-published material:

- MCA21 annual filings
- BSE / NSE disclosed financial statements (FY2018–FY2024)
- NFRA public inspection reports and orders
- SEBI enforcement orders
- Official regulatory texts: IndAS Vol 1 & 2, Schedule III, SEBI circulars, RBI Master Directions, BRSR guidelines

No proprietary client data from Aether's MSME deployments is used.

---

## Security & Deployment

- **Deployment:** On-premise, private cloud, or hybrid — NFRA-controlled infrastructure
- **Encryption:** AES-256 at rest · TLS 1.3 in transit
- **Access control:** Role-based (RBAC) with immutable audit logs
- **Data residency:** Zero egress; air-gapped deployment available
- **Compliance:** DPDP Act 2023 · ISO 27001 · MeitY cloud security guidelines
- **Key management:** Encryption keys remain within NFRA's own infrastructure

---

## About Aether Software Solutions

Aether Software Solutions Pvt. Ltd. is an Indian technology company founded over 11 years ago. We have built and deployed custom ERP systems, POS platforms, property management systems, and financial operations tools for clients across restaurants, retail chains, and real estate.

Our close collaboration with Practising Chartered Accountants has given us deep, first-hand knowledge of compliance workflows, audit documentation standards, and statutory reporting obligations. PhyloAI is the AI product line born from this domain knowledge — agentic financial intelligence built from the ground up, not adapted from generic tools.

---

## Contact

**Aether Software Solutions Pvt. Ltd.**
📧 pankaj@phylo-ai.com
🌐 phylo-ai.com

---

*This repository contains architecture and solution documentation submitted as part of the IndiaAI Financial Reporting Compliance Challenge (February 2026). Core implementation code is maintained in a private repository.*
