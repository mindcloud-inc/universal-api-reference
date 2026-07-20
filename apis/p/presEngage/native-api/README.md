# PresEngage: Native API Reference

A consolidated summary of PresEngage's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://developer.presengage.com/
- **API base URL:** `https://shared.presengage.com/functions/v1/presengage-api`

## Authentication

### API Key

Authenticate PresEngage requests with your PresEngage API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developer.presengage.com/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Webhook Subscription](actions/create-webhook-subscription.md) | `POST /hooks` | [docs](https://developer.presengage.com/) |
| [Delete Webhook Subscription](actions/delete-webhook-subscription.md) | `DELETE /hooks/unsubscribe/:subscriptionId` | [docs](https://developer.presengage.com/) |
| [Get Authenticated User](actions/get-authenticated-user.md) | `GET /auth/test` | [docs](https://developer.presengage.com/) |
| [List Sample Webhook Messages](actions/list-sample-webhook-messages.md) | `GET /hooks/performList` | [docs](https://developer.presengage.com/) |
