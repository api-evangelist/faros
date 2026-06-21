# Faros AI (faros)

Faros AI is an engineering-operations intelligence platform (software engineering intelligence / SEI) that ingests data from across the SDLC toolchain into a connected canonical model and exposes it for querying. The platform offers a REST API for events and data ingestion at https://prod.api.faros.ai plus a GraphQL query API over the canonical model, with an open-source Faros Community Edition.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/faros/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/faros/refs/heads/main/apis.yml)

## Tags

- Engineering Operations
- Software Engineering Intelligence
- SEI
- DORA Metrics
- Developer Productivity
- Data Ingestion

## Timestamps

- **Created:** 2026-06-21
- **Modified:** 2026-06-21

## APIs

### Faros Events / Ingestion API (REST)

REST API for ingesting events and writing data into the Faros canonical model. Uses an API key passed in the Authorization header against the https://prod.api.faros.ai base URL, with endpoints for account/identity, graph management, and event ingestion. Backed by the open-source faros-events-cli and faros-js-client.

- **Human URL:** [https://docs.faros.ai/reference/getting-api-access](https://docs.faros.ai/reference/getting-api-access)
- **Base URL:** `https://prod.api.faros.ai`

#### Tags

- Events
- Ingestion
- REST
- CI/CD

#### Properties

- [Documentation](https://docs.faros.ai/reference/getting-api-access)
- [API Reference](https://docs.faros.ai/docs/the-custom-flows-api)
- [OpenAPI](openapi/faros-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/faros.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/faros.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Faros GraphQL Query API

Hasura-powered GraphQL API for querying the connected canonical model spanning the whole SDLC (50+ entities across VCS, CI/CD, task management, QA, incident management, compute, and org namespaces). Queries are issued to POST /graphs/{graph}/graphql, where graph is typically "default".

- **Human URL:** [https://docs.faros.ai/docs/querying-data](https://docs.faros.ai/docs/querying-data)
- **Base URL:** `https://prod.api.faros.ai`

#### Tags

- GraphQL
- Query
- Canonical Model
- Hasura

#### Properties

- [Documentation](https://docs.faros.ai/docs/querying-data)
- [API Reference](https://docs.faros.ai/docs/using-graphiql-application-to-query-data)
- [GraphQL](graphql/faros-graphql.md) — [GraphQL](https://graphql.org/)
- [OpenAPI](openapi/faros-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/faros.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/faros.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Faros Deployments / CI-CD API

Reports CI (build), CD (deployment), and TestExecution events into the platform to power DORA metrics and delivery analytics. Surfaced through the events ingestion REST API and the faros-events-cli / faros-cicd-github-action open-source tooling.

- **Human URL:** [https://github.com/faros-ai/faros-events-cli](https://github.com/faros-ai/faros-events-cli)
- **Base URL:** `https://prod.api.faros.ai`

#### Tags

- Deployments
- CI/CD
- Builds
- DORA Metrics

#### Properties

- [Documentation](https://docs.faros.ai/reference/getting-api-access)
- [API Reference](https://github.com/faros-ai/faros-events-cli)
- [OpenAPI](openapi/faros-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/faros.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/faros.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Faros Webhooks API

Inbound webhook endpoints that let source systems push events into Faros. Each webhook definition provides a unique URL of the form POST /webhooks/{webhook_id}/events for delivering events to the platform.

- **Human URL:** [https://docs.faros.ai/docs/configuring-your-source-system-with-webhooks](https://docs.faros.ai/docs/configuring-your-source-system-with-webhooks)
- **Base URL:** `https://prod.api.faros.ai`

#### Tags

- Webhooks
- Events
- Ingestion

#### Properties

- [Documentation](https://docs.faros.ai/docs/configuring-your-source-system-with-webhooks)
- [OpenAPI](openapi/faros-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/faros.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/faros.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [GitHub Organization](https://github.com/faros-ai)
- [LinkedIn](https://www.linkedin.com/company/faros-ai)
- [Website](https://www.faros.ai)
- [Documentation](https://docs.faros.ai)
- [Plans](plans/faros-plans-pricing.yml)
- [Rate Limits](rate-limits/faros-rate-limits.yml)
- [Fin Ops](finops/faros-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
