# Slottable: Native API Reference

A consolidated summary of Slottable's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://slottable.app/docs/p/integrations-and-api
- **API base URL:** `https://slottable.app/api/v1`

## Authentication

### API Token

Use the API token generated in Slottable integrations settings.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://slottable.app/docs/p/integrations-and-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | `POST /companies/:companyId/webhooks` | [docs](https://slottable.app/docs/p/integrations-and-api) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /companies/:companyId/webhooks/:hookId` | [docs](https://slottable.app/docs/p/integrations-and-api) |
| [Get Token Details](actions/get-token-details.md) | `GET /token` | [docs](https://slottable.app/docs/p/integrations-and-api) |
