# myUplink: Native API Reference

A consolidated summary of myUplink's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://dev.myuplink.com/documentation/intro?activeTab=intro
- **API base URL:** `https://api.myuplink.com`

## Authentication

### OAuth2

Connect with OAuth2 authorization code to access the user's myUplink systems and devices.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://api.myuplink.com/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://api.myuplink.com/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `READSYSTEM WRITESYSTEM`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://api.myuplink.com/oauth/token.

[Official authentication documentation](https://dev.myuplink.com/documentation/auth?activeTab=auth)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON. The current page number is read from `page`.

## Pagination

Use `itemsPerPage` in the query string to set the page size (default 100; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get My Systems](actions/get-my-systems.md) | `GET /v2/systems/me` | [docs](https://dev.myuplink.com/swagger/index.html) |
| [Test API Availability](actions/test-api-availability.md) | `GET /v2/ping` | [docs](https://dev.myuplink.com/swagger/index.html) |
| [Test Authorized API Availability](actions/test-authorized-api-availability.md) | `GET /v2/protected-ping` | [docs](https://dev.myuplink.com/swagger/index.html) |
