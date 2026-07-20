# Nudgify: Native API Reference

A consolidated summary of Nudgify's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://www.nudgify.com/docs/categories/for-developers/
- **API base URL:** `https://app.nudgify.com`

## Authentication

### API Key

Use your Nudgify API Key and Site Key to send social proof events.

### Credentials

- **API Key:** `apiKey` · required
- **Site Key:** `siteKey` · required · Your Nudgify Site Key for the site that will receive social proof events.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.nudgify.com/docs/knowledge-base/rest-api-for-sign-ups/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `accept` | `application/json` |
| `content-type` | `application/json` |

Responses from this API use JSON.

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Conversion](actions/create-conversion.md) | `POST /api/conversions` | [docs](https://www.nudgify.com/docs/knowledge-base/rest-api-for-sign-ups/) |
| [Create Purchase](actions/create-purchase.md) | `POST /api/purchases` | [docs](https://www.nudgify.com/docs/knowledge-base/api-purchase-nudges/) |
