# Zoho Survey: Native API Reference

A consolidated summary of Zoho Survey's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://help.zoho.com/portal/en/kb/survey/launch/distribution
- **API base URL:** `https://survey.zoho.com/api/v1/external-private`

## Authentication

### OAuth 2.0

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://accounts.zoho.com/oauth/v2/auth to approve access.
2. Exchange the returned authorization code with a POST request to {{credentials.authorizeRequest.["accounts-server"]}}/oauth/v2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `ZohoSurvey.invitation.CREATE,AaaServer.profile.READ,email`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to {{credentials.authorizeRequest.["accounts-server"]}}/oauth/v2/token.

[Official authentication documentation](https://www.zoho.com/accounts/protocol/oauth/web-server-applications.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get OAuth User Info](actions/get-oauth-user-info.md) | `GET {{credentials.authorizeRequest.["accounts-server"]}}/oauth/user/info` | [docs](https://www.zoho.com/accounts/protocol/oauth/use-access-token.html) |
