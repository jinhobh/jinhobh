# Hi, I'm Jinho

Computer Science student building backend systems from the ground up. I care
less about how much I can stack together and more about being able to defend
every decision: why a retry queue over a cron job, why a database constraint over
an application-level check, what breaks under concurrency, and how I handle it.

Most of what I build lives in the unglamorous parts of the happy path: retries,
partial failures, idempotency, and the edge cases that only show up in
production.

## Currently Working On

**[Reliable Webhook Delivery Platform](https://github.com/jinhobh/reliable-webhook-platform)**  
`FastAPI` · `PostgreSQL` · `SQLAlchemy` · `Alembic` · `Docker`

A service for reliably delivering webhooks to subscriber endpoints. Payloads are
signed with HMAC-SHA256 so receivers can verify authenticity, and failed
deliveries are retried with backoff rather than dropped. The interesting work is
the failure handling: what counts as a delivery, when to give up, and how to keep
retries from stepping on each other.

```mermaid
flowchart LR
    Client[API client] -->|event + idempotency key| API[FastAPI app]
    API --> DB[(PostgreSQL)]
    API --> Delivery[delivery records]
    Delivery --> Worker[worker]
    Worker -->|signed webhook| Endpoint[subscriber endpoint]
    Worker --> Attempts[attempt logs]
    Worker --> Retry[retry / dead-letter / redrive]
    Attempts --> DB
    Retry --> DB
```

## Currently Learning

- State machine modeling for resource lifecycles
- Idempotency and safe retries
- Concurrency control through database constraints
- Cryptographic token hashing and secure invite/link design

**Next up:** a real-time collaborative editor to get hands-on with WebSockets and
presence management.

## Tools

![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![Java](https://img.shields.io/badge/Java-007396)
![C](https://img.shields.io/badge/C-00599C?logo=c&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?logo=fastapi&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?logo=postgresql&logoColor=white)
![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy-D71F00)
![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white)
![pytest](https://img.shields.io/badge/pytest-0A9EDC?logo=pytest&logoColor=white)

## How I Work

I learn by building. I'd rather ship a small thing that handles the hard cases
correctly than a big thing that only works on the demo. If a design decision
can't be explained with its tradeoffs, it's not finished yet.

## Reach Me

- Email: jinho.baej@gmail.com
