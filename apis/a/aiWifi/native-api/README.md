# AiWifi: Native API Reference

A consolidated summary of AiWifi's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://help.aiwifi.io/en/category/webhook
- **API base URL:** `https://api.aiwifi.io/api/v1`

## Authentication

### Workspace login

Sign in with an AiWifi workspace email and password to generate a bearer token for API requests.

### Credentials

- **Email:** `email` · required · AiWifi workspace login email.
- **Password:** `password` · required · AiWifi workspace login password.
- **Brand ID:** `brandId` · required · Numeric AiWifi brand ID from the `/en/{brandId}/...` app URL.

Send these headers with each API request:

```http
Authorization: Bearer <custom.accessToken>
```

[Official authentication documentation](https://help.aiwifi.io/developers/webhook-setup-and-configuration)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json, text/plain, */*` |

Responses from this API use JSON.

## Pagination

Use `length` in the query string to set the page size. Use `start` in the query string as the record offset; numbering starts at 0.

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create webhook](actions/create-webhook.md) | `POST /brands/{{brandId}}/webhook-configs` | [docs](https://help.aiwifi.io/en/category/webhook/article/webhook-setup-and-configuration) |
| [Delete webhook](actions/delete-webhook.md) | `DELETE /brands/{{brandId}}/webhook-configs/{{webhookId}}` | [docs](https://help.aiwifi.io/en/category/webhook/article/webhook-setup-and-configuration) |
| [Get auth token](actions/get-auth-token.md) | `POST /login` | [docs](https://help.aiwifi.io/developers/webhook-setup-and-configuration) |
| [Get webhook events](actions/get-webhook-events.md) | `GET /webhook/events` | [docs](https://help.aiwifi.io/developers/8718/webhooks) |
| [Get webhook log](actions/get-webhook-log.md) | `GET /brands/{{brandId}}/webhook-logs/{{logId}}` | [docs](https://help.aiwifi.io/en/category/webhook/article/logs-validation-and-testing-of-webhooks) |
| [List webhook logs](actions/list-webhook-logs.md) | `GET /brands/{{brandId}}/webhook-logs` | [docs](https://help.aiwifi.io/en/category/webhook/article/logs-validation-and-testing-of-webhooks) |
| [List webhooks](actions/list-webhooks.md) | `GET /brands/{{brandId}}/webhook-configs` | [docs](https://help.aiwifi.io/en/category/webhook/article/webhook-setup-and-configuration) |
| [Send test webhook event](actions/send-test-webhook-event.md) | `POST /brands/{{brandId}}/webhook-configs/{{webhookId}}/event/test` | [docs](https://help.aiwifi.io/en/category/webhook/article/logs-validation-and-testing-of-webhooks) |
| [Set webhook enabled](actions/set-webhook-enabled.md) | `PATCH /brands/{{brandId}}/enable/webhook/{{webhookId}}` | [docs](https://help.aiwifi.io/en/category/webhook/article/webhook-setup-and-configuration) |
| [Update webhook](actions/update-webhook.md) | `PUT /brands/{{brandId}}/webhook-configs/{{webhookId}}` | [docs](https://help.aiwifi.io/en/category/webhook/article/webhook-setup-and-configuration) |
