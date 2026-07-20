# Budgets.ai: Native API Reference

A consolidated summary of Budgets.ai's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://crm.budgets.ai/dashboard/api-center/incoming
- **API base URL:** `https://myapiconnect.com`

## Authentication

### API Key

Budgets.ai expects your API key in the JSON request body as api_key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://crm.budgets.ai/dashboard/api-center/incoming)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Campaigns](actions/list-campaigns.md) | `POST /api-product/incoming-webhook/fetch-all-campaigns` | [docs](https://crm.budgets.ai/dashboard/api-center/incoming) |
