# Sign Customiser: Native API Reference

A consolidated summary of Sign Customiser's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://www.signcustomiser.com/help/api/
- **OpenAPI specification:** https://www.signcustomiser.com/help/openapi.yaml
- **API base URL:** `https://web.signcustomiser.com`

## Authentication

### API Token

Use a Sign Customiser API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.signcustomiser.com/help/universal-app/how-to-create-an-api-token/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | `POST /api/v2/webhooks` | [docs](https://www.signcustomiser.com/help/api/post-create-a-new-webhook/) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /api/v2/webhooks/:webhookId` | [docs](https://www.signcustomiser.com/help/api/delete-delete-a-webhook/) |
| [Get Webhook](actions/get-webhook.md) | `GET /api/v2/webhooks/:webhookId` | [docs](https://www.signcustomiser.com/help/api/get-get-a-single-webhook/) |
| [List Webhooks](actions/list-webhooks.md) | `GET /api/v2/webhooks` | [docs](https://www.signcustomiser.com/help/api/get-list-all-webhooks/) |
| [Update Webhook](actions/update-webhook.md) | `PUT /api/v2/webhooks/:webhookId` | [docs](https://www.signcustomiser.com/help/api/put-update-a-webhook/) |
