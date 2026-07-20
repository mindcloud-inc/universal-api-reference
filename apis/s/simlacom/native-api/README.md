# Simla.com: Native API Reference

A consolidated summary of Simla.com's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://docs.simla.com/Developers/API/APIVersions/APIv5
- **API base URL:** `https://apps2.simla.com`

## Authentication

### API Key

Use a Simla API key to authenticate requests to the current workspace.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-KEY: <apiKey>
```

[Official authentication documentation](https://docs.simla.com/Developers/API/APIFeatures/APIRules)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Current API Credentials](actions/get-current-api-credentials.md) | `GET /api/credentials` | [docs](https://docs.simla.com/api/en/RetailCRM/apiMethods/v5#get--api-credentials) |
| [List Cost Groups](actions/list-cost-groups.md) | `GET /api/v5/reference/cost-groups` | [docs](https://docs.simla.com/api/en/RetailCRM/apiMethods/v5#get--api-v5-reference-cost-groups) |
| [List Cost Items](actions/list-cost-items.md) | `GET /api/v5/reference/cost-items` | [docs](https://docs.simla.com/api/en/RetailCRM/apiMethods/v5#get--api-v5-reference-cost-items) |
| [List Countries](actions/list-countries.md) | `GET /api/v5/reference/countries` | [docs](https://docs.simla.com/api/en/RetailCRM/apiMethods/v5#get--api-v5-reference-countries) |
| [List Couriers](actions/list-couriers.md) | `GET /api/v5/reference/couriers` | [docs](https://docs.simla.com/api/en/RetailCRM/apiMethods/v5#get--api-v5-reference-couriers) |
| [List Currencies](actions/list-currencies.md) | `GET /api/v5/reference/currencies` | [docs](https://docs.simla.com/api/en/RetailCRM/apiMethods/v5#get--api-v5-reference-currencies) |
| [List Delivery Services](actions/list-delivery-services.md) | `GET /api/v5/reference/delivery-services` | [docs](https://docs.simla.com/api/en/RetailCRM/apiMethods/v5#get--api-v5-reference-delivery-services) |
| [List Delivery Types](actions/list-delivery-types.md) | `GET /api/v5/reference/delivery-types` | [docs](https://docs.simla.com/api/en/RetailCRM/apiMethods/v5#get--api-v5-reference-delivery-types) |
| [List Legal Entities](actions/list-legal-entities.md) | `GET /api/v5/reference/legal-entities` | [docs](https://docs.simla.com/api/en/RetailCRM/apiMethods/v5#get--api-v5-reference-legal-entities) |
| [List Order Methods](actions/list-order-methods.md) | `GET /api/v5/reference/order-methods` | [docs](https://docs.simla.com/api/en/RetailCRM/apiMethods/v5#get--api-v5-reference-order-methods) |
| [List Order Types](actions/list-order-types.md) | `GET /api/v5/reference/order-types` | [docs](https://docs.simla.com/api/en/RetailCRM/apiMethods/v5#get--api-v5-reference-order-types) |
| [List Payment Statuses](actions/list-payment-statuses.md) | `GET /api/v5/reference/payment-statuses` | [docs](https://docs.simla.com/api/en/RetailCRM/apiMethods/v5#get--api-v5-reference-payment-statuses) |
| [List Payment Types](actions/list-payment-types.md) | `GET /api/v5/reference/payment-types` | [docs](https://docs.simla.com/api/en/RetailCRM/apiMethods/v5#get--api-v5-reference-payment-types) |
| [List Price Types](actions/list-price-types.md) | `GET /api/v5/reference/price-types` | [docs](https://docs.simla.com/api/en/RetailCRM/apiMethods/v5#get--api-v5-reference-price-types) |
| [List Product Statuses](actions/list-product-statuses.md) | `GET /api/v5/reference/product-statuses` | [docs](https://docs.simla.com/api/en/RetailCRM/apiMethods/v5#get--api-v5-reference-product-statuses) |
| [List Sites](actions/list-sites.md) | `GET /api/v5/reference/sites` | [docs](https://docs.simla.com/api/en/RetailCRM/apiMethods/v5#get--api-v5-reference-sites) |
| [List Status Groups](actions/list-status-groups.md) | `GET /api/v5/reference/status-groups` | [docs](https://docs.simla.com/api/en/RetailCRM/apiMethods/v5#get--api-v5-reference-status-groups) |
| [List Statuses](actions/list-statuses.md) | `GET /api/v5/reference/statuses` | [docs](https://docs.simla.com/api/en/RetailCRM/apiMethods/v5#get--api-v5-reference-statuses) |
| [List Stores](actions/list-stores.md) | `GET /api/v5/reference/stores` | [docs](https://docs.simla.com/api/en/RetailCRM/apiMethods/v5#get--api-v5-reference-stores) |
| [List Units](actions/list-units.md) | `GET /api/v5/reference/units` | [docs](https://docs.simla.com/api/en/RetailCRM/apiMethods/v5#get--api-v5-reference-units) |
