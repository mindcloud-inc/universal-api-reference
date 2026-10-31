# Google Local Services: Native API Reference

A consolidated summary of Google Local Services's API configuration, with links to official documentation.

- **Official docs:** https://developers.google.com/local-services-ads/guides/local-services-api-overview
- **API base URL:** `https://localservices.googleapis.com/v1/`

## Authentication

### OAuth 2.0

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://accounts.google.com/o/oauth2/v2/auth to approve access.
2. Exchange the returned authorization code with a POST request to https://oauth2.googleapis.com/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `https://www.googleapis.com/auth/adwords`.

Refresh expired access tokens with a POST request to https://oauth2.googleapis.com/token.

[Official authentication documentation](https://developers.google.com/identity/protocols/oauth2)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Pagination

Use `pageSize` in the query string to set the page size (default 1000; accepted range 1000–10000).
