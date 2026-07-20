# ProAbono: Native API Reference

A consolidated summary of ProAbono's API configuration, with links to official documentation.

- **Official docs:** https://docs.proabono.com/api/
- **API base URL:** `https://api-1891.proabono.com`

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `SizePage` in the query string to set the page size (default 20). Use `page` in the query string to choose the page; numbering starts at 1.
