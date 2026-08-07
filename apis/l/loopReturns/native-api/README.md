# Loop Returns: Native API Reference

A consolidated summary of Loop Returns's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://docs.loopreturns.com/api-reference/authentication
- **API base URL:** `https://api.loopreturns.com/api/v1`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-Authorization: <apiKey>
```

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

The next-page cursor is read from `nextPageUrl`.

## Pagination

Use `pageSize` in the query string to set the page size (default 500; accepted range 1–500). Follow the complete next-page URL returned by the API.

## Retry behavior

Retry responses with status codes `429, 500, 502, 503, 524`. Wait 5000 ms before the first retry. Stop after 5 attempts. Multiply the delay by 3 after each failed attempt.

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Flag Return](actions/flag-return.md) | `POST https://api.loopreturns.com/api/v1/warehouse/return/{{return_id}}/flag` | [docs](https://docs.loopreturns.com/api-reference/latest/return-actions/flag-return) |
| [List Destinations](actions/list-destinations.md) | `GET /destinations` | [docs](https://docs.loopreturns.com/api-reference/latest/destinations/get-all-destinations) |
| [Get Return Details](actions/list-return-details.md) | `GET /warehouse/return/details` | [docs](https://docs.loopreturns.com/api-reference/latest/return-data/get-return-details) |
| [List Returns](actions/list-returns.md) | `GET /warehouse/return/list` | [docs](https://docs.loopreturns.com/api-reference/latest/return-data/detailed-returns-list) |
| [Process Return](actions/process-return.md) | `POST https://api.loopreturns.com/api/v1/warehouse/return/{{return_id}}/process` | [docs](https://docs.loopreturns.com/api-reference/latest/return-actions/process-return) |
