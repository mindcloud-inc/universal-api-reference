# Wafrow: Native API Reference

A consolidated summary of Wafrow's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://wafrow.com/docs/api
- **API base URL:** `https://wafrow.com/api`

## Authentication

### API Token

Use a Wafrow API token generated from Settings -> API Tokens in the Wafrow dashboard.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://wafrow.com/docs/api)

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
| [Get Current User](actions/get-current-user.md) | `GET /me` | [docs](https://wafrow.com/docs/api#/operations/auth.me) |
| [Get Variant Image](actions/get-variant-image.md) | `GET /i/:template_id/:campaign_id` | [docs](https://wafrow.com/docs/api#/operations/imageMagic.serveVariant) |
| [Pre-render Image](actions/pre-render-image.md) | `POST /img/:template_id` | [docs](https://wafrow.com/docs/api#/operations/imageMagic.createImage) |
| [Pre-render Image From Webhook](actions/pre-render-image-from-webhook.md) | `POST /i/:template_id` | [docs](https://wafrow.com/docs/api#/operations/imageMagic.generateFromWebhook) |
| [Save Variant](actions/save-variant.md) | `POST /storeVariant/:templateID` | [docs](https://wafrow.com/docs/api#/operations/variant.store) |
