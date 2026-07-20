# CompanyHub: Native API Reference

A consolidated summary of CompanyHub's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://companyhub.com/docs/api-documentation
- **API base URL:** `https://api.companyhub.com/v1`

## Authentication

### API Key

CompanyHub API key authentication with subdomain-based Authorization header

### Credentials

- **API Key:** `apiKey` · required
- **Subdomain:** `subdomain` · required · Your CompanyHub subdomain without spaces, for example mindcloud.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://companyhub.com/docs/api-documentation)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `limit` in the query string to set the page size. Use `start` in the query string as the record offset.

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Record](actions/create-record.md) | `POST /tables/:tableName` | [docs](https://companyhub.com/docs/api-documentation#resources) |
| [Delete Records](actions/delete-records.md) | `DELETE /tables/:tableName` | [docs](https://companyhub.com/docs/api-documentation#resources) |
| [Get Current User](actions/get-current-user.md) | `GET /me` | [docs](https://companyhub.com/docs/api-documentation#resources) |
| [Get Record](actions/get-record.md) | `GET /tables/:tableName/:id` | [docs](https://companyhub.com/docs/api-documentation#resources) |
| [List Records](actions/list-records.md) | `GET /tables/:tableName` | [docs](https://companyhub.com/docs/api-documentation#resources) |
| [Search Records](actions/search-records.md) | `GET /tables/:tableName` | [docs](https://companyhub.com/docs/api-documentation#howToFilterRecords) |
| [Search Records by Exact Match](actions/search-records-by-exact-match.md) | `POST /tables/:tableName/search` | [docs](https://companyhub.com/docs/api-documentation#howToFilterRecords) |
| [Update Record](actions/update-record.md) | `PUT /tables/:tableName/:id` | [docs](https://companyhub.com/docs/api-documentation#resources) |
