# Commerce Layer: Native API Reference

A consolidated summary of Commerce Layer's API configuration and 59 documented operations, with links to official documentation.

- **Official docs:** https://docs.commercelayer.io/core-api-reference
- **API base URL:** `{coreApiEndpoint}`

## Authentication

### OAuth2 (Client Credentials)

Use Commerce Layer Integration credentials with the Core API endpoint from the same environment.

### Credentials

- **Client ID:** `clientId` · required · Commerce Layer Integration credential client ID.
- **Client Secret:** `clientSecret` · required · Commerce Layer Integration credential client secret.
- **Core API Endpoint:** `coreApiEndpoint` · required · Your Commerce Layer organization Core API endpoint, for example https://yourdomain.commercelayer.io.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://auth.commercelayer.io/oauth/token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `market:all`.

A machine-to-machine flow is configured.

[Official authentication documentation](https://docs.commercelayer.io/core/authentication/client-credentials)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.api+json` |
| `Content-Type` | `application/vnd.api+json` |

Responses from this API use JSON.

## Pagination

Use `page[size]` in the query string to set the page size (default 10; accepted range 1–25). Use `page[number]` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string. Supported operators: `contains`, `ends`, `eq`, `gt`, `gte`, `in`, `lt`, `lte`, `ne`, `nin`, `starts`.

## Sorting

Set the sort field with `sort` in the query string. Prefix the field name to select its direction. Multiple sort fields can be combined.

## Endpoints (59 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Address](actions/create-address.md) | `POST /api/addresses` | [docs](https://docs.commercelayer.io/core-api-reference/addresses/create) |
| [Create Avalara Account](actions/create-avalara-account.md) | `POST /api/avalara_accounts` | [docs](https://docs.commercelayer.io/core-api-reference/avalara_accounts/create) |
| [Create Customer Group](actions/create-customer-group.md) | `POST /api/customer_groups` | [docs](https://docs.commercelayer.io/core-api-reference/customer_groups/create) |
| [Create Inventory Model](actions/create-inventory-model.md) | `POST /api/inventory_models` | [docs](https://docs.commercelayer.io/core-api-reference/inventory_models/create) |
| [Create Manual Tax Calculator](actions/create-manual-tax-calculator.md) | `POST /api/manual_tax_calculators` | [docs](https://docs.commercelayer.io/core-api-reference/manual_tax_calculators/create) |
| [Create Market](actions/create-market.md) | `POST /api/markets` | [docs](https://docs.commercelayer.io/core-api-reference/markets/create) |
| [Create Merchant](actions/create-merchant.md) | `POST /api/merchants` | [docs](https://docs.commercelayer.io/core-api-reference/merchants/create) |
| [Create Price List](actions/create-price-list.md) | `POST /api/price_lists` | [docs](https://docs.commercelayer.io/core-api-reference/price_lists/create) |
| [Create Shipping Category](actions/create-shipping-category.md) | `POST /api/shipping_categories` | [docs](https://docs.commercelayer.io/core-api-reference/shipping_categories/create) |
| [Create SKU](actions/create-sku.md) | `POST /api/skus` | [docs](https://docs.commercelayer.io/core-api-reference/skus/create) |
| [Create Stock Location](actions/create-stock-location.md) | `POST /api/stock_locations` | [docs](https://docs.commercelayer.io/core-api-reference/stock_locations/create) |
| [Create Tax Category](actions/create-tax-category.md) | `POST /api/tax_categories` | [docs](https://docs.commercelayer.io/core-api-reference/tax_categories/create) |
| [Create Tax Rule](actions/create-tax-rule.md) | `POST /api/tax_rules` | [docs](https://docs.commercelayer.io/core-api-reference/tax_rules/create) |
| [Delete Address](actions/delete-address.md) | `DELETE /api/addresses/:id` | [docs](https://docs.commercelayer.io/core-api-reference/addresses/delete) |
| [Delete Customer Group](actions/delete-customer-group.md) | `DELETE /api/customer_groups/:id` | [docs](https://docs.commercelayer.io/core-api-reference/customer_groups/delete) |
| [Delete Inventory Model](actions/delete-inventory-model.md) | `DELETE /api/inventory_models/:id` | [docs](https://docs.commercelayer.io/core-api-reference/inventory_models/delete) |
| [Delete Manual Tax Calculator](actions/delete-manual-tax-calculator.md) | `DELETE /api/manual_tax_calculators/:id` | [docs](https://docs.commercelayer.io/core-api-reference/manual_tax_calculators/delete) |
| [Delete Market](actions/delete-market.md) | `DELETE /api/markets/:id` | [docs](https://docs.commercelayer.io/core-api-reference/markets/delete) |
| [Delete Merchant](actions/delete-merchant.md) | `DELETE /api/merchants/:id` | [docs](https://docs.commercelayer.io/core-api-reference/merchants/delete) |
| [Delete Price List](actions/delete-price-list.md) | `DELETE /api/price_lists/:id` | [docs](https://docs.commercelayer.io/core-api-reference/price_lists/delete) |
| [Delete Shipping Category](actions/delete-shipping-category.md) | `DELETE /api/shipping_categories/:id` | [docs](https://docs.commercelayer.io/core-api-reference/shipping_categories/delete) |
| [Delete Stock Location](actions/delete-stock-location.md) | `DELETE /api/stock_locations/:id` | [docs](https://docs.commercelayer.io/core-api-reference/stock_locations/delete) |
| [Delete Tax Category](actions/delete-tax-category.md) | `DELETE /api/tax_categories/:id` | [docs](https://docs.commercelayer.io/core-api-reference/tax_categories/delete) |
| [Delete Tax Rule](actions/delete-tax-rule.md) | `DELETE /api/tax_rules/:id` | [docs](https://docs.commercelayer.io/core-api-reference/tax_rules/delete) |
| [Get Address](actions/get-address.md) | `GET /api/addresses/:id` | [docs](https://docs.commercelayer.io/core-api-reference/addresses/retrieve) |
| [Get Customer Group](actions/get-customer-group.md) | `GET /api/customer_groups/:id` | [docs](https://docs.commercelayer.io/core-api-reference/customer_groups/retrieve) |
| [Get Inventory Model](actions/get-inventory-model.md) | `GET /api/inventory_models/:id` | [docs](https://docs.commercelayer.io/core-api-reference/inventory_models/retrieve) |
| [Get Manual Tax Calculator](actions/get-manual-tax-calculator.md) | `GET /api/manual_tax_calculators/:id` | [docs](https://docs.commercelayer.io/core-api-reference/manual_tax_calculators/retrieve) |
| [Get Market](actions/get-market.md) | `GET /api/markets/:id` | [docs](https://docs.commercelayer.io/core-api-reference/markets/retrieve) |
| [Get Merchant](actions/get-merchant.md) | `GET /api/merchants/:id` | [docs](https://docs.commercelayer.io/core-api-reference/merchants/retrieve) |
| [Get Price List](actions/get-price-list.md) | `GET /api/price_lists/:id` | [docs](https://docs.commercelayer.io/core-api-reference/price_lists/retrieve) |
| [Get Shipping Category](actions/get-shipping-category.md) | `GET /api/shipping_categories/:id` | [docs](https://docs.commercelayer.io/core-api-reference/shipping_categories/retrieve) |
| [Get Stock Location](actions/get-stock-location.md) | `GET /api/stock_locations/:id` | [docs](https://docs.commercelayer.io/core-api-reference/stock_locations/retrieve) |
| [Get Tax Category](actions/get-tax-category.md) | `GET /api/tax_categories/:id` | [docs](https://docs.commercelayer.io/core-api-reference/tax_categories/retrieve) |
| [Get Tax Rule](actions/get-tax-rule.md) | `GET /api/tax_rules/:id` | [docs](https://docs.commercelayer.io/core-api-reference/tax_rules/retrieve) |
| [List Addresses](actions/list-addresses.md) | `GET /api/addresses` | [docs](https://docs.commercelayer.io/core-api-reference/addresses/list) |
| [List Avalara Accounts](actions/list-avalara-accounts.md) | `GET /api/avalara_accounts` | [docs](https://docs.commercelayer.io/core-api-reference/avalara_accounts/list) |
| [List Customer Groups](actions/list-customer-groups.md) | `GET /api/customer_groups` | [docs](https://docs.commercelayer.io/core-api-reference/customer_groups/list) |
| [List Inventory Models](actions/list-inventory-models.md) | `GET /api/inventory_models` | [docs](https://docs.commercelayer.io/core-api-reference/inventory_models/list) |
| [List Manual Tax Calculators](actions/list-manual-tax-calculators.md) | `GET /api/manual_tax_calculators` | [docs](https://docs.commercelayer.io/core-api-reference/manual_tax_calculators/list) |
| [List Markets](actions/list-markets.md) | `GET /api/markets` | [docs](https://docs.commercelayer.io/core-api-reference/markets/list) |
| [List Merchants](actions/list-merchants.md) | `GET /api/merchants` | [docs](https://docs.commercelayer.io/core-api-reference/merchants/list) |
| [List Price Lists](actions/list-price-lists.md) | `GET /api/price_lists` | [docs](https://docs.commercelayer.io/core-api-reference/price_lists/list) |
| [List Shipping Categories](actions/list-shipping-categories.md) | `GET /api/shipping_categories` | [docs](https://docs.commercelayer.io/core-api-reference/shipping_categories/list) |
| [List Stock Locations](actions/list-stock-locations.md) | `GET /api/stock_locations` | [docs](https://docs.commercelayer.io/core-api-reference/stock_locations/list) |
| [List Tax Calculators](actions/list-tax-calculators.md) | `GET /api/tax_calculators` | [docs](https://docs.commercelayer.io/core-api-reference/tax_calculators/list) |
| [List Tax Categories](actions/list-tax-categories.md) | `GET /api/tax_categories` | [docs](https://docs.commercelayer.io/core-api-reference/tax_categories/list) |
| [List Tax Rules](actions/list-tax-rules.md) | `GET /api/tax_rules` | [docs](https://docs.commercelayer.io/core-api-reference/tax_rules/list) |
| [Update Address](actions/update-address.md) | `PATCH /api/addresses/:id` | [docs](https://docs.commercelayer.io/core-api-reference/addresses/update) |
| [Update Customer Group](actions/update-customer-group.md) | `PATCH /api/customer_groups/:id` | [docs](https://docs.commercelayer.io/core-api-reference/customer_groups/update) |
| [Update Inventory Model](actions/update-inventory-model.md) | `PATCH /api/inventory_models/:id` | [docs](https://docs.commercelayer.io/core-api-reference/inventory_models/update) |
| [Update Manual Tax Calculator](actions/update-manual-tax-calculator.md) | `PATCH /api/manual_tax_calculators/:id` | [docs](https://docs.commercelayer.io/core-api-reference/manual_tax_calculators/update) |
| [Update Market](actions/update-market.md) | `PATCH /api/markets/:id` | [docs](https://docs.commercelayer.io/core-api-reference/markets/update) |
| [Update Merchant](actions/update-merchant.md) | `PATCH /api/merchants/:id` | [docs](https://docs.commercelayer.io/core-api-reference/merchants/update) |
| [Update Price List](actions/update-price-list.md) | `PATCH /api/price_lists/:id` | [docs](https://docs.commercelayer.io/core-api-reference/price_lists/update) |
| [Update Shipping Category](actions/update-shipping-category.md) | `PATCH /api/shipping_categories/:id` | [docs](https://docs.commercelayer.io/core-api-reference/shipping_categories/update) |
| [Update Stock Location](actions/update-stock-location.md) | `PATCH /api/stock_locations/:id` | [docs](https://docs.commercelayer.io/core-api-reference/stock_locations/update) |
| [Update Tax Category](actions/update-tax-category.md) | `PATCH /api/tax_categories/:id` | [docs](https://docs.commercelayer.io/core-api-reference/tax_categories/update) |
| [Update Tax Rule](actions/update-tax-rule.md) | `PATCH /api/tax_rules/:id` | [docs](https://docs.commercelayer.io/core-api-reference/tax_rules/update) |
