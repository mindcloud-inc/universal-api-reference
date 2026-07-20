# Lnk.Bio: Native API Reference

A consolidated summary of Lnk.Bio's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://api.lnk.bio/
- **API base URL:** `https://lnk.bio/oauth/v1`

## Authentication

### OAuth2

Lnk.Bio public app access using OAuth2 authorization code.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://lnk.bio/manage/access to approve access.
2. Exchange the returned authorization code with a POST request to https://lnk.bio/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `basic`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://lnk.bio/oauth/token.

[Official authentication documentation](https://api.lnk.bio/doc-498662)

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Lnk](actions/create-lnk.md) | `POST /lnk/add` | [docs](https://api.lnk.bio/api-6746008) |
| [Delete Lnk](actions/delete-lnk.md) | `POST /lnk/delete` | [docs](https://api.lnk.bio/api-6746009) |
| [List Lnk Groups](actions/list-lnk-groups.md) | `GET /group/list` | [docs](https://api.lnk.bio/api-6746010) |
| [List Lnks](actions/list-lnks.md) | `GET /lnk/list` | [docs](https://api.lnk.bio/api-6746007) |
| [Retrieve Basic Profile Info](actions/retrieve-basic-profile-info.md) | `GET /me` | [docs](https://api.lnk.bio/api-6746006) |
