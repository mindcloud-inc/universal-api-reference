# Persona: Native API Reference

A consolidated summary of Persona's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://docs.withpersona.com/api-keys
- **OpenAPI specification:** https://raw.githubusercontent.com/persona-id/persona-openapi/main/2025-12-08/openapi-bundled.json
- **API base URL:** `https://api.withpersona.com/api/v1`

## Authentication

### API Key

Connect Persona with a Persona API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.withpersona.com/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `page[size]` in the query string to set the page size. Use `page[number]` in the query string to choose the page; numbering starts at 0.

## Filtering

Send filters in the query string. Supported operators: `eq`.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Account Tag](actions/add-account-tag.md) | `POST /accounts/[:account-id]/add-tag` | [docs](https://docs.withpersona.com/api-reference/accounts/add-tag-to-an-account) |
| [Create Account](actions/create-account.md) | `POST /accounts` | [docs](https://docs.withpersona.com/api-reference/accounts/create-an-account) |
| [List Accounts](actions/list-accounts.md) | `GET /accounts` | [docs](https://docs.withpersona.com/api-reference/accounts/list-all-accounts) |
| [List API keys](actions/list-api-keys.md) | `GET /api-keys` | [docs](https://docs.withpersona.com/api-reference/api-keys/list-all-api-keys) |
| [List API Logs](actions/list-api-logs.md) | `GET /api-logs` | [docs](https://docs.withpersona.com/api-reference/api-logs/list-all-api-logs) |
| [List Cases](actions/list-cases.md) | `GET /cases` | [docs](https://docs.withpersona.com/api-reference/cases/list-all-cases) |
| [List Connections](actions/list-connections.md) | `GET /connect/connections` | [docs](https://docs.withpersona.com/api-reference/connect/connections/list-all-connect-connections) |
| [List Devices](actions/list-devices.md) | `GET /devices` | [docs](https://docs.withpersona.com/api-reference/devices/list-all-devices) |
| [List Events](actions/list-events.md) | `GET /events` | [docs](https://docs.withpersona.com/api-reference/events/list-all-events) |
| [List Importers](actions/list-importers.md) | `GET /importers` | [docs](https://docs.withpersona.com/api-reference/importers/list-all-importers) |
| [List Inquiries](actions/list-inquiries.md) | `GET /inquiries` | [docs](https://docs.withpersona.com/api-reference/inquiries/list-all-inquiries) |
| [List Inquiry Sessions](actions/list-inquiry-sessions.md) | `GET /inquiry-sessions` | [docs](https://docs.withpersona.com/api-reference/inquiry-sessions/list-all-inquiry-sessions) |
| [List Inquiry Templates](actions/list-inquiry-templates.md) | `GET /inquiry-templates` | [docs](https://docs.withpersona.com/api-reference/inquiry-templates/list-all-inquiry-templates) |
| [List Lists](actions/list-lists.md) | `GET /lists` | [docs](https://docs.withpersona.com/api-reference/lists/list-all-lists) |
| [List Rate Limits](actions/list-rate-limits.md) | `GET /rate-limits` | [docs](https://docs.withpersona.com/api-reference/rate-limits/list-all-rate-limits) |
| [List Reports](actions/list-reports.md) | `GET /reports` | [docs](https://docs.withpersona.com/api-reference/reports/list-all-reports) |
| [List Share Tokens](actions/list-share-tokens.md) | `GET /connect/share-tokens` | [docs](https://docs.withpersona.com/api-reference/share-tokens/list-all-share-tokens) |
| [List Transactions](actions/list-transactions.md) | `GET /transactions` | [docs](https://docs.withpersona.com/api-reference/transactions/list-all-transactions) |
| [List User Audit Logs](actions/list-user-audit-logs.md) | `GET /user-audit-logs` | [docs](https://docs.withpersona.com/api-reference/user-audit-logs/list-all-user-audit-logs) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks` | [docs](https://docs.withpersona.com/api-reference/webhooks/list-all-webhooks) |
| [List Workflow Runs](actions/list-workflow-runs.md) | `GET /workflow-runs` | [docs](https://docs.withpersona.com/api-reference/workflow-runs/list-all-workflow-runs) |
| [Redact Account](actions/redact-account.md) | `DELETE /accounts/[:account-id]` | [docs](https://docs.withpersona.com/api-reference/accounts/redact-an-account) |
| [Remove Account Tag](actions/remove-account-tag.md) | `POST /accounts/[:account-id]/remove-tag` | [docs](https://docs.withpersona.com/api-reference/accounts/remove-tag-from-an-account) |
| [Retrieve Account](actions/retrieve-account.md) | `GET /accounts/[:account-id]` | [docs](https://docs.withpersona.com/api-reference/accounts/retrieve-an-account) |
| [Retrieve API Log](actions/retrieve-api-log.md) | `GET /api-logs/[:api-log-id]` | [docs](https://docs.withpersona.com/api-reference/api-logs/retrieve-an-api-log) |
| [Retrieve Event](actions/retrieve-event.md) | `GET /events/[:event-id]` | [docs](https://docs.withpersona.com/api-reference/events/retrieve-an-event) |
| [Retrieve Inquiry Template](actions/retrieve-inquiry-template.md) | `GET /inquiry-templates/[:inquiry-template-id]` | [docs](https://docs.withpersona.com/api-reference/inquiry-templates/retrieve-an-inquiry-template) |
| [Search Accounts](actions/search-accounts.md) | `POST /accounts/search` | [docs](https://docs.withpersona.com/api-reference/accounts/search-accounts) |
| [Search Cases](actions/search-cases.md) | `POST /cases/search` | [docs](https://docs.withpersona.com/api-reference/cases/search-cases) |
| [Update Account](actions/update-account.md) | `PATCH /accounts/[:account-id]` | [docs](https://docs.withpersona.com/api-reference/accounts/update-an-account) |
