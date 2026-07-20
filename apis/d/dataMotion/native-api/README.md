# DataMotion: Native API Reference

A consolidated summary of DataMotion's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://datamotion.com/guide-to-secure-message-delivery-api/
- **API base URL:** `https://api.datamotion.com/SecureMessageDelivery`

## Authentication

### API Key

Authenticate requests with DataMotion's X-API-Key and X-API-Secret headers.

### Credentials

- **X-API-Key:** `apiKey` · required
- **X-API-Secret:** `apiSecret` · required · Secret value tied to the DataMotion API key.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://datamotion.com/guide-to-secure-message-delivery-api/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Retract Secure Message](actions/retract-secure-message.md) | `DELETE /v1.2/:transactionId/Retract` | [docs](https://learn.microsoft.com/en-us/connectors/securemessagedelivery/) |
| [Send Secure Message](actions/send-secure-message.md) | `POST /v1.2/Email` | [docs](https://datamotion.com/guide-to-secure-message-delivery-api/) |
| [Track Secure Message](actions/track-secure-message.md) | `GET /v1.2/:transactionId/Track` | [docs](https://learn.microsoft.com/en-us/connectors/securemessagedelivery/) |
