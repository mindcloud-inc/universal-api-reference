# Das Keyboard 5Q: Native API Reference

A consolidated summary of Das Keyboard 5Q's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://www.daskeyboard.io/q-api-doc/
- **API base URL:** `https://q2.daskeyboard.com/api/1.0`

## Authentication

### Q Cloud API Key

Authenticate Q Cloud requests with the Das Keyboard API key sent in the X-API-KEY request header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-KEY: <apiKey>
```

[Official authentication documentation](https://www.daskeyboard.io/q-api-doc/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The total page count is read from `totalPages`. The current page number is read from `number`.

## Pagination

Use `size` in the query string to set the page size (default 20; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 0.

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Signal](actions/create-signal.md) | `POST /signals` | [docs](https://www.daskeyboard.io/api-ressources/signal/create-signal/) |
| [Delete Signal](actions/delete-signal.md) | `DELETE /signals/:id` | [docs](https://www.daskeyboard.io/api-ressources/signal/delete-signal/) |
| [Delete Signal By Zone](actions/delete-signal-by-zone.md) | `DELETE /signals/pid/:pid/zoneId/:zoneId` | [docs](https://www.daskeyboard.io/api-ressources/signal/delete-signal-by-zone-id/) |
| [Get Signal By Zone](actions/get-signal-by-zone.md) | `GET /signals/pid/:pid/zoneId/:zoneId` | [docs](https://www.daskeyboard.io/api-ressources/signal/get-signal-by-zone-id/) |
| [Get Signal Color By Zone](actions/get-signal-color-by-zone.md) | `GET /signals/pid/:pid/zoneId/:zoneId/color` | [docs](https://www.daskeyboard.io/api-ressources/signal/get-signal-color-by-zone-id/) |
| [List Device Shadow Signals](actions/list-device-shadow-signals.md) | `GET /signals/pid/:pid/shadows` | [docs](https://www.daskeyboard.io/api-ressources/signal/get-shadow-signals-for-device/) |
| [List Shadow Signals](actions/list-shadow-signals.md) | `GET /signals/shadows` | [docs](https://www.daskeyboard.io/api-ressources/signal/get-all-shadow-signals/) |
| [List Signals](actions/list-signals.md) | `GET /signals` | [docs](https://www.daskeyboard.io/api-ressources/signal/get-signals/) |
