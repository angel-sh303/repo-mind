# Repository Structure

This document explains the directory layout for the **DataForge AI** project.

The project is organized as a **monorepo** containing backend services, frontend UI, infrastructure configuration, and documentation.

## Root Directory

| Path | Type | Purpose |
|---|---|---|
| `README.md` | File | Public-facing overview of the project |
| `PROJECT_SPEC.md` | File | Internal product specification |
| `.env.example` | File | Template for environment variables |
| `.gitignore` | File | Git ignore configuration |
| `apps/` | Folder | Contains application code |
| `docs/` | Folder | Project documentation |
| `infra/` | Folder | Infrastructure configuration |
| `scripts/` | Folder | Development scripts |
| `data/` | Folder | Local testing data |

## Applications

| Path | Type | Purpose |
|---|---|---|
| `apps/api/` | Folder | Python FastAPI backend |
| `apps/ui/` | Folder | Next.js frontend application |

## Backend (FastAPI)

| Path | Type | Purpose |
|---|---|---|
| `apps/api/Dockerfile` | File | Backend container configuration |
| `apps/api/requirements.txt` | File | Python dependencies |
| `apps/api/app/main.py` | File | FastAPI application entry point |

## Backend Core

| Path | Type | Purpose |
|---|---|---|
| `apps/api/app/core/config.py` | File | Environment configuration |
| `apps/api/app/core/database.py` | File | Database connection logic |
| `apps/api/app/core/models.py` | File | SQLAlchemy models |
| `apps/api/app/core/schemas.py` | File | Pydantic API schemas |

## API Routes

| Path | Type | Purpose |
|---|---|---|
| `apps/api/app/api/routes/` | Folder | API endpoint definitions |
| `apps/api/app/api/routes/health.py` | File | Health check endpoint |

## Database Layer

| Path | Type | Purpose |
|---|---|---|
| `apps/api/app/db/` | Folder | Database helpers and future migrations |

## Ingestion System

| Path | Type | Purpose |
|---|---|---|
| `apps/api/app/ingest/scanner.py` | File | Scans repositories and identifies files |
| `apps/api/app/ingest/router.py` | File | Routes files to parsing plugins |
| `apps/api/app/ingest/plugins/` | Folder | File parsing plugins |

## Ingestion Plugins

| Path | Type | Purpose |
|---|---|---|
| `apps/api/app/ingest/plugins/base.py` | File | Base plugin interface |
| `apps/api/app/ingest/plugins/sql.py` | File | SQL parsing and chunk extraction |
| `apps/api/app/ingest/plugins/text.py` | File | Generic text processing |
| `apps/api/app/ingest/plugins/markdown.py` | File | Markdown document parsing |

## RAG System (AI Layer)

| Path | Type | Purpose |
|---|---|---|
| `apps/api/app/rag/embeddings.py` | File | Generate vector embeddings |
| `apps/api/app/rag/retriever.py` | File | Retrieve relevant chunks |
| `apps/api/app/rag/llm.py` | File | Interface with language models |

## Services Layer

| Path | Type | Purpose |
|---|---|---|
| `apps/api/app/services/ingest_service.py` | File | Repository ingestion workflow |
| `apps/api/app/services/chat_service.py` | File | Chat orchestration |

## Utilities

| Path | Type | Purpose |
|---|---|---|
| `apps/api/app/utils/` | Folder | Shared helper utilities |

## Frontend (Next.js)

| Path | Type | Purpose |
|---|---|---|
| `apps/ui/Dockerfile` | File | Frontend container configuration |
| `apps/ui/package.json` | File | Node dependencies |

## Frontend Application

| Path | Type | Purpose |
|---|---|---|
| `apps/ui/app/layout.tsx` | File | Global UI layout |
| `apps/ui/app/page.tsx` | File | Main application page |

## Frontend Components

| Path | Type | Purpose |
|---|---|---|
| `apps/ui/components/Chat.tsx` | File | Chat interface |
| `apps/ui/components/Sources.tsx` | File | Citation viewer |
| `apps/ui/components/FileViewer.tsx` | File | File and code viewer |

## Frontend Utilities

| Path | Type | Purpose |
|---|---|---|
| `apps/ui/lib/api.ts` | File | API request helpers |
| `apps/ui/lib/types.ts` | File | Shared TypeScript types |

## Static Assets

| Path | Type | Purpose |
|---|---|---|
| `apps/ui/public/` | Folder | Static assets such as icons and images |

## Infrastructure

| Path | Type | Purpose |
|---|---|---|
| `infra/docker-compose.yml` | File | Docker Compose configuration for local development |

## Data Directory

| Path | Type | Purpose |
|---|---|---|
| `data/repos/` | Folder | Local repositories used for ingestion |
| `data/indexes/` | Folder | Local indexing artifacts |

## Scripts

| Path | Type | Purpose |
|---|---|---|
| `scripts/` | Folder | Utility scripts for development and maintenance |

## Documentation

| Path | Type | Purpose |
|---|---|---|
| `docs/architecture.md` | File | System architecture overview |
| `docs/roadmap.md` | File | Development roadmap |
| `docs/repository_structure.md` | File | Repository structure documentation |
| `docs/devlog/` | Folder | Development journal |

## Summary

| Layer | Location | Purpose |
|---|---|---|
| Backend API | `apps/api` | Ingestion, parsing, retrieval, and chat services |
| Frontend UI | `apps/ui` | Web interface for chat, search, and file viewing |
| Infrastructure | `infra` | Local container orchestration |
| Documentation | `docs` | Product, architecture, roadmap, and dev notes |
| Development Data | `data` | Local repos and index artifacts for testing |

This structure keeps the project clean, scalable, and easy to understand as it grows from a local development tool into a production-ready platform.