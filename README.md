# Carvio

> Personalized job & internship alert system with scraping, filtering, and skill-based matching.

**Live Demo:** https://trycarvio.vercel.app/

---

## Table of Contents

- [Philosophy](#philosophy)
- [System Architecture](#system-architecture)
- [Repositories](#repositories)
  - [Frontend — carvio-client](#frontend--carvio-client)
  - [Backend — carvio-server](#backend--carvio-server)
- [Design Principles](#design-principles)
- [Key Highlights](#key-highlights)
- [Future Scope](#future-scope)
- [Why Carvio?](#why-carvio)
- [Author](#author)
- [Note](#note)

---

## Philosophy

Carvio is built on one idea: the biggest bottleneck in job hunting isn't applying — it's filtering.

Most job seekers spend more time deciding what to ignore than actually applying. Switching platforms, scanning irrelevant listings, and manually filtering roles is repetitive work that a system should handle.

Carvio automates discovery by aggregating and filtering opportunities so users can focus entirely on applying — not searching.

---

## System Architecture

```
Client (Next.js)
        ↓
REST API (Node.js)
        ↓
Job Processing Layer (Cron + Scrapers)
        ↓
Data Normalization & Deduplication
        ↓
Database (MongoDB)
        ↓
Filtering & Matching Engine

```

Carvio is designed as a **pipeline-driven backend system** that automates job ingestion and filtering, reducing manual effort in job discovery.

---

## Repositories

### Frontend — carvio-client

https://github.com/me-prakhargupta/carvio-client

- Next.js (App Router)
- TypeScript
- Tailwind CSS
- Minimal UI

---

### Backend — carvio-server

https://github.com/me-prakhargupta/carvio-server

- Node.js (TypeScript)
- Automated job ingestion and filtering pipeline
- Cron-based background processing
- Handles core data flow: `scraping → normalization → storage → delivery`

---

## Design Principles

- **Pipeline-First Architecture**  
  The system is designed as a continuous data pipeline  
  `ingestion → normalization → storage → matching → delivery`

- **Signal over Noise**  
  Prioritize relevance, not volume  
  Only high-quality, filtered opportunities should reach the user

- **Automation over Manual Effort**  
  Replace repetitive user actions (searching, filtering) with backend automation  
  Shift from user-driven search → system-driven discovery

- **Backend-Driven Personalization**  
  Personalization happens at the backend layer, not UI hacks  
  Matching engine decides relevance before data reaches user

---

## Key Highlights

- Automated job aggregation across 32+ companies and 11+ domains
- Cron-based scraping and pipeline-driven backend architecture
- Data normalization, deduplication, and relevance filtering
- Designed to reduce search time and improve application efficiency

---

## Future Scope

- Advanced Matching Engine
- Real-Time Alerts
- Multi-platform job aggregation
- Smart Deduplication & Ranking
- Resume-Based Matching

---

## Why Carvio?

Carvio was built to solve a simple problem: **finding the right opportunities takes more time than applying**.

It automates job discovery by aggregating and filtering listings from platforms like **Greenhouse** and **Internshala**.

> The goal is to reduce noise and help users focus on applying, not searching.

---

## Author

**Prakhar Gupta**  
Full-Stack Developer (Next.js, Node.js, TypeScript)  
Focused on building backend-driven, production-grade web applications.

---

## Note

This repository serves as the **central entry point** for the Carvio system, linking all services and providing architectural context.
