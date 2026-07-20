# bitFit Asset Management Software: Native API Reference

A consolidated summary of bitFit Asset Management Software's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://assets.bitfit.com/setup/api/docs
- **API base URL:** `https://api-assets.bitfit.com`

## Authentication

### OAuth2 Password Grant

Use a BitFit user login plus BitFit account client credentials to obtain a bearer token from the BitFit OAuth2 token endpoint.

### Credentials

- **Username:** `username` · required · BitFit user email or username used for password-grant authentication.
- **Password:** `password` · required · BitFit password used for password-grant authentication.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://api-assets.bitfit.com/oauth2/token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://api-assets.bitfit.com/oauth2/token.

[Official authentication documentation](https://assets.bitfit.com/setup/api/docs)

## Pagination

Use `limit` in the query string to set the page size (default 50; accepted range 1–100). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Asset](actions/get-asset.md) | `GET /v2/assets/:id` | [docs](https://assets.bitfit.com/setup/api/docs) |
| [Get Attachment](actions/get-attachment.md) | `GET /v2/attachments/:id` | [docs](https://assets.bitfit.com/setup/api/docs) |
| [Get Company](actions/get-company.md) | `GET /v2/companies/:id` | [docs](https://assets.bitfit.com/setup/api/docs) |
| [Get Config](actions/get-config.md) | `GET /v2/configs/:id` | [docs](https://assets.bitfit.com/setup/api/docs) |
| [Get Consumable](actions/get-consumable.md) | `GET /v2/consumables/:id` | [docs](https://assets.bitfit.com/setup/api/docs) |
| [Get Group](actions/get-group.md) | `GET /v2/groups/:id` | [docs](https://assets.bitfit.com/setup/api/docs) |
| [Get Inventory Rule](actions/get-inventory-rule.md) | `GET /v2/inventory_rules/:id` | [docs](https://assets.bitfit.com/setup/api/docs) |
| [Get List](actions/get-list.md) | `GET /v2/lists/:id` | [docs](https://assets.bitfit.com/setup/api/docs) |
| [Get Location](actions/get-location.md) | `GET /v2/locations/:id` | [docs](https://assets.bitfit.com/setup/api/docs) |
| [Get Page](actions/get-page.md) | `GET /v2/pages/:id` | [docs](https://assets.bitfit.com/setup/api/docs) |
| [Get Request](actions/get-request.md) | `GET /v2/requests/:id` | [docs](https://assets.bitfit.com/setup/api/docs) |
| [Get Role](actions/get-role.md) | `GET /v2/roles/:id` | [docs](https://assets.bitfit.com/setup/api/docs) |
| [Get User](actions/get-user.md) | `GET /v2/users/:id` | [docs](https://assets.bitfit.com/setup/api/docs) |
| [Get Widget](actions/get-widget.md) | `GET /v2/widgets/:id` | [docs](https://assets.bitfit.com/setup/api/docs) |
| [Get Widget Config](actions/get-widget-config.md) | `GET /v2/widget_configs/:id` | [docs](https://assets.bitfit.com/setup/api/docs) |
| [List Assets](actions/list-assets.md) | `GET /v2/assets` | [docs](https://assets.bitfit.com/setup/api/docs) |
| [List Attachments](actions/list-attachments.md) | `GET /v2/attachments` | [docs](https://assets.bitfit.com/setup/api/docs) |
| [List Companies](actions/list-companies.md) | `GET /v2/companies` | [docs](https://assets.bitfit.com/setup/api/docs) |
| [List Configs](actions/list-configs.md) | `GET /v2/configs` | [docs](https://assets.bitfit.com/setup/api/docs) |
| [List Consumables](actions/list-consumables.md) | `GET /v2/consumables` | [docs](https://assets.bitfit.com/setup/api/docs) |
| [List Groups](actions/list-groups.md) | `GET /v2/groups` | [docs](https://assets.bitfit.com/setup/api/docs) |
| [List Inventory Rules](actions/list-inventory-rules.md) | `GET /v2/inventory_rules` | [docs](https://assets.bitfit.com/setup/api/docs) |
| [List Lists](actions/list-lists.md) | `GET /v2/lists` | [docs](https://assets.bitfit.com/setup/api/docs) |
| [List Locations](actions/list-locations.md) | `GET /v2/locations` | [docs](https://assets.bitfit.com/setup/api/docs) |
| [List Pages](actions/list-pages.md) | `GET /v2/pages` | [docs](https://assets.bitfit.com/setup/api/docs) |
| [List Requests](actions/list-requests.md) | `GET /v2/requests` | [docs](https://assets.bitfit.com/setup/api/docs) |
| [List Roles](actions/list-roles.md) | `GET /v2/roles` | [docs](https://assets.bitfit.com/setup/api/docs) |
| [List Users](actions/list-users.md) | `GET /v2/users` | [docs](https://assets.bitfit.com/setup/api/docs) |
| [List Widget Configs](actions/list-widget-configs.md) | `GET /v2/widget_configs` | [docs](https://assets.bitfit.com/setup/api/docs) |
| [List Widgets](actions/list-widgets.md) | `GET /v2/widgets` | [docs](https://assets.bitfit.com/setup/api/docs) |
