# Auphonic: Native API Reference

A consolidated summary of Auphonic's API configuration and 22 documented operations, with links to official documentation.

- **Official docs:** https://auphonic.com/help/api/
- **OpenAPI specification:** https://auphonic.com/help/openapi.yaml
- **API base URL:** `https://auphonic.com/api`

## Authentication

### API Key

Authenticate with an Auphonic API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://auphonic.com/help/api/authentication.html#api-key-authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 100; minimum 1). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (22 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Preset](actions/create-preset.md) | `POST /presets.json` | [docs](https://auphonic.com/help/api/details.html#creation-of-presets) |
| [Create Production](actions/create-production.md) | `POST /productions.json` | [docs](https://auphonic.com/help/api/details.html#create-a-production-with-detailed-audio-metadata) |
| [Delete Preset](actions/delete-preset.md) | `DELETE /preset/:uuid.json` | [docs](https://auphonic.com/help/api/update.html#further-examples) |
| [Delete Production](actions/delete-production.md) | `DELETE /production/:uuid.json` | [docs](https://auphonic.com/help/api/update.html#further-examples) |
| [Delete Production Webhook](actions/delete-production-webhook.md) | `DELETE /production/:uuid/webhook.json` | [docs](https://auphonic.com/help/api/webhook.html#delete-a-webhook) |
| [Get API Information](actions/get-api-information.md) | `GET /info.json` | [docs](https://auphonic.com/help/api/query.html) |
| [Get Audio Algorithms](actions/get-audio-algorithms.md) | `GET /info/algorithms.json` | [docs](https://auphonic.com/help/api/details.html#query-audio-algorithms) |
| [Get Current User Account Info](actions/get-current-user-account-info.md) | `GET /user.json` | [docs](https://auphonic.com/help/api/query.html#information-about-a-user-account) |
| [Get Output File Formats](actions/get-output-file-formats.md) | `GET /info/output_files.json` | [docs](https://auphonic.com/help/api/details.html#query-output-formats) |
| [Get Preset](actions/get-preset.md) | `GET /preset/:uuid.json` | [docs](https://auphonic.com/help/api/query.html#details-about-a-preset) |
| [Get Production](actions/get-production.md) | `GET /production/:uuid.json` | [docs](https://auphonic.com/help/api/query.html#details-about-a-production) |
| [Get Production Status](actions/get-production-status.md) | `GET /production/:uuid/status.json` | [docs](https://auphonic.com/help/api/query.html) |
| [Get Production Status Codes](actions/get-production-status-codes.md) | `GET /info/production_status.json` | [docs](https://auphonic.com/help/api/query.html#query-production-status) |
| [Get Production Webhook](actions/get-production-webhook.md) | `GET /production/:uuid/webhook.json` | [docs](https://auphonic.com/help/api/webhook.html) |
| [Get Service Types](actions/get-service-types.md) | `GET /info/service_types.json` | [docs](https://auphonic.com/help/api/details.html#query-service-types) |
| [List Presets](actions/list-presets.md) | `GET /presets.json` | [docs](https://auphonic.com/help/api/query.html#list-all-productions-and-presets) |
| [List Productions](actions/list-productions.md) | `GET /productions.json` | [docs](https://auphonic.com/help/api/query.html#list-all-productions-and-presets) |
| [List Services](actions/list-services.md) | `GET /services.json` | [docs](https://auphonic.com/help/api/details.html#query-external-services) |
| [Set Production Webhook](actions/set-production-webhook.md) | `POST /production/:uuid/webhook.json` | [docs](https://auphonic.com/help/api/webhook.html#add-a-webhook-to-a-production) |
| [Stop Production](actions/stop-production.md) | `POST /production/:uuid/stop.json` | [docs](https://auphonic.com/help/api/update.html#further-examples) |
| [Update Preset](actions/update-preset.md) | `POST /preset/:uuid.json` | [docs](https://auphonic.com/help/api/update.html#update-a-production-or-preset-and-reset-data) |
| [Update Production](actions/update-production.md) | `POST /production/:uuid.json` | [docs](https://auphonic.com/help/api/update.html#update-a-production-or-preset-and-reset-data) |
