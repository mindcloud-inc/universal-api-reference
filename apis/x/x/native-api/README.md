# X: Native API Reference

A consolidated summary of X's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://docs.x.com/x-api
- **OpenAPI specification:** https://api.x.com/2/openapi.json
- **API base URL:** `https://api.x.com`

## Authentication

### OAuth 2.0

OAuth 2.0 user-context authentication for X API

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://x.com/i/oauth2/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://api.x.com/2/oauth2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `tweet.read tweet.write users.read offline.access`.

PKCE is enabled. The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://api.x.com/2/oauth2/token.

[Official authentication documentation](https://docs.x.com/fundamentals/authentication/oauth-2-0/authorization-code)

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Post](actions/create-post.md) | `POST /2/tweets` | [docs](https://docs.x.com/x-api/posts/create-post) |
| [Get My Profile](actions/get-my-profile.md) | `GET /2/users/me` | [docs](https://docs.x.com/x-api/users/lookup/api-reference/get-users-me) |
