# ShareFile: Native API Reference

A consolidated summary of ShareFile's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://api.sharefile.com/docs
- **API base URL:** `https://{subdomain}.{apicp}/sf/v3`

## Authentication

### OAuth 2

Authenticate with ShareFile using OAuth 2.0 authorization code flow.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://secure.sharefile.com/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://secure.sharefile.com/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://{{credentials.accessTokenRequest.subdomain}}.{{credentials.accessTokenRequest.apicp}}/oauth/token.

[Official authentication documentation](https://api.sharefile.com/gettingstarted/oauth2)

## Pagination

Use `$top` in the query string to set the page size (default 50; accepted range 1–200). Use `$skip` in the query string as the record offset; numbering starts at 0.

## Filtering

Send filters in the query string. Supported operators: `contains`, `eq`, `gt`, `gte`, `lt`, `lte`, `ne`.

## Sorting

Set the sort field with `$orderby` in the query string. Multiple sort fields can be combined.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 500 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Client User](actions/create-client-user.md) | `POST /Users` | [docs](https://api.sharefile.com/html/docs/Users.html) |
| [Create Folder](actions/create-folder.md) | `POST /Items({{id}})/Folder` | [docs](https://api.sharefile.com/html/docs/Items.html) |
| [Create Group](actions/create-group.md) | `POST /Groups` | [docs](https://api.sharefile.com/html/docs/Groups.html) |
| [Delete Group](actions/delete-group.md) | `DELETE /Groups({{id}})` | [docs](https://api.sharefile.com/html/docs/Groups.html) |
| [Delete Item](actions/delete-item.md) | `DELETE /Items({{id}})` | [docs](https://api.sharefile.com/html/docs/Items.html) |
| [Delete Share](actions/delete-share.md) | `DELETE /Shares({{id}})` | [docs](https://api.sharefile.com/html/docs/Shares.html) |
| [Delete User](actions/delete-user.md) | `DELETE /Users({{id}})` | [docs](https://api.sharefile.com/html/docs/Users.html) |
| [Get Account](actions/get-account.md) | `GET /Accounts({{id}})` | [docs](https://api.sharefile.com/html/docs/Accounts.html) |
| [Get Current Account](actions/get-current-account.md) | `GET /Accounts` | [docs](https://api.sharefile.com/html/docs/Accounts.html) |
| [Get Current User](actions/get-current-user.md) | `GET /Users` | [docs](https://api.sharefile.com/html/docs/Users.html) |
| [Get Group](actions/get-group.md) | `GET /Groups({{id}})` | [docs](https://api.sharefile.com/html/docs/Groups.html) |
| [Get Home Folder for Current User](actions/get-home-folder-for-current-user.md) | `GET /Items` | [docs](https://api.sharefile.com/html/docs/Items.html) |
| [Get Item](actions/get-item.md) | `GET /Items({{id}})` | [docs](https://api.sharefile.com/html/docs/Items.html) |
| [Get Session](actions/get-session.md) | `GET /Sessions` | [docs](https://api.sharefile.com/html/docs/Sessions.html) |
| [Get Share](actions/get-share.md) | `GET /Shares({{id}})` | [docs](https://api.sharefile.com/html/docs/Shares.html) |
| [Get User](actions/get-user.md) | `GET /Users({{id}})` | [docs](https://api.sharefile.com/html/docs/Users.html) |
| [Get Zone](actions/get-zone.md) | `GET /Zones({{id}})` | [docs](https://api.sharefile.com/html/docs/Zones.html) |
| [List Groups](actions/list-groups.md) | `GET /Groups` | [docs](https://api.sharefile.com/html/docs/Groups.html) |
| [List Item Children](actions/list-item-children.md) | `GET /Items({{id}})/Children` | [docs](https://api.sharefile.com/html/docs/Items.html) |
| [List Shares](actions/list-shares.md) | `GET /Shares` | [docs](https://api.sharefile.com/html/docs/Shares.html) |
| [List Zones](actions/list-zones.md) | `GET /Zones` | [docs](https://api.sharefile.com/html/docs/Zones.html) |
| [Send Share](actions/send-share.md) | `POST /Shares/Send` | [docs](https://api.sharefile.com/html/docs/Shares.html) |
| [Update Group](actions/update-group.md) | `PATCH /Groups({{id}})` | [docs](https://api.sharefile.com/html/docs/Groups.html) |
| [Update User](actions/update-user.md) | `PATCH /Users({{id}})` | [docs](https://api.sharefile.com/html/docs/Users.html) |
