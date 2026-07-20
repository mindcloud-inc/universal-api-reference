# Landingi: Native API Reference

A consolidated summary of Landingi's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://api.landingi.com/v2/docs
- **OpenAPI specification:** https://api.landingi.com/v2/openapi
- **API base URL:** `https://api.landingi.com/v2`

## Authentication

### API Key

Authenticate with a Landingi static API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://landingi.com/help/new-zapier-integration/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `collection`. The total page count is read from `pagination.counter.total`. The current page number is read from `pagination.counter.current`.

## Pagination

Use `limit` in the query string to set the page size (default 10; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort` in the query string. Prefix the field name to select its direction. Only one sort field is accepted.

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Programmatic Process](actions/get-programmatic-process.md) | `GET /landing-page/programmatic/processes/:processUuid` | [docs](https://api.landingi.com/v2/docs#tag/programmatic-lp/operation/getProgrammaticLandingPageProcess) |
| [List Landing Pages for Programmatic Process](actions/list-landing-pages-for-programmatic-process.md) | `GET /landing-page/programmatic/processes/:processUuid/landing-pages` | [docs](https://api.landingi.com/v2/docs#tag/programmatic-lp/operation/getProgrammaticLandingPageProcessLandingPages) |
| [List Programmatic Processes](actions/list-programmatic-processes.md) | `GET /landing-page/programmatic/processes` | [docs](https://api.landingi.com/v2/docs#tag/programmatic-lp/operation/getProgrammaticLandingPageProcesses) |
| [Start Programmatic Process](actions/start-programmatic-process.md) | `POST /landing-page/programmatic/start` | [docs](https://api.landingi.com/v2/docs#tag/programmatic-lp/operation/startProgrammaticLandingPageProcess) |
