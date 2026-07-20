# Shorten.REST: Native API Reference

A consolidated summary of Shorten.REST's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://docs.shorten.rest/
- **OpenAPI specification:** https://docs.shorten.rest/swagger.json
- **API base URL:** `https://api.shorten.rest`

## Authentication

### API Key

Connect with a Shorten.REST API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://shorten.rest/knowledge-base/getting-started/where-to-find-your-api-key-on-your-shorten-rest-app-dashboard/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The next-page cursor is read from `lastId`.

## Pagination

Use `limit` in the query string to set the page size (default 1000; accepted range 1–1000). Use `continueFrom` in the query string as the pagination cursor.

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Alias](actions/create-alias.md) | `POST /aliases` | [docs](https://docs.shorten.rest/#POST--aliases) |
| [Delete Alias](actions/delete-alias.md) | `DELETE /aliases` | [docs](https://docs.shorten.rest/#DELETE--aliases) |
| [Get Alias](actions/get-alias.md) | `GET /aliases` | [docs](https://docs.shorten.rest/#GET--aliases) |
| [List Aliases by Domain](actions/list-aliases-by-domain.md) | `GET /aliases/all` | [docs](https://docs.shorten.rest/#GET--aliases-all) |
| [List Clicks](actions/list-clicks.md) | `GET /clicks` | [docs](https://docs.shorten.rest/#GET--clicks) |
| [Update Alias](actions/update-alias.md) | `PUT /aliases` | [docs](https://docs.shorten.rest/#PUT--aliases) |
