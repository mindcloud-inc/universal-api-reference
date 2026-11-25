# Celigo: Native API Reference

A consolidated summary of Celigo's API configuration and 17 documented operations, with links to official documentation.

- **Official docs:** https://developer.celigo.com/api
- **API base URL:** `https://{apiHost}/v1`

## Authentication

### API Token

Connect with a Celigo integrator.io API token (service token or personal access token).

### Credentials

- **API Token:** `apiKey` · required
- **API Host:** `apiHost` · required · Your Celigo region's API host. Keep api.integrator.io for US accounts (you sign in at integrator.io). Use api.eu.integrator.io for EU, api.au.integrator.io for AU, or api.ca.integrator.io for CA.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developer.celigo.com/api/getting-started/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–1000). Use `after` in the query string as the pagination cursor. Follow the complete next-page URL returned by the API.

## Retry behavior

Retry responses with status codes `429`. Wait 1000 ms before the first retry. Stop after 5 attempts. Multiply the delay by 1 after each failed attempt.

## Endpoints (17 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Connection](actions/get-connection.md) | `GET /connections/:connectionId` | [docs](https://developer.celigo.com/api/api-reference/connections-and-http-connectors/connections) |
| [Get Flow](actions/get-flow.md) | `GET /flows/:flowId` | [docs](https://developer.celigo.com/api/api-reference/integrations-and-flows/flows) |
| [Get Flow Error Summary](actions/get-flow-error-summary.md) | `GET /flows/:flowId/errors` | [docs](https://developer.celigo.com/api/api-reference/integrations-and-flows/flows) |
| [Get Integration](actions/get-integration.md) | `GET /integrations/:integrationId` | [docs](https://developer.celigo.com/api/api-reference/integrations-and-flows/integrations) |
| [Get Integration Error Summary](actions/get-integration-error-summary.md) | `GET /integrations/:integrationId/errors` | [docs](https://developer.celigo.com/api/api-reference/integrations-and-flows/integrations) |
| [Get Token Info](actions/get-token-info.md) | `GET /tokenInfo` | [docs](https://developer.celigo.com/api/api-reference/account-and-admin/account) |
| [List Audit Logs](actions/list-audit-logs.md) | `GET /audit` | [docs](https://developer.celigo.com/api/api-reference/monitoring/audit-logs) |
| [List Connections](actions/list-connections.md) | `GET /connections` | [docs](https://developer.celigo.com/api/api-reference/connections-and-http-connectors/connections) |
| [List Exports](actions/list-exports.md) | `GET /exports` | [docs](https://developer.celigo.com/api/api-reference/exports-imports-and-tools/exports) |
| [List Flows](actions/list-flows.md) | `GET /flows` | [docs](https://developer.celigo.com/api/api-reference/integrations-and-flows/flows) |
| [List Imports](actions/list-imports.md) | `GET /imports` | [docs](https://developer.celigo.com/api/api-reference/exports-imports-and-tools/imports) |
| [List Integrations](actions/list-integrations.md) | `GET /integrations` | [docs](https://developer.celigo.com/api/api-reference/integrations-and-flows/integrations) |
| [List Jobs](actions/list-jobs.md) | `GET /jobs` | [docs](https://developer.celigo.com/api/api-reference/monitoring/jobs) |
| [List Latest Flow Jobs](actions/list-latest-flow-jobs.md) | `GET /flows/:flowId/jobs/latest` | [docs](https://developer.celigo.com/api/api-reference/monitoring/jobs) |
| [List Open Errors](actions/list-open-errors.md) | `GET /flows/:flowId/:stepId/errors` | [docs](https://developer.celigo.com/api/api-reference/integrations-and-flows/flows) |
| [List Resolved Errors](actions/list-resolved-errors.md) | `GET /flows/:flowId/:stepId/resolved` | [docs](https://developer.celigo.com/api/api-reference/integrations-and-flows/flows) |
| [Ping Connection](actions/ping-connection.md) | `GET /connections/:connectionId/ping` | [docs](https://developer.celigo.com/api/api-reference/connections-and-http-connectors/connections) |
