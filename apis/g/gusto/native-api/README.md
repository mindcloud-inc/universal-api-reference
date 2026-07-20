# Gusto: Native API Reference

A consolidated summary of Gusto's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://docs.gusto.com/app-integrations/reference
- **API base URL:** `https://api.gusto-demo.com`

## Authentication

### OAuth2

OAuth2 company access tokens for the Gusto App Integrations API demo environment.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://api.gusto-demo.com/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://api.gusto-demo.com/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `public webhook_subscriptions:read webhook_subscriptions:write`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://api.gusto-demo.com/oauth/token.

[Official authentication documentation](https://docs.gusto.com/app-integrations/docs/oauth2)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Token Info](actions/get-token-info.md) | `GET /v1/token_info` | [docs](https://docs.gusto.com/app-integrations/reference/get-v1-token-info) |
