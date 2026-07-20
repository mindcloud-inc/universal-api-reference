# Climbo 2.0: Native API Reference

A consolidated summary of Climbo 2.0's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://climbo.readme.io/reference
- **API base URL:** `https://api.climbo.com`

## Authentication

### API Key

Climbo uses an x-api-key header on all documented Agency Mode endpoints.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://climbo.readme.io/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Client](actions/add-client.md) | `POST /client` | [docs](https://climbo.readme.io/reference/add-client) |
| [Change Client Plan](actions/change-client-plan.md) | `POST /client/{client_id}/change-plan` | [docs](https://climbo.readme.io/reference/change-client-plan) |
| [Change Client Status](actions/change-client-status.md) | `POST /client/{client_id}/change-status` | [docs](https://climbo.readme.io/reference/change-client-status) |
| [Create Subscription](actions/create-subscription.md) | `POST /webhook/subscribe` | [docs](https://climbo.readme.io/reference/create-subscription) |
| [Delete Client](actions/delete-client.md) | `DELETE /client/{client_id}` | [docs](https://climbo.readme.io/reference/delete-client) |
| [Delete Subscription](actions/delete-subscription.md) | `DELETE /webhook/unsubscribe/{webhook_id}` | [docs](https://climbo.readme.io/reference/delete-subscription) |
| [Get Client](actions/get-client.md) | `GET /client/{client_id}` | [docs](https://climbo.readme.io/reference/get-client) |
| [Get Plan](actions/get-plan.md) | `GET /plan/{plan_id}` | [docs](https://climbo.readme.io/reference/get-plan) |
| [List Clients](actions/list-clients.md) | `GET /clients` | [docs](https://climbo.readme.io/reference/list-clients) |
| [List Plans](actions/list-plans.md) | `GET /plans` | [docs](https://climbo.readme.io/reference/list-plans) |
