# LaMetric: Native API Reference

A consolidated summary of LaMetric's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://lametric-documentation.readthedocs.io/en/latest/
- **API base URL:** `https://developer.lametric.com`

## Authentication

### OAuth2

LaMetric uses explicit OAuth2 for cloud APIs. The cloud scopes are basic, devices_read, and devices_write.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://developer.lametric.com/api/v2/oauth2/authorize/ to approve access.
2. Exchange the returned authorization code with a POST request to https://developer.lametric.com/api/v2/oauth2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `basic devices_read devices_write`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://developer.lametric.com/api/v2/oauth2/token.

[Official authentication documentation](https://lametric-documentation.readthedocs.io/en/latest/reference-docs/cloud-authorization.html)

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get User Profile](actions/get-user-profile.md) | `GET /api/v2/users/me` | [docs](https://lametric-documentation.readthedocs.io/en/latest/reference-docs/cloud-users.html#get-user) |
| [List Devices](actions/list-devices.md) | `GET /api/v2/users/me/devices` | [docs](https://lametric-documentation.readthedocs.io/en/latest/reference-docs/cloud-users.html#get-devices) |
