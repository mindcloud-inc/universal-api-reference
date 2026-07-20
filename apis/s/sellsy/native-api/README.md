# Sellsy: Native API Reference

A consolidated summary of Sellsy's API configuration, with links to official documentation.

- **Official docs:** https://docs.sellsy.com/api/v2/
- **OpenAPI specification:** https://docs.sellsy.com/api/v2/dist/sellsy.v2.latest.yaml
- **API base URL:** `https://api.sellsy.com/v2`

## Authentication

### OAuth 2.0 (Client Credentials)

Connect Sellsy using a personal OAuth 2.0 client with the client credentials grant.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://login.sellsy.com/oauth2/authorization to approve access.
2. Exchange the returned authorization code with a POST request to https://login.sellsy.com/oauth2/access-tokens.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `comments.read comments.write companies.read companies.write contacts.read contacts.write opportunities.read opportunities.write tasks.read tasks.write estimates.read orders.read`.

Refresh expired access tokens with a POST request to https://login.sellsy.com/oauth2/access-tokens. A machine-to-machine flow is configured.

[Official authentication documentation](https://docs.sellsy.com/api/v2/#section/Authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

The next-page cursor is read from `pagination.offset`.

## Pagination

Use `limit` in the query string to set the page size. Use `offset` in the query string as the pagination cursor.

## Sorting

Set the sort field with `order` in the query string. Set the direction separately with `direction`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.
