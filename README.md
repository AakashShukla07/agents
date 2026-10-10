# Enterprise Multi-Agent Systems (Dify.ai Workflows)

Production-grade, parallel multi-agent architectures engineered for enterprise risk automation and telemetry triage. Built with deterministic Python execution engines, domain-specific worker swarms, and auditable operational workflows.

---

## Repository Contents

* **`LegalOps Contract Risk & Redline Auditor.yml`** — Autonomous contract analysis and negotiation drafting workflow.
* **`Autonomous SOC Threat Triage & Incident Responder.yml`** — Real-time cybersecurity incident triage and containment runbook generator.

Both architectures implement parallel worker swarms combined with deterministic Python code nodes to eliminate hallucinations and produce auditable outputs.

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
```

### Key Capabilities
* **Parallel Specialist Swarm:** Evaluates financial liability caps, GDPR/SOC 2 compliance windows, and IP ownership simultaneously.
* **Deterministic Risk Scoring:** Computes an objective index ($0\text{–}100$) using Python rather than relying on unstructured LLM estimates.
* **Redline Negotiation Matrix:** Generates side-by-side contract counter-proposals with defensible business rationales ready for procurement teams.

---

## 2. Autonomous SOC Threat Triage & Incident Responder

Real-time SecOps alert investigation pipeline that processes raw SIEM telemetry, isolates forensic Indicators of Compromise (IoCs), assesses exploitation severity, maps attack tactics to the MITRE ATT&CK matrix, and produces Tier-1 through Tier-3 containment runbooks.

### Architecture

```text
                  [User Input: Raw SIEM Alert & Environment Tier]
                                         │
                             [LLM: IoC Extractor]
                      (IPs, Hashes, Parent PIDs, Commands)
                                         │
                 ┌───────────────────────┴───────────────────────┐
                 │                                               │
   [Sub-Agent A: Network Threat                     [Sub-Agent B: Identity & Host
        Intelligence Analyst]                             Compromise Auditor]
  (C2 Beaconing, Tor Egress, Shodan)              (LSASS Injections, LOLBins, IAM)
                 │                                               │
                 └───────────────────────┬───────────────────────┘
                                         │
                           [Code Node: Python Engine]
                     Threat Index = (0.50*Net) + (0.50*Host)
                                         │
                         [LLM: Incident Commander]
                   (MITRE ATT&CK Mapping & Runbook Dispatch)
                                         │
                             [Output: Forensic Dossier]
```

### Key Capabilities
* **Forensic IoC Extraction:** Automatically parses IP addresses, malicious domains, parent-child processes, and base64 commands from unstructured logs.
* **Dual-Track Triage:** Audits network beaconing anomalies and host privilege escalations in parallel.
* **MITRE ATT&CK Alignment:** Maps observed behaviors directly to standardized technique IDs (e.g., T1003 Credential Dumping, T1059 Command Execution).
* **Automated Containment Runbook:** Generates operational steps for immediate host quarantine, firewall drop rules, and identity session invalidation.

---

## How to Import into Dify

1. Download either `.yml` file from this repository.
2. Log in to [Dify.ai](https://cloud.dify.ai).
3. In **Studio**, click **Create from Blank** $\rightarrow$ select **Import DSL file**.
4. Upload the downloaded file to immediately launch and run the workflow canvas.
