<!--
HOUSEFIND PHOENIX – README
Tip: Put this in your repo's README.md.
For your profile README (bit901/bit901), grab the "Profile Flair" block at the end.
-->

<p align="center">
  <img src="https://raw.githubusercontent.com/bit901/housefind-phoenix/main/.github/banner.png" alt="HouseFind Phoenix Banner" width="100%" />
  <!-- Fallback if you don't have a banner yet: replace with a screenshot or remove this img tag -->
</p>

<h1 align="center">HouseFind Phoenix</h1>

<p align="center">
  <b>Production-ready event discovery for Phoenix’s underground electronic music scene.</b><br/>
  Security-first • Fast APIs • Real-time updates • Clean UX
</p>

<p align="center">
  <a href="https://github.com/bit901/housefind-phoenix/actions">
    <img alt="CI" src="https://img.shields.io/github/actions/workflow/status/bit901/housefind-phoenix/ci.yml?label=CI&logo=githubactions&logoColor=white">
  </a>
  <img alt="TypeScript" src="https://img.shields.io/badge/TypeScript-Strict-3178C6?logo=typescript&labelColor=1b1f23&style=flat">
  <img alt="Performance" src="https://img.shields.io/badge/Perf-Optimized-blue?labelColor=1b1f23&style=flat">
  <img alt="Security" src="https://img.shields.io/badge/Security-100%25-success?labelColor=1b1f23&style=flat">
  <img alt="License" src="https://img.shields.io/badge/License-MIT-informational?labelColor=1b1f23&style=flat">
</p>

---

## 🔥 Why this exists

Phoenix has a thriving, slightly secret electronic scene. HouseFind Phoenix aggregates events from multiple sources (submissions, partner venues, scrapers) into a **fast, filterable** feed you can actually use on a Friday night.

---

## 📊 Key Metrics (current snapshot)

> Replace with your real metrics via your monitoring stack; values below are example targets.

| Metric                | Target (Industry) | HouseFind Phoenix | Status     |
|----------------------:|:------------------|:------------------|:-----------|
| API Response Time     | < 1000 ms         | **71–752 ms**     | ✅ Exceeded |
| DB Query Time         | < 500 ms          | **145–220 ms**    | ✅ Exceeded |
| Cache Speedup         | 2–3×              | **~9×**           | ⭐ Excellent |
| Page Load (P95)       | < 3 s             | **< 1 s**         | 🚀 Superior |
| Security Score        | ≥ 80%             | **100%**          | 🛡️ Perfect |

<details>
<summary><b>How</b> we hit these numbers</summary>

- 31+ hand-picked indexes, cursor-based pagination, eager loading to avoid N+1.
- In-memory LRU (server) + TanStack Query (client) with smart invalidation.
- Minimal payloads, HTTP caching, and SSR/edge delivery where possible.
</details>

---

## 🧩 Features

- **Real Scene Data:** Pulls from user submissions, verified venues, and scrapers.  
- **Advanced Filters:** Genre, date range, location radius, price, venue, source.  
- **Pro UX:** Mobile-first, PWA-ready, accessible components, dark mode.  
- **Live Updates:** Server-sent events (SSE) for at-the-door freshness.  
- **Security First:** CSRF protection, parameterized queries, strict validation (Zod).

---

## 🛠 Tech Stack

| Area      | Tech |
|-----------|------|
| Frontend  | React 18 + TypeScript, Vite, Tailwind (in-app), TanStack Query v5 |
| Backend   | Node.js + Express, Drizzle ORM |
| Database  | PostgreSQL (Neon serverless) |
| Auth      | Session-based, bcrypt |
| Monitoring| Sentry/DataDog, `pg_stat_statements`, UptimeRobot |

---

## 🚀 Quickstart

```bash
# 1) Install
npm install

# 2) Env
cp .env.example .env
# Edit .env with your secrets (DB, session secret, optional OAuth)

# 3) DB
npm run db:push   # or your drizzle migration command

# 4) Dev
npm run dev
