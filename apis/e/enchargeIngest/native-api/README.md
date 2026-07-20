# Encharge Ingest: Native API Reference

A consolidated summary of Encharge Ingest's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://docs.encharge.io/getting-started/connecting-your-app-to-encharge/ingest-api
- **API base URL:** `https://ingest.encharge.io/v1`

## Authentication

### Write Key

Connect to Encharge Ingest with your account write key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-Encharge-Token: <apiKey>
```

[Official authentication documentation](https://docs.encharge.io/getting-started/connecting-your-app-to-encharge/ingest-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Alias Person](actions/alias-person.md) | `POST /` | [docs](https://docs.encharge.io/getting-started/connecting-your-app-to-encharge/ingest-api) |
| [Group Object](actions/group-object.md) | `POST /` | [docs](https://docs.encharge.io/getting-started/connecting-your-app-to-encharge/ingest-api) |
| [Identify Person](actions/identify-person.md) | `POST /` | [docs](https://docs.encharge.io/getting-started/connecting-your-app-to-encharge/ingest-api) |
| [Send Event](actions/send-event.md) | `POST /` | [docs](https://docs.encharge.io/getting-started/connecting-your-app-to-encharge/ingest-api) |
