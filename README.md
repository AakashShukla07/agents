# Enterprise Multi-Agent Systems (Dify.ai Workflows)

Production-grade, parallel multi-agent architectures engineered for enterprise risk automation and telemetry triage. Built with deterministic Python execution engines, domain-specific worker swarms, and auditable operational workflows.

---

## Repository Overview

This repository contains exportable Dify DSL (`.yml`) workflow blueprints for two enterprise systems:

1. **LegalOps Contract Risk & Redline Auditor** (`LegalOps Contract Risk & Redline Auditor.yml`)
2. **Autonomous SOC Threat Triage & Incident Responder** (`Autonomous SOC Threat Triage & Incident Responder.yml`)

Both systems utilize **parallel multi-agent fan-out/fan-in patterns** and **deterministic scoring engines**, eliminating qualitative hallucinations and providing verifiable, repeatable outputs.

---

## 1. LegalOps Contract Risk & Redline Auditor

Autonomous contract governance workflow that evaluates vendor MSAs, SLAs, and SaaS agreements, computes a mathematically weighted liability score, and generates a structured counter-negotiation redline table.

### Architecture

```text
                  [User Input: Raw Contract & Risk Policy]
                                     │
                        [LLM: Clause Classifier]
                                     │
         ┌───────────────────────────┼───────────────────────────┐
         │                           │                           │
 [Sub-Agent A: Financial     [Sub-Agent B: Compliance     [Sub-Agent C: IP &
   & Liability Auditor]        & Privacy Auditor]          Commercial Lock-in]
 (Caps, Fees, Penalties)    (GDPR, SOC2, SLA Windows)     (Indemnity, Auto-Renew)
         │                           │                           │
         └───────────────────────────┬───────────────────────────┘
                                     │
                       [Code Node: Python Risk Engine]
                 Composite Score = (0.40*F) + (0.35*C) + (0.25*L)
                                     │
                        [LLM: Redline Drafter]
                   (Generates Clause Negotiation Matrix)
                                     │
                            [Output: Audit Dossier]
