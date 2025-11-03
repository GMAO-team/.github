<div align="center">

<img src="https://img.shields.io/badge/GMAO-team-CMMS%20for%20real%20operations-4b8bbe?style=for-the-badge" alt="GMAO-team: CMMS for real operations" />

# GMAO-team
**Open, pragmatic CMMS (GMAO) built with Django — fast to adopt, easy to operate, pleasant to extend.**

[![Built with Django](https://img.shields.io/badge/Django-Framework-092E20?style=for-the-badge&logo=django&logoColor=white)](https://www.djangoproject.com/)
[![Python 3.x](https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Docker Ready](https://img.shields.io/badge/Docker-Ready-2496ED?style=for-the-badge&logo=docker&logoColor=white)](https://www.docker.com/)
[![Code Style: Black](https://img.shields.io/badge/Code%20Style-Black-000000?style=flat)](https://black.readthedocs.io/)
[![Lint: Ruff](https://img.shields.io/badge/Lint-Ruff-5A9?style=flat)](https://docs.astral.sh/ruff/)
<br/>

### 🇫🇷 **GMAO** = *Gestion de Maintenance Assistée par Ordinateur* • 🇬🇧 **CMMS** = *Computerized Maintenance Management System*
</div>

---

## Why another CMMS?

Because small-to-mid teams deserve **clarity, speed, and ownership**:
- **Clear domain model** that matches maintenance reality.
- **Fast UI** for technicians and planners.
- **Own your data** with a standard relational DB and a documented API.
- **Deploy anywhere**: laptop, VM, on-prem, or cloud with Docker.

---

## What’s inside (MVP scope)

| Module (Domain) | Django app (code) | Purpose |
|---|---|---|
| **Accounts & Orgs** | `accounts` | Users, roles, orgs, auth flows. |
| **Assets & Locations** | `cmms_assets` | Asset register, locations, vendors, parts mapping. |
| **Work Orders** | `work_orders` | Corrective tasks, lifecycle, assignments, comments. |
| **Preventive Maintenance** | `procedures` | Procedures, checklists, PM plans. |
| **Meters & Readings** | `meters` | Counters, runtime, thresholds and alerts. |
| **Inventory** | `inventory` | Stock, parts, min/max, reservations, movements. |
| **Purchasing** | `purchasing` | RFQs/POs, suppliers, costs, receipts. |
| **Requests Portal** | `requests_portal` | Simple submit-a-request interface for non-users. |
| **Integrations** | `integrations` | Webhooks, health checks, external system connectors. |
| **Reports** | `reports` | KPIs, exports (CSV/Excel), dashboards. |
| **Core / API** | `core`, `cmms/src/api` | Settings, URLs, REST API endpoints. |

> Primary app repo: **`gmao-with-django-mvp`** → https://github.com/GMAO-team/gmao-with-django-mvp

---

## Architecture & Stack

- **Backend**: Django (+ Django REST Framework), typed views/forms, service-oriented modules.
- **Database**: PostgreSQL or MySQL (configurable), SQLite for local dev.
- **Packaging / Tooling**: `pyproject.toml`, pre-commit with **Ruff** + **Black**.
- **Containerization**: Docker / Compose for reproducible dev and deployment.
- **CI (suggested)**: GitHub Actions (lint, tests, migrations, build artifacts).

---

## Roadmap (high-level)

1. **MVP** — assets, WOs, PM, inventory, purchasing, meters, procedures, portal, reports.
2. **Multi-tenant orgs** — org boundaries, roles & permissions matrix.
3. **API polish** — pagination, filtering, webhooks; client SDKs.
4. **UX polish** — quick actions, mobile-friendly pages, fast lists.
5. **Integrations** — SSO, email notifications, Slack/Teams, ERP bridges.

> Track issues and milestones in the app repo: https://github.com/GMAO-team/gmao-with-django-mvp

---

## Try it now

- **Open in Codespaces** (recommended for a first look):  
  https://github.com/codespaces/new?hide_repo_select=true&ref=main&repo=GMAO-team%2Fgmao-with-django-mvp

- **Local with Docker** (from the app repo):
  ```bash
  git clone https://github.com/GMAO-team/gmao-with-django-mvp.git
  cd gmao-with-django-mvp
  cp .env.example .env   # adjust settings
  docker compose up -d --build
  ```

---

## Contributing

We welcome focused, incremental contributions:

- Start with **good first issues** in the app repo.
- Follow code style (**Black**) and lint (**Ruff**).
- Keep PRs small, documented, and testable.

> Organization-wide docs live here in `.github`:
>
> - `CONTRIBUTING.md` — how we work  
> - `CODE_OF_CONDUCT.md`  
> - `ISSUE_TEMPLATE/` & `PULL_REQUEST_TEMPLATE.md`

---

## Contact

- **Organization**: @GMAO-team  
- **Project**: https://github.com/GMAO-team/gmao-with-django-mvp  
- **Questions / ideas**: open an issue in the app repo

<div align="center">

**Built for maintainers, technicians, and planners.**  
*Fast to learn. Solid by design.*

</div>
