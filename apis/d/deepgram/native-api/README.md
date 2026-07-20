# Deepgram: Native API Reference

A consolidated summary of Deepgram's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://developers.deepgram.com/reference/deepgram-api-overview
- **API base URL:** `https://api.deepgram.com`

## Authentication

### API Key

Authenticate with a Deepgram project API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.deepgram.com/docs/authenticating)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `limit` in the query string to set the page size (default 10; accepted range 1–1000). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Project Key](actions/create-project-key.md) | `POST /v1/projects/:project_id/keys` | [docs](https://developers.deepgram.com/reference/manage/keys/create) |
| [Generate Temporary Token](actions/generate-temporary-token.md) | `POST /v1/auth/grant` | [docs](https://developers.deepgram.com/reference/auth/tokens/grant) |
| [Get Available Model](actions/get-available-model.md) | `GET /v1/models/:model_id` | [docs](https://developers.deepgram.com/reference/manage/models/get) |
| [Get Project](actions/get-project.md) | `GET /v1/projects/:project_id` | [docs](https://developers.deepgram.com/reference/manage/projects/get) |
| [Get Project Balance](actions/get-project-balance.md) | `GET /v1/projects/:project_id/balances/:balance_id` | [docs](https://developers.deepgram.com/reference/manage/billing/get) |
| [Get Project Balances](actions/get-project-balances.md) | `GET /v1/projects/:project_id/balances` | [docs](https://developers.deepgram.com/reference/manage/billing/list) |
| [Get Project Billing Breakdown](actions/get-project-billing-breakdown.md) | `GET /v1/projects/:project_id/billing/breakdown` | [docs](https://developers.deepgram.com/reference/manage/billing/breakdown/get) |
| [Get Project Key](actions/get-project-key.md) | `GET /v1/projects/:project_id/keys/:key_id` | [docs](https://developers.deepgram.com/reference/manage/keys/get) |
| [Get Project Model](actions/get-project-model.md) | `GET /v1/projects/:project_id/models/:model_id` | [docs](https://developers.deepgram.com/reference/manage/projects/models/get) |
| [Get Project Request](actions/get-project-request.md) | `GET /v1/projects/:project_id/requests/:request_id` | [docs](https://developers.deepgram.com/reference/manage/requests/get) |
| [Get Project Usage](actions/get-project-usage.md) | `GET /v1/projects/:project_id/usage` | [docs](https://developers.deepgram.com/reference/manage/usage/get) |
| [Get Project Usage Breakdown](actions/get-project-usage-breakdown.md) | `GET /v1/projects/:project_id/usage/breakdown` | [docs](https://developers.deepgram.com/reference/manage/usage/breakdown/get) |
| [Get Token Details](actions/get-token-details.md) | `GET /v1/auth/token` | [docs](https://developers.deepgram.com/guides/fundamentals/authenticating) |
| [List All Available Models](actions/list-all-available-models.md) | `GET /v1/models` | [docs](https://developers.deepgram.com/reference/manage/models/list) |
| [List Project Billing Fields](actions/list-project-billing-fields.md) | `GET /v1/projects/:project_id/billing/fields` | [docs](https://developers.deepgram.com/reference/manage/billing/fields/get) |
| [List Project Invites](actions/list-project-invites.md) | `GET /v1/projects/:project_id/invites` | [docs](https://developers.deepgram.com/reference/manage/invites/list) |
| [List Project Keys](actions/list-project-keys.md) | `GET /v1/projects/:project_id/keys` | [docs](https://developers.deepgram.com/reference/manage/keys/list) |
| [List Project Member Scopes](actions/list-project-member-scopes.md) | `GET /v1/projects/:project_id/members/:member_id/scopes` | [docs](https://developers.deepgram.com/reference/manage/members/scopes/list) |
| [List Project Members](actions/list-project-members.md) | `GET /v1/projects/:project_id/members` | [docs](https://developers.deepgram.com/reference/manage/members/list) |
| [List Project Models](actions/list-project-models.md) | `GET /v1/projects/:project_id/models` | [docs](https://developers.deepgram.com/reference/manage/projects/models/list) |
| [List Project Purchases](actions/list-project-purchases.md) | `GET /v1/projects/:project_id/purchases` | [docs](https://developers.deepgram.com/reference/manage/billing/purchases/get) |
| [List Project Requests](actions/list-project-requests.md) | `GET /v1/projects/:project_id/requests` | [docs](https://developers.deepgram.com/reference/manage/requests/list) |
| [List Project Usage Fields](actions/list-project-usage-fields.md) | `GET /v1/projects/:project_id/usage/fields` | [docs](https://developers.deepgram.com/reference/manage/usage/list) |
| [List Projects](actions/list-projects.md) | `GET /v1/projects` | [docs](https://developers.deepgram.com/reference/manage/projects/list) |
