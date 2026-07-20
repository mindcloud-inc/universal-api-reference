# Apaleo Official: Native API Reference

A consolidated summary of Apaleo Official's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://api.apaleo.com/swagger/index.html
- **API base URL:** `https://api.apaleo.com`

## Authentication

### OAuth2

Connect apaleo with the OAuth 2.0 authorization code flow.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://identity.apaleo.com/connect/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://identity.apaleo.com/connect/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `offline_access account.manage account.suspend accounting.read authorizations.manage authorizations.read availability.manage availability.read charges.delete companies.manage companies.read depositItems.manage deposits.manage deposits.read distribution:reservations.manage distribution:subscriptions.manage fiscalization:configuration.read fiscalization:invoices.read fiscalization:receipts.read fiscalization:reports.read folios.manage folios.manage-negative-payments folios.payment-with-charges folios.read identity:account-users.manage identity:account-users.read identity:roles.manage identity:roles.read integration:ui-integrations.manage invoices.manage invoices.read logs.read maintenances.manage maintenances.read mcp:prompts mcp:resources mcp:tools offer-index.read offers.read openid operations.change-room-state operations.trigger-night-audit payment-accounts.manage payment-accounts.read payment:configuration.read payment:invoices.read payment:payment-logs.read payment:reports.read payment:transactions.manage payment:transactions.read payments.manage payments.read prepayment-notices.read profile profile:manage profile:read rateplans.read-corporate rateplans.read-negotiated rates.manage rates.read reports.read reservations.force-manage reservations.manage reservations.read routings.create routings.manage routings.read servicegroups.create servicegroups.manage servicegroups.read setup.manage setup.read sfa:admin`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://identity.apaleo.com/connect/token.

[Official authentication documentation](https://apaleo.dev/guides/oauth-connection/auth-code-grant.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `pageSize` in the query string to set the page size (default 500; accepted range 1–500). Use `pageNumber` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort` in the query string. Use `asc` for ascending order and `desc` for descending order. Multiple sort fields can be combined.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Properties](actions/list-properties.md) | `GET /inventory/v1/properties` | [docs](https://api.apaleo.com/swagger/index.html?urls.primaryName=Inventory%20V1#/Property/InventoryPropertiesGet) |
