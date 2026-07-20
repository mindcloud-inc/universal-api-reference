# Airtable: Native API Reference

A consolidated summary of Airtable's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://airtable.com/developers/web/api
- **API base URL:** `https://api.airtable.com/v0`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://support.airtable.com/docs/creating-personal-access-tokens)

### OAuth 2.0

Authenticate with Airtable via OAuth 2.0

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://airtable.com/oauth2/v1/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://airtable.com/oauth2/v1/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `schema.bases:read schema.bases:write data.records:read data.records:write`.

PKCE is enabled. The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://airtable.com/oauth2/v1/token.

[Official authentication documentation](https://airtable.com/developers/web/api/oauth-reference)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Pagination

Use `pageSize` in the query string to set the page size (default 100; maximum 100). Use `offset` in the query string as the pagination cursor; numbering starts at 0.

## Retry behavior

Wait 70000 ms before the first retry.

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Record](actions/create-record.md) | `POST /:baseId/:tableId` | [docs](https://airtable.com/developers/web/api/create-records) |
| [Create Table](actions/create-table.md) | `POST /meta/bases/:baseId/tables` | [docs](https://airtable.com/developers/web/api/create-table) |
| [Get Record](actions/get-record.md) | `GET /:baseId/:tableId/:recordId` | [docs](https://airtable.com/developers/web/api/get-record) |
| [List Bases](actions/list-bases.md) | `GET /meta/bases` | [docs](https://airtable.com/developers/web/api/list-bases) |
| [List Records](actions/list-records.md) | `GET /:baseId/:tableId` | [docs](https://airtable.com/developers/web/api/list-records) |
| [List Records - Compact](actions/list-records-compact.md) | `POST /:baseId/:tableId/listRecords` | [docs](https://airtable.com/developers/web/api/list-records) |
| [Update Multiple Records](actions/update-multiple-records.md) | `PATCH /:baseId/:tableIdOrName` | [docs](https://airtable.com/developers/web/api/update-multiple-records) |
| [Update Record](actions/update-record.md) | `PATCH /:baseId/:tableId/:recordId` | [docs](https://airtable.com/developers/web/api/update-record) |
