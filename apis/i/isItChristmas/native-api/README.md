# Is It Christmas?: Native API Reference

A consolidated summary of Is It Christmas?'s API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://github.com/isitchristmas/web
- **API base URL:** `https://isitchristmas.com`

## Authentication

### No Authentication

Public Is It Christmas endpoints require no authentication.

This API does not require request authentication.

[Official authentication documentation](https://github.com/isitchristmas/web/blob/master/api.js)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `christmases`.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Christmases](actions/list-christmases.md) | `GET /api` | [docs](https://github.com/isitchristmas/web/blob/master/api.js) |
