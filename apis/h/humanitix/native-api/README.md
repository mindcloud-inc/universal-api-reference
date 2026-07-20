# Humanitix: Native API Reference

A consolidated summary of Humanitix's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://humanitix.stoplight.io/docs/humanitix-public-api/e508a657c1467-humanitix-public-api
- **API base URL:** `https://api.humanitix.com/v1`

## Authentication

### API Key

Connect with a Humanitix Public API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://humanitix.stoplight.io/docs/humanitix-public-api/e508a657c1467-humanitix-public-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The current page number is read from `page`.

## Pagination

Use `pageSize` in the query string to set the page size (default 100; minimum 1). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Event](actions/get-event.md) | `GET /events/:eventId` | [docs](https://humanitix.stoplight.io/docs/humanitix-public-api/970584136120e-get-event) |
| [Get Order](actions/get-order.md) | `GET /events/:eventId/orders/:orderId` | [docs](https://humanitix.stoplight.io/docs/humanitix-public-api/3be38b97d385c-get-order) |
| [List Events](actions/list-events.md) | `GET /events` | [docs](https://humanitix.stoplight.io/docs/humanitix-public-api/476881e4b5d55-get-events) |
| [List Orders](actions/list-orders.md) | `GET /events/:eventId/orders` | [docs](https://humanitix.stoplight.io/docs/humanitix-public-api/468f50b741494-get-orders) |
