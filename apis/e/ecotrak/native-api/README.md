# Ecotrak: Native API Reference

A consolidated summary of Ecotrak's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://api-docs.ecotrak.com
- **API base URL:** `https://api.ecotrak.com`

## Authentication

### OAuth2 Client Credentials

Connect Ecotrak with your own OAuth2 client credentials. This flow exchanges client ID and client secret directly for a token, so no browser authorization modal is expected.

### Credentials

- **Client ID:** `clientId` · required · Ecotrak OAuth2 client ID for this connection.
- **Client Secret:** `clientSecret` · required · Ecotrak OAuth2 client secret for this connection.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://auth.ecotrak.com/oauth2/token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


A machine-to-machine flow is configured.

[Official authentication documentation](https://api-docs.ecotrak.com)

## Pagination

Use `take` in the query string to set the page size (default 100). Use `page` in the query string to choose the page; numbering starts at 0.

## Filtering

Send filters in the query string.

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create User](actions/create-user.md) | `POST /v2/user` | [docs](https://documenter.getpostman.com/view/19394488/2sAYk8u3FF#customer-user-create-user) |
| [Get User](actions/get-user.md) | `GET /v2/user/:user_id` | [docs](https://documenter.getpostman.com/view/19394488/2sAYk8u3FF#customer-user-view-user-details) |
| [List Users](actions/list-users.md) | `GET /v2/user` | [docs](https://api-docs.ecotrak.com/#d030c2de-800e-438b-b1a5-8d651045c202) |
| [List Work Orders](actions/list-work-orders.md) | `GET /v1/workorders` | [docs](https://documenter.getpostman.com/view/19394488/2sAYk8u3FF#customer-work-order-work-orders) |
| [Search Invoices](actions/search-invoices.md) | `GET /v1/invoices/search` | [docs](https://documenter.getpostman.com/view/19394488/2sAYk8u3FF#customer-invoices-search-invoices) |
| [Search Work Orders](actions/search-work-orders.md) | `GET /v1/workorders/search` | [docs](https://documenter.getpostman.com/view/19394488/2sAYk8u3FF#customer-work-order-search-work-order) |
| [Update User](actions/update-user.md) | `PUT /v2/user/:user_id` | [docs](https://documenter.getpostman.com/view/19394488/2sAYk8u3FF#customer-user-edit-user) |
| [Update User Assigned Locations](actions/update-user-assigned-locations.md) | `PUT /v2/user/:user_id/location` | [docs](https://documenter.getpostman.com/view/19394488/2sAYk8u3FF#customer-user-edit-user-s-assigned-locations) |
