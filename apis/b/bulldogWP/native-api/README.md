# Bulldog-WP: Native API Reference

A consolidated summary of Bulldog-WP's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://console.bulldog-wp.co.il/docs/
- **OpenAPI specification:** https://console.bulldog-wp.co.il/docs/specification
- **API base URL:** `https://api.bulldog-wp.co.il/v1`

## Authentication

### API Key

Use a Bulldog WP API key. The provider requires the key in the Token request header; the token can be created in the Bulldog WP console.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Token: <apiKey>
```

[Official authentication documentation](https://console.bulldog-wp.co.il/docs/specification)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `size` in the query string to set the page size (default 20; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 0.

## Filtering

Send filters in the query string. Supported operators: `contains`, `eq`, `gte`, `lte`.

## Sorting

Set the sort field with `sort` in the query string. Prefix the field name to select its direction. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get session health](actions/device-health.md) | `GET /devices/{deviceId}/health` | [docs](https://console.bulldog-wp.co.il/docs/specification) |
| [Download file content](actions/download-file.md) | `GET /files/{fileId}/download` | [docs](https://console.bulldog-wp.co.il/docs/specification) |
| [Get analytics](actions/get-analytics.md) | `GET /analytics` | [docs](https://console.bulldog-wp.co.il/docs/specification) |
| [Get campaign](actions/get-campaign.md) | `GET /campaigns/{campaignId}` | [docs](https://console.bulldog-wp.co.il/docs/specification) |
| [List campaign contacts](actions/get-campaign-contacts.md) | `GET /campaigns/{campaignId}/contacts` | [docs](https://console.bulldog-wp.co.il/docs/specification) |
| [Get campaigns](actions/get-campaigns.md) | `GET /campaigns` | [docs](https://console.bulldog-wp.co.il/docs/specification) |
| [Search chat messages](actions/get-chat-messages.md) | `GET /chat/{deviceId}/messages` | [docs](https://console.bulldog-wp.co.il/docs/specification) |
| [Get number by ID](actions/get-device-by-id.md) | `GET /devices/{deviceId}` | [docs](https://console.bulldog-wp.co.il/docs/specification) |
| [Get chat by WID](actions/get-device-chat-details.md) | `GET /chat/{deviceId}/chats/{chatWid}` | [docs](https://console.bulldog-wp.co.il/docs/specification) |
| [Search chats](actions/get-device-chats.md) | `GET /chat/{deviceId}/chats` | [docs](https://console.bulldog-wp.co.il/docs/specification) |
| [Get contact](actions/get-device-contact-details.md) | `GET /chat/{deviceId}/contacts/{contactWid}` | [docs](https://console.bulldog-wp.co.il/docs/specification) |
| [List contacts](actions/get-device-contacts.md) | `GET /chat/{deviceId}/contacts` | [docs](https://console.bulldog-wp.co.il/docs/specification) |
| [Get inbound file details](actions/get-device-file-details.md) | `GET /chat/{deviceId}/files/{fileId}` | [docs](https://console.bulldog-wp.co.il/docs/specification) |
| [Search inbound files](actions/get-device-files.md) | `GET /chat/{deviceId}/files` | [docs](https://console.bulldog-wp.co.il/docs/specification) |
| [Get message details](actions/get-device-message-details.md) | `GET /chat/{deviceId}/messages/{messageWid}` | [docs](https://console.bulldog-wp.co.il/docs/specification) |
| [Get numbers](actions/get-devices.md) | `GET /devices` | [docs](https://console.bulldog-wp.co.il/docs/specification) |
| [Get file information](actions/get-file.md) | `GET /files/{fileId}` | [docs](https://console.bulldog-wp.co.il/docs/specification) |
| [List labels](actions/get-labels.md) | `GET /devices/{deviceId}/labels` | [docs](https://console.bulldog-wp.co.il/docs/specification) |
| [Get message by ID](actions/get-message.md) | `GET /messages/{messageId}` | [docs](https://console.bulldog-wp.co.il/docs/specification) |
| [Get users](actions/get-team-users.md) | `GET /team` | [docs](https://console.bulldog-wp.co.il/docs/specification) |
| [List templates](actions/get-templates.md) | `GET /waba/templates` | [docs](https://console.bulldog-wp.co.il/docs/specification) |
| [Get messaging prices](actions/get-waba-prices.md) | `GET /waba/prices` | [docs](https://console.bulldog-wp.co.il/docs/specification) |
| [Get webhook details](actions/get-webhook.md) | `GET /webhooks/{webhookId}` | [docs](https://console.bulldog-wp.co.il/docs/specification) |
| [Get webhook logs](actions/get-webhook-logs.md) | `GET /webhooks/{webhookId}/logs` | [docs](https://console.bulldog-wp.co.il/docs/specification) |
| [Get webhooks](actions/get-webhooks.md) | `GET /webhooks` | [docs](https://console.bulldog-wp.co.il/docs/specification) |
| [Check number exists](actions/number-exists.md) | `POST /numbers/exists` | [docs](https://console.bulldog-wp.co.il/docs/specification) |
| [Preview image](actions/preview-file.md) | `GET /files/{fileId}/preview` | [docs](https://console.bulldog-wp.co.il/docs/specification) |
| [Search files](actions/search-files.md) | `GET /files` | [docs](https://console.bulldog-wp.co.il/docs/specification) |
| [Search messages](actions/search-messages.md) | `GET /messages` | [docs](https://console.bulldog-wp.co.il/docs/specification) |
| [Validate numbers](actions/validate-numbers.md) | `POST /numbers/validate` | [docs](https://console.bulldog-wp.co.il/docs/specification) |
