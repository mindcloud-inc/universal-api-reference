# Extensiv 3PL Warehouse: Native API Reference

A consolidated summary of Extensiv 3PL Warehouse's API configuration, with links to official documentation.

- **Official docs:** https://developer.3plcentral.com/#34586810-c20c-410d-9295-9ae07aa10c54
- **OpenAPI specification:** https://developer.3plcentral.com/api/collections/8399762/SVn3tFsv?segregateAuth=true&versionTag=latest
- **API base URL:** `{connection}`

## Authentication

### REST API Token

Uses Extensiv REST API keys to request and refresh temporary bearer tokens through the documented token endpoint.

### Credentials

- **Client ID:** `clientId` · required
- **Client Secret:** `clientSecret` · required
- **User Login ID:** `userLoginId` · required · The Extensiv UserLogin ID supplied by the warehouse for API audit visibility.
- **Connection:** `connection` · required

Send these headers with each API request:

```http
Authorization: Bearer <custom.accessToken>
```

[Official authentication documentation](https://help.extensiv.com/rest-api/providing-rest-api-access)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/hal+json` |
| `Content-Type` | `application/json; charset=utf-8` |

Responses from this API use JSON.

## Pagination

Use `pgsiz` in the query string to set the page size (default 100; accepted range 1–1000). Use `pgnum` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort` in the query string. Only one sort field is accepted.
