# Jinho

I build backend systems and developer tools with an eye for reliability, clear
interfaces, and practical automation.

Right now I am focused on production-style Python services, distributed-system
failure modes, and agent-assisted development workflows that keep quality gates
visible instead of decorative.

## Current Work

- Building a [reliable webhook delivery platform](https://github.com/jinhobh/reliable-webhook-platform)
  with FastAPI, PostgreSQL, SQLAlchemy, Alembic, idempotency, HMAC signing,
  retries, dead-lettering, and redrive.
- Designing autonomous planner / builder / reviewer loops that turn scoped
  GitHub issues into reviewed pull requests with CI-enforced quality checks.
- Exploring static analysis through
  [tracegraph](https://github.com/jinhobh/tracegraph), a dependency analyzer for
  Python import graphs, circular imports, and test impact analysis.
- Building focused learning tools, including a browser-based interview-practice
  app with search, topic filters, a LeetCode mapping table, and an in-browser
  Python judge.

## Projects

| Project | What it demonstrates |
| --- | --- |
| [Reliable Webhook Delivery Platform](https://github.com/jinhobh/reliable-webhook-platform) | Durable event ingestion, async delivery, retries, idempotency, security, observability, and migration-driven backend design. |
| [tracegraph](https://github.com/jinhobh/tracegraph) | Python static analysis, import graph construction, circular dependency detection, and test impact reasoning. |
| [Granola](https://github.com/jinhobh/granola) | Product thinking around mobile-first content, social metadata, privacy, search, and user flows. |

## Stack

**Languages:** Python, JavaScript, SQL  
**Backend:** FastAPI, PostgreSQL, SQLAlchemy, Alembic, Pydantic  
**Quality:** pytest, mypy, ruff, CI, migration discipline  
**Interests:** reliable systems, developer tooling, agents, product engineering

## How I Work

I like small, well-specified changes; explicit acceptance criteria; and tests
that cover the behavior people actually depend on. I care about making systems
observable and recoverable because the interesting bugs usually happen after the
happy path has already passed.

