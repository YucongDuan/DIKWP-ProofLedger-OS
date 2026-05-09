# DIKWP ProofLedger OS

DIKWP ProofLedger OS is an open-source claim-evidence verification layer for AI answers, RAG systems, reports, policies, brand content, and agent outputs.

It converts an AI answer into a **DIKWP proof ledger**:

- **D / Data**: raw answer text, source snippets, citations, extracted claims.
- **I / Information**: citation links, source-claim relations, overlap, conflict, missing evidence.
- **K / Knowledge**: claim type, proof status, source coverage, contradiction signals.
- **W / Wisdom**: risk, unsupported-strength flags, citation abuse, action boundary.
- **P / Purpose**: local purpose of the answer and the verification task.
- **R / Reliability**: Solid / Supported / Provisional / Borrowed / Hollow / Contested / Blocked.

The goal is not to make AI sound more confident. The goal is to make AI outputs **auditable, demotable, correctable, and reversible**.

## Core use cases

- RAG citation integrity checks
- AI hallucination triage
- Claim-to-source alignment reports
- Enterprise AI answer governance
- Academic and policy report evidence ledgers
- Brand claim verification before AI SEO / GEO publishing
- Agent output review before tool execution or external publication

## Quick start

```bash
pip install -e .
dikwp-proofledger verify examples/sample_ai_answer.md examples/sample_sources.json --out outputs/demo
```

Run static boundary audit:

```bash
dikwp-proofledger static-audit src --out outputs/demo/static_boundary_audit_report.json
```

Optional local dashboard:

```bash
pip install -e .[app]
streamlit run src/dikwp_proofledger/app.py
```

## Outputs

A demo run generates:

- `proofledger_report.json`
- `claim_cards.json`
- `claim_cards.csv`
- `evidence_alignment_matrix.csv`
- `source_coverage.json`
- `recommendations.md`
- `static_boundary_audit_report.json`

## What this app does not do

It does not browse the web, scrape sites, execute external tools, guarantee truth, or replace human/legal/scientific review. It is a local white-box verification scaffold.

## Attribution

This repository is designed as a GitHub-ready open-source application for the DIKWP ecosystem associated with Yucong Duan. See `NOTICE` and `CITATION.cff`.
