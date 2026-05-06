# AI Business Plan Generator

Enterprise-grade AI Business Plan Operating System.

This project is not just a business plan writer.  
It is a structured AI-powered platform designed to:

- collect business intelligence
- normalize business data
- manage evidence
- refine business assumptions
- orchestrate AI reasoning
- generate investor/bank/USCIS-grade business plans

---

# Core Vision

The platform transforms fragmented business information into:

```txt
Structured Business Intelligence
→ AI Refinement
→ Evidence Validation
→ Multi-Agent Reasoning
→ Professional Business Plans
```

The system is designed for:

- startups
- franchises
- E2 / USCIS immigration business plans
- SBA/bank-ready plans
- investor-ready plans
- service businesses
- local businesses
- expansion projects

---

# Current Architecture

## 1. Intake & Data Collection Layer

### Enterprise Intake Template

Supports:

- Excel
- CSV
- Google Forms
- Microsoft Forms

Architecture:

```txt
question
→ canonical field
→ structured answer
→ project intelligence
```

Each question includes:

- help text
- examples
- required level
- audience targeting
- business type targeting

---

## 2. Canonical Field Registry

Central structured business ontology.

### Features

- canonical field keys
- aliases
- normalization
- project metadata mapping
- required field logic
- business-type requirements
- audience-specific requirements

Example:

```txt
company_name
business_name
legal_name
→ company_legal_name
```

Supports:

- franchises
- restaurants
- local services
- retail
- USCIS/E2
- startups

---

## 3. Intelligent Import Engine

Structured import pipeline.

### Import Flow

```txt
Excel / CSV / Forms
→ field normalization
→ alias mapping
→ canonical fields
→ project_answers
```

### Features

- fuzzy field mapping
- project metadata extraction
- registry fallback mapping
- intelligent section routing
- safe ingestion
- QA-friendly import review

---

## 4. Project Intelligence Layer

All business intelligence is stored as:

```txt
project_answers
```

instead of large unstructured text blobs.

This allows:

- granular AI refinement
- field-level validation
- conflict detection
- adaptive generation
- structured scoring

---

## 5. AI Refinement Loop Engine

Iterative AI-driven improvement system.

### Workflow

```txt
project_answers
→ consolidation
→ scoring
→ weakest section detection
→ refinement
→ reconsolidation
→ rescoring
```

### Features

- safe reconsolidation
- weakest-section refinement
- AI-driven improvements
- iterative optimization
- controlled loops

---

## 6. Intelligent Consolidation Engine

Transforms structured answers into professional business plan sections.

### Characteristics

- no direct hallucinated generation
- structured synthesis
- section-safe generation
- field-aware generation
- context-aware writing

---

## 7. AI Task System

Background AI orchestration system.

### Features

- async tasks
- live task state
- generation tracking
- refinement monitoring
- safe status visibility

---

## 8. Scoring Engine

Business plan evaluation engine.

### Features

- section scoring
- overall scoring
- readiness level
- critical issue detection
- next-step recommendations

### Planned Enhancements

- industry-aware scoring
- financial realism scoring
- evidence-weighted scoring
- business consistency scoring

---

## 9. RAG Evidence Engine

The RAG system is designed as an:

```txt
Evidence Layer
```

NOT a direct writing engine.

### Philosophy

RAG NEVER writes directly into business plan sections.

Workflow:

```txt
evidence
→ field proposal
→ review
→ apply to project_answers
→ reconsolidation
```

### Features

- evidence registry
- source reliability scoring
- evidence proposals
- conflict detection
- citation foundation
- structured evidence governance

### Supported Evidence Types

- franchise documents
- supplier documents
- technical sheets
- FDD documents
- market reports
- official sources
- regulatory sources
- lease information
- financial evidence

---

## 10. Conflict Detection Engine

Detects inconsistencies across business data.

Examples:

```txt
industry = bakery
services = cleaning
→ inconsistency flag
```

Planned:

- cross-section validation
- financial realism validation
- operational realism validation
- industry coherence checks

---

## 11. Evidence Governance System

Future architecture:

```txt
upload
→ classify
→ extract evidence
→ map to fields
→ generate proposals
→ review
→ apply
```

### Planned Document Types

- business_plan_model
- supplier_document
- franchise_document
- technical_sheet
- legal_document
- official_source
- market_source

### Allowed Use Policies

- style_only
- structure_only
- evidence_only
- field_proposal_only
- legal_context_only

---

# Frontend Architecture

Frontend stack:

- Next.js
- React
- TypeScript

### Main Panels

- Project List
- Questionnaire Panel
- AI Task Panel
- Refinement Loop Controller
- Score Panel
- Field Proposal Review
- RAG Evidence Engine
- Consolidation Controls

---

# Backend Architecture

Backend stack:

- FastAPI
- PostgreSQL
- SQLAlchemy
- Ollama / local LLM support

### Core Services

- intake_import
- intelligent_consolidation
- refinement_loop
- field_registry
- rag_evidence_engine
- scoring_engine
- ai_task_manager

---

# Design Philosophy

The system is intentionally:

```txt
local-first
single-user
AI-intelligence-focused
non-SaaS
```

Priority is:

- intelligence quality
- business realism
- structured reasoning
- evidence integrity
- iterative refinement

NOT:

- multi-tenant scaling
- user management
- SaaS infrastructure

---

# Current Development Status

Implemented:

- structured intake engine
- canonical field registry
- intelligent import system
- AI refinement loops
- scoring engine
- RAG evidence registry
- conflict detection foundation
- AI task orchestration
- section consolidation
- safe reconsolidation

In Progress:

- adaptive intake system
- business consistency validator
- advanced scoring
- proposal review workflows
- evidence mapping improvements

Planned:

- multi-agent reasoning engine
- advanced RAG evidence extraction
- financial realism engine
- adaptive questionnaires
- citation-aware generation
- investor-grade financial validation
- USCIS-grade evidence workflows

---

# Future Roadmap

## Iteration 8

### Multi-Agent Evidence Reasoning Engine

Architecture:

```txt
RAG evidence
→ specialized agents
→ debate
→ confidence scoring
→ structured recommendations
→ field proposals
```

---

# Example System Workflow

```txt
Client Questionnaire
→ Import
→ Canonical Mapping
→ project_answers
→ AI Consolidation
→ Scoring
→ Weakness Detection
→ Refinement Loops
→ Evidence Enrichment
→ Final Business Plan
```

---

# Long-Term Goal

Build an AI-powered:

```txt
Business Intelligence Operating System
```

capable of producing:

- investor-grade plans
- USCIS-grade plans
- SBA-ready plans
- operational business intelligence
- structured business reasoning
- explainable AI business analysis

instead of simple AI-generated text.
