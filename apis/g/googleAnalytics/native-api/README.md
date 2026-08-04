# Google Analytics: Native API Reference

A consolidated summary of Google Analytics's API configuration and 2 documented operations.

- **API base URL:** `https://www.googleapis.com/analytics/v3/`

## Authentication

### OAuth 2.0

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://accounts.google.com/o/oauth2/auth to approve access.
2. Exchange the returned authorization code with a POST request to https://oauth2.googleapis.com/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `https://www.googleapis.com/auth/analytics openid https://www.googleapis.com/auth/userinfo.email https://www.googleapis.com/auth/userinfo.profile`.

Refresh expired access tokens with a POST request to https://oauth2.googleapis.com/token.

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Pagination

Use `limit` in the request body to set the page size (default 1000).

## Endpoints (2 documented)

| Operation | Method & path |
| --- | --- |
| [List Account Summaries](actions/list-account-summaries.md) | `GET https://analyticsadmin.googleapis.com/v1beta/accountSummaries` |
| [List Accounts](actions/list-accounts.md) | `GET https://analyticsadmin.googleapis.com/v1beta/accounts` |
