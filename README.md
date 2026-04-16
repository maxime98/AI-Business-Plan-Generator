# AI Business Plan Generator

A self-hosted application for generating professional business plans section by section using AI.

## Overview

This project is designed as a structured business-plan production tool, not just a chatbot.

It allows you to:

- create and manage projects
- store project metadata
- generate business plan sections with AI
- improve sections with AI
- edit sections manually
- save and version sections
- prepare the foundation for guided interviews, completeness checks, and document export

The application is currently built with:

- **Next.js** frontend
- **FastAPI** backend
- **PostgreSQL** database
- **Ollama** for local AI generation
- **Docker Compose** for deployment
- **Synology NAS** as the hosting environment

---

## Current Features

### Project management

- Create project
- List projects
- Edit project settings:
  - name
  - industry
  - location
  - description
  - tone
  - style

### AI section workflow

- Generate business plan sections
- Improve previously generated sections
- Add extra instructions per section
- Edit section content manually
- Save section content to PostgreSQL
- Track section version and status

### UX improvements

- Animated GIF progress indicator during Generate and Improve
- Simulated percentage progress
- FastAPI health endpoints
- Ollama connectivity check endpoint

---

## Current Business Plan Sections

The current MVP includes these base sections:

- `executive_summary`
- `company_overview`
- `market_analysis`
- `competitive_analysis`
- `marketing_strategy`
- `operations_plan`
- `financial_plan`

This list is expected to evolve after analyzing a larger corpus of business plans.

---

## Writing Preferences

Each project can define writing preferences:

### Tone
- `professional`
- `formal`
- `persuasive`
- `investor_ready`
- `concise`

### Style
- `classic`
- `consulting`
- `startup`
- `bank_ready`

These are injected into the prompts used by the AI.

---

## Architecture

```text
Frontend -> Backend -> PostgreSQL
                  -> Ollama
                  -> NAS storage


/volume1/docker/bpgenerator
├── docker-compose.yml
├── frontend
│   ├── app
│   ├── public
│   │   └── pic.gif
│   └── ...
├── backend
│   ├── app
│   │   └── main.py
│   └── ...
└── docs
    └── project notes / handoff files

```
## API Summary
Health
GET /
GET /health
GET /health/ollama
GET /sections
Projects
POST /projects
GET /projects
GET /projects/{project_id}
PUT /projects/{project_id}
Sections
POST /projects/{project_id}/generate-section
POST /projects/{project_id}/improve-section
PUT /projects/{project_id}/sections/{section_key}
Database Schema
projects

## Fields:

id
name
industry
location
description
tone
style
created_at
project_sections

## Fields:

id
project_id
section_key
content
status
version
updated_at

There is a unique logical constraint on:

(project_id, section_key)
## Prompt Strategy

The backend uses:

section-specific prompt instructions
project context
project writing preferences (tone, style)
optional extra user instructions

There are two main AI workflows:

Generate

Writes a new section from project context.

Improve

Takes an existing section and improves it for:

clarity
professionalism
credibility
investor readiness
Progress Indicator

The UI currently includes a progress indicator with:

animated GIF (walk.gif)
percentage text
action label (Generating..., Improving...)

This progress is currently simulated on the frontend, not driven by backend job status.

Ollama Health Check

The backend exposes an Ollama connectivity endpoint:

GET /health/ollama

This can be used from FastAPI docs to confirm:

Ollama is reachable
the configured URL is correct
the selected model is configured
Product Direction

## This project is intended to evolve into a complete business-plan production system.

## Planned directions include:

master section model
guided interview / questionnaire system
completeness checker
DOCX/PDF export
file upload and source ingestion
RAG
multi-agent review workflows
local persistent memory for advanced agents
