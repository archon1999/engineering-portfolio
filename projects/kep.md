<picture><source media="(prefers-color-scheme: dark)" srcset="../assets/kep-dark.svg"><img src="../assets/kep-light.svg" alt="KEP.uz — Founder / Software Engineer" width="100%"></picture>

# KEP.uz

**Programming practice as a connected platform.**

KEP.uz connects problem solving, submissions, contests, duels, learning paths and community features. Nazarbek Baltabaev founded the platform and works across the product, frontend, backend and online-judge infrastructure.

| Role | Stack |
| --- | --- |
| Founder / Software Engineer | React · TypeScript · MUI · Django · PostgreSQL · Redis |

## Product surface

Problem and submission workspaces, contest flows, duels, learning and community experiences share a modular React application.

## Interface architecture

The public frontend separates app composition, product modules and shared infrastructure. Feature boundaries follow UI, application hooks, repository contracts, data-access implementations and DTO mapping.

## Typed integration

Generated OpenAPI clients connect the React workspace to backend APIs. Authentication, CSRF handling, localization and real-time updates are shared concerns.

## Judging path

Submissions pass through the backend to isolated code-evaluation infrastructure. Problems, tests and verdicts remain separate from the presentation layer.

## Operational scope

Public counters distinguish registered users, visible problems, contests and submitted solutions. They do not represent daily active users or accepted-solution totals.

## High-level architecture

```mermaid
flowchart LR
  U[Programming workspace] --> R[React / TypeScript]
  R --> C[Typed API boundary]
  C --> D[Django services]
  D --> P[(PostgreSQL)]
  D --> Q[Submission processing]
  Q --> J[Isolated judge]
  J --> V[Verdicts and results]
  V --> U
```

## Public platform data

| Registered users | Visible problems | Contests | Submissions |
| ---: | ---: | ---: | ---: |
| 9,566 | 2,101 | 374 | 436,371 |

Observed **2026-10-29**, Asia/Tashkent. [Public API](https://kep.uz/api/landing-page-statistics) · [Snapshot data](../data/platform-snapshot.json).

## Links

- [Product website](https://kep.uz/)
- [Public source repository](https://github.com/archon1999/kep-frontend)
- [Nazarbek Baltabaev](https://github.com/archon1999)

[← All projects](../README.md)
