# Continuum Insight

**Enterprise data intelligence for people who work with real data every day.**

## Demo

🎥 [Watch the full demo video](https://www.loom.com/share/cd181448ee5042b688bafdba9fcdecb6)

---

## What it does

Continuum Insight is a fully packaged desktop application that takes large, messy, multi-format data files and turns them into clean, structured, queryable data in SQL Server — with no SQL knowledge required.

---

## Features

- **Diagnostics engine** — scans your batch of files before import and flags structural issues in plain language: missing headers, mixed delimiters, malformed rows. No cryptic error messages.
- **Smart import** — connects to any SQL Server instance, detects compatible schemas across files, and merges them into a single table on import with one click.
- **Type fixer** — automatically detects date and amount columns stored as text and converts them to proper SQL data types for filtering and calculation.
- **Coverage check** — shows row counts by month across your full date range, instantly revealing missing or suspicious periods in your data.
- **Natural language querying** — ask questions about your data in plain English. Only the schema is sent to AI — column names, data types, table structure. Your actual data never leaves your local environment. The generated SQL query is shown in full so you can validate, copy, and refine.

---

## Tech Stack

- **Frontend:** TypeScript, React, Tauri
- **Backend:** Python, FastAPI
- **Database:** SQL Server
- **AI:** Anthropic API (schema-only, privacy-conscious architecture)
- **Packaging:** Full installer with automatic updates

---

## Architecture

150+ modular files across a Python backend and TypeScript/React frontend. Tauri wraps the application into a native desktop experience with a full installer and automatic update delivery.

The AI integration is deliberately minimal — only database schemas are transmitted to the model. Raw data never leaves the local environment. This is a core design constraint, not an afterthought.

---

## Other Systems Built

This application is one of several production systems I've built independently:

- **Client deliverable report generation** — VBA system that produces fully formatted, client-ready Word and Excel outputs directly from raw working files, eliminating approximately 2 days of manual work per report cycle — now the team's standard operating procedure
- **Invoice automation platform** — modular Python/Playwright system processing thousands of invoices per day across multiple client portals, with retry logic and plug-and-play portal expansion
- **OCR pipeline** — production-grade extraction and validation of structured data from hundreds of invoices with full error handling
- **ETL infrastructure** — Python/SQL Server data processing pipeline including automated diagnostics, type normalization, file merging, and coverage analysis, used daily by a team of 15
- **Lead intelligence engine** — fully autonomous pipeline from multi-source SERP scraping through AI-powered scoring, Hunter.io enrichment, and LLM-personalized outreach
---

*Full codebase available upon request.*
