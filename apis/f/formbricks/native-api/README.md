# Formbricks: Native API Reference

A consolidated summary of Formbricks's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://formbricks.com/docs/api-v2-reference/introduction
- **API base URL:** `https://app.formbricks.com/api/v2`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://formbricks.com/docs/api-v2-reference/introduction/api-key-setup)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `limit` in the query string to set the page size (default 50; accepted range 1–250). Use `skip` in the query string as the record offset.

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Client Response](actions/create-client-response.md) | `POST /client/:environmentId/responses` | [docs](https://formbricks.com/docs/api-v2-reference/client-api--response/create-response) |
| [Create Webhook](actions/create-webhook.md) | `POST /management/webhooks` | [docs](https://formbricks.com/docs/api-v2-reference/management-api--webhooks/create-a-webhook) |
| [Get Me](actions/get-me.md) | `GET /me` | [docs](https://formbricks.com/docs/api-v2-reference/me/me) |
| [Get Response](actions/get-response.md) | `GET /management/responses/:id` | [docs](https://formbricks.com/docs/api-v2-reference/management-api--responses/get-a-response) |
| [Get Responses](actions/get-responses.md) | `GET /management/responses` | [docs](https://formbricks.com/docs/api-v2-reference/management-api--responses/get-responses) |
| [Get Webhook](actions/get-webhook.md) | `GET /management/webhooks/:id` | [docs](https://formbricks.com/docs/api-v2-reference/management-api--webhooks/get-a-webhook) |
| [Get Webhooks](actions/get-webhooks.md) | `GET /management/webhooks` | [docs](https://formbricks.com/docs/api-v2-reference/management-api--webhooks/get-webhooks) |
| [Update Client Response](actions/update-client-response.md) | `PUT /client/:environmentId/responses/:responseId` | [docs](https://formbricks.com/docs/api-v2-reference/client-api--response/update-response) |
