# Hipsy: Native API Reference

A consolidated summary of Hipsy's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://docs.hipsy.nl/api-reference/getting-started
- **API base URL:** `https://api.hipsy.nl/v1`

## Authentication

### API Key

Use a Hipsy API key for account access.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.hipsy.nl/the-api-key)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`. The total page count is read from `meta.last_page`. The current page number is read from `meta.current_page`.

## Pagination

Use `limit` in the query string to set the page size (default 25; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Events](actions/list-events.md) | `GET /organisation/:organisationSlug/events` | [docs](https://docs.hipsy.nl/api-reference/list-events) |
| [List Orders](actions/list-orders.md) | `GET /organisation/:organisationSlug/orders` | [docs](https://docs.hipsy.nl/api-reference/list-orders) |
| [List Organisations](actions/list-organisations.md) | `GET /organisations/index` | [docs](https://docs.hipsy.nl/api-reference/list-organisations) |
