# Emailchaser: Native API Reference

A consolidated summary of Emailchaser's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://run.emailchaser.com
- **OpenAPI specification:** https://openapi.gitbook.com/o/pCbc8OJU0aG1uHvE5p9b/spec/emailchaser-api.json
- **API base URL:** `https://api.emailchaser.com/r`

## Authentication

### API Key

Connect Emailchaser with an API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://run.emailchaser.com/getting-started/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Campaigns](actions/list-campaigns.md) | `GET /campaigns` | [docs](https://run.emailchaser.com/api-reference/campaigns) |
