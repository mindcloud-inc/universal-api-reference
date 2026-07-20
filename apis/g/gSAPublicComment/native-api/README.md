# GSA Public Comment: Native API Reference

A consolidated summary of GSA Public Comment's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://open.gsa.gov/api/regulationsgov/
- **OpenAPI specification:** https://open.gsa.gov/api/regulationsgov/v4/openapi.yaml
- **API base URL:** `https://api.regulations.gov/v4`

## Authentication

### API Key

Use an api.data.gov API key for Regulations.gov requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://open.gsa.gov/api/regulationsgov/#getting-started)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.api+json` |

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `page[size]` in the query string to set the page size (default 25; accepted range 5–250). Use `page[number]` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort` in the query string. Prefix the field name to select its direction. Multiple sort fields can be combined.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Comment](actions/get-comment.md) | `GET /comments/:commentId` | [docs](https://open.gsa.gov/api/regulationsgov/#detailed-information-for-a-single-comment) |
| [Get Docket](actions/get-docket.md) | `GET /dockets/:docketId` | [docs](https://open.gsa.gov/api/regulationsgov/#detailed-information-for-a-single-docket) |
| [Get Document](actions/get-document.md) | `GET /documents/:documentId` | [docs](https://open.gsa.gov/api/regulationsgov/#detailed-information-for-a-single-document) |
| [List Agency Categories](actions/list-agency-categories.md) | `GET /agency-categories` | [docs](https://open.gsa.gov/api/regulationsgov/) |
| [List Comments](actions/list-comments.md) | `GET /comments` | [docs](https://open.gsa.gov/api/regulationsgov/#searching-for-comments) |
| [List Dockets](actions/list-dockets.md) | `GET /dockets` | [docs](https://open.gsa.gov/api/regulationsgov/#searching-for-dockets) |
| [List Documents](actions/list-documents.md) | `GET /documents` | [docs](https://open.gsa.gov/api/regulationsgov/#searching-for-documents) |
