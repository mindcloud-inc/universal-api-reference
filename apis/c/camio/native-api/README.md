# Camio: Native API Reference

A consolidated summary of Camio's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://api.camio.com/
- **API base URL:** `https://camio.com/api`

## Authentication

### OAuth2

Connect your Camio account with OAuth2.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://camio.com/api/login/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://camio.com/api/login/oauth/access_token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `user,settings,settings:read,settings:write,settings:recording,settings:recording:read,settings:recording:write`.

[Official authentication documentation](https://api.camio.com/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Camio](actions/create-camio.md) | `PUT /users/me/camios` | [docs](https://api.camio.com/#create-camio) |
| [Create Pinned Query](actions/create-pinned-query.md) | `PUT /users/:user/queries/pinned` | [docs](https://api.camio.com/#create-a-pinned-query) |
| [Delete Camio](actions/delete-camio.md) | `DELETE /users/me/camios` | [docs](https://api.camio.com/#delete-camio) |
| [Delete Pinned Query](actions/delete-pinned-query.md) | `DELETE /users/:user/queries/pinned/:id` | [docs](https://api.camio.com/#deleta-a-pinned-query) |
| [Get Camio](actions/get-camio.md) | `GET /users/me/camios` | [docs](https://api.camio.com/#get-a-camio) |
| [Get Current Account](actions/get-current-account.md) | `GET /accounts` | [docs](https://api.camio.com/#get-an-account) |
| [Get Current User](actions/get-current-user.md) | `GET /users/:user` | [docs](https://api.camio.com/#get-a-user) |
| [Get Profile](actions/get-profile.md) | `GET /users/:user/profile` | [docs](https://api.camio.com/#get-a-profile) |
| [Get Settings](actions/get-settings.md) | `GET /users/:user/settings` | [docs](https://api.camio.com/#get-settings) |
| [Get Upload Token](actions/get-upload-token.md) | `GET /users/me/tokens/upload` | [docs](https://api.camio.com/#get-upload-token) |
| [List Camios](actions/list-camios.md) | `GET /users/me/camios` | [docs](https://api.camio.com/#list-all-camios) |
| [List Connected Cameras](actions/list-connected-cameras.md) | `GET /users/me/cameras/` | [docs](https://api.camio.com/#list-connected-cameras) |
| [List Devices](actions/list-devices.md) | `GET /devices` | [docs](https://api.camio.com/#list-all-devices) |
| [List Pinned Queries](actions/list-pinned-queries.md) | `GET /users/:user/queries/pinned` | [docs](https://api.camio.com/#list-pinned-queries) |
| [List User Accounts](actions/list-user-accounts.md) | `GET /users/:user/accounts` | [docs](https://api.camio.com/#list-users-accounts) |
| [Search Cameras](actions/search-cameras.md) | `GET /search/cameras` | [docs](https://api.camio.com/#search-cameras) |
| [Search Events](actions/search-events.md) | `GET /search` | [docs](https://api.camio.com/#search-video) |
| [Update Camio Collaborators](actions/update-camio-collaborators.md) | `POST /users/me/camios` | [docs](https://api.camio.com/#update-a-camio) |
| [Update Profile](actions/update-profile.md) | `POST /users/:user/profile` | [docs](https://api.camio.com/#create-a-profile) |
| [Update Settings](actions/update-settings.md) | `POST /users/:user/settings` | [docs](https://api.camio.com/#update-settings) |
