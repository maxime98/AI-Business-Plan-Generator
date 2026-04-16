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
