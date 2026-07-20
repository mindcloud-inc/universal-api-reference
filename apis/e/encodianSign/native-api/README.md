# Encodian - Sign: Native API Reference

A consolidated summary of Encodian - Sign's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://support.encodian.com/hc/en-gb/sections/25624905449116-Power-Automate-Action-Documentation
- **OpenAPI specification:** https://api.apps-encodian.com/swagger/Sign/swagger.json
- **API base URL:** `https://api.apps-encodian.com`

## Authentication

### API Key

Use your Encodian API key from the Encodian account portal.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-ApiKey: <apiKey>
```

[Official authentication documentation](https://support.encodian.com/hc/en-gb/articles/13665831383836-Multiple-API-Key-Management)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Trigr Webhook Subscription](actions/create-trigr-webhook-subscription.md) | `POST /api/v1/Trigr/ManageWebHook` | [docs](https://api.apps-encodian.com/swagger/Sign/swagger.json) |
| [Delete Trigr Webhook Subscription](actions/delete-trigr-webhook-subscription.md) | `DELETE /api/v1/Trigr/ManageWebHook/:tenantWebHookId` | [docs](https://api.apps-encodian.com/swagger/Sign/swagger.json) |
| [Get Trigr Subscription Status](actions/get-trigr-subscription-status.md) | `GET /api/v1/Trigr/GetTrigrSubscriptionStatus` | [docs](https://api.apps-encodian.com/swagger/Sign/swagger.json) |
| [Sign - Send File For Signature](actions/sign-send-file-for-signature.md) | `POST /api/v1/Sign/EnvelopeCreateSingle` | [docs](https://support.encodian.com/hc/en-gb/articles/26845003436828-Envelope-Send-File-for-Signature) |
