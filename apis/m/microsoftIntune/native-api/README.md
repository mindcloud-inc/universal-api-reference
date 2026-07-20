# Microsoft Intune: Native API Reference

A consolidated summary of Microsoft Intune's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://learn.microsoft.com/en-us/graph/api/resources/intune-graph-overview?view=graph-rest-1.0
- **API base URL:** `https://graph.microsoft.com`

## Authentication

### OAuth 2.0

Connect to Microsoft Intune through Microsoft Graph using the Microsoft identity platform authorization-code flow.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://login.microsoftonline.com/organizations/oauth2/v2.0/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://login.microsoftonline.com/organizations/oauth2/v2.0/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `offline_access User.Read DeviceManagementManagedDevices.Read.All DeviceManagementApps.Read.All DeviceManagementConfiguration.Read.All`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://login.microsoftonline.com/organizations/oauth2/v2.0/token.

[Official authentication documentation](https://learn.microsoft.com/en-us/entra/identity-platform/v2-oauth2-auth-code-flow)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get My Profile](actions/get-my-profile.md) | `GET /v1.0/me` | [docs](https://learn.microsoft.com/en-us/graph/api/user-get?view=graph-rest-1.0) |
