# Adalo: Native API Reference

A consolidated summary of Adalo's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://help.adalo.com/integrations/the-adalo-api
- **API base URL:** `https://api.adalo.com`

## Authentication

### API Key

Connect with an Adalo app API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.adalo.com/integrations/the-adalo-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `limit` in the query string to set the page size. Use `offset` in the query string as the record offset.

## Filtering

Send filters in the query string.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Collection Records](actions/list-collection-records.md) | `GET /v0/apps/:appId/collections/:collectionId` | [docs](https://help.adalo.com/integrations/the-adalo-api/collections) |
