# Renderly: Native API Reference

A consolidated summary of Renderly's API configuration and 9 documented operations, with links to official documentation.

- **Official docs:** https://renderly.video/docs
- **OpenAPI specification:** https://renderly.video/api/openapi
- **API base URL:** `https://renderly.video/api/v1`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://renderly.video/api/docs)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (9 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Render Job](actions/create-render-job.md) | `POST /renders` | [docs](https://renderly.video/api/docs) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks` | [docs](https://renderly.video/api/docs) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /webhooks` | [docs](https://renderly.video/api/docs) |
| [Get Account](actions/get-account.md) | `GET /account` | [docs](https://renderly.video/api/docs) |
| [Get Render Status](actions/get-render-status.md) | `GET /renders/:jobId` | [docs](https://renderly.video/api/docs) |
| [List Templates](actions/list-templates.md) | `GET /templates` | [docs](https://renderly.video/api/docs) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks` | [docs](https://renderly.video/api/docs) |
| [Upload Media](actions/upload-media.md) | `POST /uploads` | [docs](https://renderly.video/api/docs) |
| [Verify API Key](actions/verify-api-key.md) | `POST /auth/verify` | [docs](https://renderly.video/api/docs) |
