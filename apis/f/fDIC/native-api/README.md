# FDIC: Native API Reference

A consolidated summary of FDIC's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://api.fdic.gov/banks/docs
- **OpenAPI specification:** https://api.fdic.gov/banks/docs/swagger.yaml
- **API base URL:** `https://api.fdic.gov/banks`

## Authentication

### API Key

FDIC BankFind API key. FDIC currently accepts API queries without a key, but the OpenAPI specification exposes an optional api_key query parameter for key-backed requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.fdic.gov/banks/docs)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `limit` in the query string to set the page size (default 10; accepted range 0–10000). Use `offset` in the query string as the record offset; numbering starts at 0.

## Filtering

Send filters in the query string. Supported operators: `custom`.

## Sorting

Set the sort field with `sort_by` in the query string. Set the direction separately with `sort_order`. Use `ASC` for ascending order and `DESC` for descending order. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Bank Failures](actions/list-bank-failures.md) | `GET /failures` | [docs](https://api.fdic.gov/banks/docs) |
| [List Demographics Summary](actions/list-demographics-summary.md) | `GET /demographics` | [docs](https://api.fdic.gov/banks/docs) |
| [List Financial Institutions](actions/list-financial-institutions.md) | `GET /institutions` | [docs](https://api.fdic.gov/banks/docs) |
| [List Historical Aggregate Data](actions/list-historical-aggregate-data.md) | `GET /summary` | [docs](https://api.fdic.gov/banks/docs) |
| [List Institution Financials](actions/list-institution-financials.md) | `GET /financials` | [docs](https://api.fdic.gov/banks/docs) |
| [List Institution Locations](actions/list-institution-locations.md) | `GET /locations` | [docs](https://api.fdic.gov/banks/docs) |
| [List Structure Change Events](actions/list-structure-change-events.md) | `GET /history` | [docs](https://api.fdic.gov/banks/docs) |
| [List Summary Of Deposits](actions/list-summary-of-deposits.md) | `GET /sod` | [docs](https://api.fdic.gov/banks/docs) |
