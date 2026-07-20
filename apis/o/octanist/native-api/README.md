# Octanist: Native API Reference

A consolidated summary of Octanist's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://octanist.com/docs/api-reference/introduction
- **API base URL:** `https://octanist.com/api`

## Authentication

### API Key

Authenticate Octanist requests with an organization-scoped API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-KEY: <apiKey>
```

[Official authentication documentation](https://octanist.com/docs/api-reference/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The total page count is read from `meta.pagination.totalPages`. The current page number is read from `meta.pagination.page`.

## Pagination

Use `limit` in the query string to set the page size (default 50; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string. Supported operators: `eq`, `exists`, `gt`, `gte`, `lt`, `lte`.

## Sorting

Set the sort field with `sort` in the query string. Use `asc` for ascending order and `desc` for descending order. Multiple sort fields can be combined.

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check API Key](actions/check-api-key.md) | `POST /check` | [docs](https://octanist.com/docs/api-reference/endpoint/check) |
| [Create Lead](actions/create-lead.md) | `POST /leads` | [docs](https://octanist.com/docs/api-reference/endpoint/create-lead) |
| [Get Ad Spend](actions/get-ad-spend.md) | `POST /ad-spend` | [docs](https://octanist.com/docs/api-reference/endpoint/ad-spend) |
| [Get Lead by ID](actions/get-lead-by-id.md) | `GET /leads/{id}` | [docs](https://octanist.com/docs/api-reference/endpoint/get-lead) |
| [Get Stats](actions/get-stats.md) | `POST /stats` | [docs](https://octanist.com/docs/api-reference/endpoint/stats) |
| [List Leads](actions/list-leads.md) | `GET /leads` | [docs](https://octanist.com/docs/api-reference/endpoint/get-leads) |
| [Update Lead](actions/update-lead.md) | `PATCH /leads` | [docs](https://octanist.com/docs/api-reference/endpoint/update-lead) |
