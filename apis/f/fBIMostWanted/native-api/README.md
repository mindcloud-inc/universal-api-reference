# FBI Most Wanted: Native API Reference

A consolidated summary of FBI Most Wanted's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://www.fbi.gov/wanted/api
- **API base URL:** `https://api.fbi.gov/wanted/v1`

## Authentication

### No Authentication

The FBI Wanted API is a public REST endpoint and does not require credentials for documented read access.

This API does not require request authentication.

[Official authentication documentation](https://www.fbi.gov/wanted/api)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `User-Agent` | `MindCloud/1.0 (+https://www.mindcloud.co)` |

Responses from this API use JSON. Response data is read from `items`. The current page number is read from `page`.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string. Supported operators: `eq`.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Wanted Records](actions/list-wanted-records.md) | `GET /list` | [docs](https://www.fbi.gov/wanted/api) |
