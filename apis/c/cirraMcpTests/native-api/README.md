# Cirra MCP Tests - Do Not Delete: Native API Reference

A consolidated summary of Cirra MCP Tests - Do Not Delete's API configuration and 4 documented operations.

- **REST - Offset Pagination base URL:** `https://api.mindcloud.co/v1/internal/cirra/tests`
- **REST - Cursor Pagination base URL:** `https://api.mindcloud.co/v1/internal/cirra/tests`
- **REST - Page 0 Index Pagination base URL:** `https://api.mindcloud.co/v1/internal/cirra/tests`
- **REST - Page 1 Index Pagination base URL:** `https://api.mindcloud.co/v1/internal/cirra/tests`

## Authentication

### None

This API does not require request authentication.

## API conventions

### REST - Offset Pagination

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `data`.

### REST - Cursor Pagination

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `data`. The next-page cursor is read from `meta.cursor`.

### REST - Page 0 Index Pagination

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `data`.

### REST - Page 1 Index Pagination

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `data`.

## Pagination

- **REST - Offset Pagination:** Use `limit` in the query string to set the page size (default 10; accepted range 1–100). Use `offset` in the query string as the record offset; numbering starts at 0.
- **REST - Cursor Pagination:** Use `limit` in the query string to set the page size (default 10; accepted range 1–100). Use `cursor` in the query string as the pagination cursor.
- **REST - Page 0 Index Pagination:** Use `limit` in the query string to set the page size (default 10; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 0.
- **REST - Page 1 Index Pagination:** Use `limit` in the query string to set the page size (default 10; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (4 documented)

| Operation | API | Method & path | Vendor docs |
| --- | --- | --- | --- |
| [Pagination Cursor](actions/pagination-cursor.md) | REST - Cursor Pagination | `GET /pagination-t1-cursor` |  |
| [Pagination Offset](actions/pagination-offset.md) | REST - Offset Pagination | `GET /pagination-t1-offset` | [docs](https://github.com/mindcloud-inc/gravity/blob/master/docs/cirra/projects/api/domains/cirra-tests-pagination-t1.md) |
| [Pagination Page 1 Index](actions/pagination-page-one-index.md) | REST - Page 1 Index Pagination | `GET /pagination-t1-page-one-index` |  |
| [Pagination Page 0 Index](actions/pagination-page-zero-index.md) | REST - Page 0 Index Pagination | `GET /pagination-t1-page-zero-index` |  |
