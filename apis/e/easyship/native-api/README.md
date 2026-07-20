# Easyship: Native API Reference

A consolidated summary of Easyship's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://developers.easyship.com/reference
- **API base URL:** `https://public-api.easyship.com/2024-09`

## Authentication

### API Token

Use an Easyship bearer token for the Easyship Public API.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.easyship.com/reference/authentication)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 1 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Pickup](actions/cancel-pickup.md) | `POST /pickups/:pickup_id/cancel` | [docs](https://developers.easyship.com/reference/pickups_cancel) |
| [Cancel Shipment](actions/cancel-shipment.md) | `POST /shipments/:shipment_id/cancel` | [docs](https://developers.easyship.com/reference/shipments_cancel) |
| [Create Address](actions/create-address.md) | `POST /addresses` | [docs](https://developers.easyship.com/reference/addresses_create) |
| [Create Batch of Labels](actions/create-batch-of-labels.md) | `POST /batches/labels` | [docs](https://developers.easyship.com/reference/batch_labels_create) |
| [Create Pickup](actions/create-pickup.md) | `POST /pickups` | [docs](https://developers.easyship.com/reference/pickups_create) |
| [Create Product](actions/create-product.md) | `POST /products` | [docs](https://developers.easyship.com/reference/products_create) |
| [Create Shipment](actions/create-shipment.md) | `POST /shipments` | [docs](https://developers.easyship.com/reference/shipments_create) |
| [Create Shipping Rule](actions/create-shipping-rule.md) | `POST /shipping_rules` | [docs](https://developers.easyship.com/reference/shipping_rules_create) |
| [Get Account Information](actions/get-account-information.md) | `GET /account` | [docs](https://developers.easyship.com/reference/account_show) |
| [Get Shipment](actions/get-shipment.md) | `GET /shipments/:shipment_id` | [docs](https://developers.easyship.com/reference/shipments_show) |
| [Get Shipping Rule](actions/get-shipping-rule.md) | `GET /shipping_rules/:shipping_rule_id` | [docs](https://developers.easyship.com/reference/shipping_rules_show) |
| [List Addresses](actions/list-addresses.md) | `GET /addresses` | [docs](https://developers.easyship.com/reference/addresses_index) |
| [List Courier Services](actions/list-courier-services.md) | `GET /courier_services` | [docs](https://developers.easyship.com/reference/courier_services_index) |
| [List Couriers](actions/list-couriers.md) | `GET /couriers` | [docs](https://developers.easyship.com/reference/couriers_index) |
| [List Pickups](actions/list-pickups.md) | `GET /pickups` | [docs](https://developers.easyship.com/reference/pickups_index) |
| [List Products](actions/list-products.md) | `GET /products` | [docs](https://developers.easyship.com/reference/products_index) |
| [List Shipment Trackings](actions/list-shipment-trackings.md) | `GET /shipments/trackings` | [docs](https://developers.easyship.com/reference/shipments_trackings_index) |
| [List Shipments](actions/list-shipments.md) | `GET /shipments` | [docs](https://developers.easyship.com/reference/shipments_index) |
| [List Shipping Rules](actions/list-shipping-rules.md) | `GET /shipping_rules` | [docs](https://developers.easyship.com/reference/shipping_rules_index) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks` | [docs](https://developers.easyship.com/reference/webhooks_index) |
| [Request Rates](actions/request-rates.md) | `POST /rates` | [docs](https://developers.easyship.com/reference/rates_request) |
| [Update Address](actions/update-address.md) | `PATCH /addresses/:address_id` | [docs](https://developers.easyship.com/reference/addresses_update) |
| [Update Product](actions/update-product.md) | `PATCH /products/:product_id` | [docs](https://developers.easyship.com/reference/products_update) |
| [Update Shipment](actions/update-shipment.md) | `PATCH /shipments/:shipment_id` | [docs](https://developers.easyship.com/reference/shipments_update) |
