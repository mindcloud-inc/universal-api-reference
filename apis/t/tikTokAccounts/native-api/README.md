# TikTok Accounts: Native API Reference

A consolidated summary of TikTok Accounts's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://developers.tiktok.com/doc/tiktok-api-v2-get-user-info/
- **API base URL:** `https://open.tiktokapis.com`

## Authentication

### OAuth 2.0

Connect with TikTok OAuth 2.0.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://www.tiktok.com/v2/auth/authorize/ to approve access.
2. Exchange the returned authorization code with a POST request to https://open.tiktokapis.com/v2/oauth/token/.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `user.info.basic`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://open.tiktokapis.com/v2/oauth/token/.

[Official authentication documentation](https://developers.tiktok.com/doc/oauth-user-access-token-management)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `data.user`.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get User Info](actions/get-user-info.md) | `GET /v2/user/info/` | [docs](https://developers.tiktok.com/doc/tiktok-api-v2-get-user-info/) |
