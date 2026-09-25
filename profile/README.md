<p align="center">
  <img src="https://avatars.githubusercontent.com/u/301216518?v=4" alt="LiveXFace logo" width="108" />
</p>

<h1 align="center">LiveXFace</h1>

<p align="center">
  <strong>Face recognition and liveness through an API.</strong><br />
  A proof of concept for integrating biometric checks into applications.
</p>

## What we're building

LiveXFace is an API-first project for face recognition and liveness detection. The goal is to keep application-facing APIs separate from model inference and face search, so each part can evolve without changing the way applications integrate.

| Area | Focus |
| --- | --- |
| Face recognition | Match faces and search stored embeddings. |
| Liveness | Assess whether a face capture comes from a live person. |
| Integration | Expose these capabilities through clear API boundaries. |

## Technical direction

The POC is being developed around the following components:

| Component | Technology |
| --- | --- |
| API | Go, Gin |
| Inference | Python, Flask, InsightFace |
| Face search and storage | PostgreSQL, pgvector |
| Cache and messaging | Redis, NATS |
| Routing | Traefik |

## Status

LiveXFace is in the POC stage. Interfaces, documentation, and repository structure may change as the product is validated. This README describes the project's direction; it is not a production-readiness or accuracy claim.
