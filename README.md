# Project Spec

## Project Name
Repo-Mind (name pending...)

## Product Statement
A local-first AI data engineering platform that ingests repositories, understands SQL and engineering logic, and enables grounded chat, search, and analysis through a web UI.

## Problem Statement
Data and analytics repositories are difficult to understand, especially when SQL logic is spread across many files, dialects, and layers. Documentation is often incomplete, onboarding is slow, and impact analysis is manual.

## Target Audience
- Data Engineers
- Technical Analysts
- New team members onboarding into complex repos
- Analytics Engineers

## MVP Goals
- Ingest a local repository
- Identify and process SQL files
- Store documents and chunks
- Enable semantic search
- Support chat with citations
- Show file path and line references in the UI

## Non-Goals
- Enterprise auth
- Perfect lineage
- Full dbt manifest integration
- Cloud deployment
- Direct writeback to databases
- Full support for every language in v1

## Success Criteria
- A user can ingest a repo successfully
- A user can search for SQL logic and find relevant files
- A user can ask questions and receive grounded answers with citations
- A user can inspect the source file and line range from the UI

## Planned Stack
- FastAPI
- Next.js
- PostgreSQL
- Qdrant
- Docker
- Python
- TypeScript

## Status
Project setup and architecture in progress.