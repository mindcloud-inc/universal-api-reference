# EventSquare: Native API Reference

A consolidated summary of EventSquare's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://api.eventsquare.io/docs
- **OpenAPI specification:** https://api.eventsquare.io/openapi/openapi.yaml
- **API base URL:** `https://api.eventsquare.io`

## Authentication

### API Key

API key authentication for the EventSquare Integrations API.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.eventsquare.io/docs)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Delete Make Webhook](actions/delete-make-webhook.md) | `DELETE /1.0/integrations/make/triggers` | [docs](https://api.eventsquare.io/docs) |
| [Delete Zapier Webhook](actions/delete-zapier-webhook.md) | `DELETE /1.0/integrations/zapier/triggers` | [docs](https://api.eventsquare.io/docs) |
| [Get Make Account](actions/get-make-account.md) | `GET /1.0/integrations/make/test` | [docs](https://api.eventsquare.io/docs) |
| [Get Zapier Account](actions/get-zapier-account.md) | `GET /1.0/integrations/zapier/test` | [docs](https://api.eventsquare.io/docs) |
| [List Make Trigger Examples](actions/list-make-trigger-examples.md) | `GET /1.0/integrations/make/triggers` | [docs](https://api.eventsquare.io/docs) |
| [List Zapier Trigger Examples](actions/list-zapier-trigger-examples.md) | `GET /1.0/integrations/zapier/triggers` | [docs](https://api.eventsquare.io/docs) |
| [Register Make Webhook](actions/register-make-webhook.md) | `POST /1.0/integrations/make/triggers` | [docs](https://api.eventsquare.io/docs) |
| [Register Zapier Webhook](actions/register-zapier-webhook.md) | `POST /1.0/integrations/zapier/triggers` | [docs](https://api.eventsquare.io/docs) |
