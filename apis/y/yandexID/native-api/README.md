# Yandex ID: Native API Reference

A consolidated summary of Yandex ID's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://yandex.com/dev/id/doc/en/
- **API base URL:** `https://login.yandex.ru`

## Authentication

### Yandex OAuth

OAuth 2.0 for Yandex ID user login and profile access.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://oauth.yandex.com/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://oauth.yandex.com/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `login:info login:email login:avatar`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://oauth.yandex.com/token.

[Official authentication documentation](https://yandex.com/dev/id/doc/en/how-to)

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Authenticated User](actions/get-authenticated-user.md) | `GET /info` | [docs](https://yandex.com/dev/id/doc/en/user-information) |
