# Polycom: Native API Reference

A consolidated summary of Polycom's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://api.lens.poly.com/docs/graphql/getting-started
- **API base URL:** `https://api.silica-prod01.io.lens.poly.com`

## Authentication

### OAuth2

OAuth 2.0 client credentials flow for Poly Lens API connections.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://login.lens.poly.com/oauth/token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


A machine-to-machine flow is configured.

[Official authentication documentation](https://api.lens.poly.com/docs/graphql/getting-started)

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Count Tenant Admins](actions/count-tenant-admins.md) | `POST /graphql` | [docs](https://api.lens.poly.com/docs/graphql/Example%20Queries/platform-management-queries) |
| [List Tenant Admins](actions/list-tenant-admins.md) | `POST /graphql` | [docs](https://api.lens.poly.com/docs/graphql/Example%20Queries/platform-management-queries) |
| [List Tenant Members By Role](actions/list-tenant-members-by-role.md) | `POST /graphql` | [docs](https://api.lens.poly.com/docs/graphql/Example%20Queries/platform-management-queries) |
| [List Tenants](actions/list-tenants.md) | `POST /graphql` | [docs](https://api.lens.poly.com/docs/graphql/Example%20Queries/platform-management-queries) |
| [Search Devices](actions/search-devices.md) | `POST /graphql` | [docs](https://api.lens.poly.com/docs/graphql/Example%20Queries/inventory-reporting) |
| [Search Studio X Teams and Zoom Devices](actions/search-studio-x-teams-and-zoom-devices.md) | `POST /graphql` | [docs](https://api.lens.poly.com/docs/graphql/Example%20Queries/inventory-reporting) |
| [Search Teams and Zoom Devices](actions/search-teams-and-zoom-devices.md) | `POST /graphql` | [docs](https://api.lens.poly.com/docs/graphql/Example%20Queries/inventory-reporting) |
| [Search Zoom Devices](actions/search-zoom-devices.md) | `POST /graphql` | [docs](https://api.lens.poly.com/docs/graphql/Example%20Queries/inventory-reporting) |
