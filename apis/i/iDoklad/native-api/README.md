# iDoklad: Native API Reference

A consolidated summary of iDoklad's API configuration, with links to official documentation.

- **Official docs:** https://api.idoklad.cz/Help/v3/cs/
- **API base URL:** `https://api.idoklad.cz/v3`

## Authentication

### OAuth2

Use iDoklad client credentials for server-to-server access. The connection must include application_id from the Developer Portal and tenant client_id/client_secret from iDoklad Settings > Applications/API.

### Credentials

- **Application ID:** `applicationId` · required · Application ID from the iDoklad Developer Portal.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://identity.idoklad.cz/server/v2/connect/token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `idoklad_api offline_access`.

A machine-to-machine flow is configured.

[Official authentication documentation](https://api.idoklad.cz/Help/v3/cs/#api-ClienCredentialsFlow)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `pageSize` in the query string to set the page size (default 20; maximum 200). Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string. Supported operators: `ct`, `eq`, `gt`, `gte`, `lt`, `lte`.

## Sorting

Set the sort field with `sort` in the query string. Use `asc` for ascending order and `desc` for descending order. Multiple sort fields can be combined.

## Retry behavior

Retry responses with status codes `429,500,502,503`. Wait 500 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.
