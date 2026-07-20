# Tiliter: Native API Reference

A consolidated summary of Tiliter's API configuration and 32 documented operations, with links to official documentation.

- **Official docs:** https://developer.tiliter.com/reference/index
- **OpenAPI specification:** https://developer.tiliter.com/openapi.json
- **API base URL:** `https://recognition.services.tiliter.com/v1/15`

## Authentication

### API Key

Tiliter tenant API key sent in the shared tiliter-api-key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
tiliter-api-key: <apiKey>
```

[Official authentication documentation](https://developer.tiliter.com/docs/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (32 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Device](actions/create-device.md) | `POST /devices/:device_id` | [docs](https://developer.tiliter.com/reference/create_device) |
| [Create Or Update Products Batch](actions/create-or-update-products-batch.md) | `POST /products/batch` | [docs](https://developer.tiliter.com/reference/create_or_update_products_batch) |
| [Create Product](actions/create-product.md) | `POST /products/:product_id` | [docs](https://developer.tiliter.com/reference/create_product) |
| [Create Product Mapping](actions/create-product-mapping.md) | `POST /product_mappings/` | [docs](https://developer.tiliter.com/reference/create_product_mapping) |
| [Create Product Sample](actions/create-product-sample.md) | `POST /products/:product_id/samples` | [docs](https://developer.tiliter.com/reference/create_product_sample) |
| [Create Recognition Request](actions/create-recognition-request.md) | `POST /recognition/` | [docs](https://developer.tiliter.com/docs/overview-of-the-operational-endpoints) |
| [Create Selection Report](actions/create-selection-report.md) | `POST /recognition/:recognition_id/selection_report` | [docs](https://developer.tiliter.com/reference/create_selection_report) |
| [Create Store](actions/create-store.md) | `POST /stores/:store_id` | [docs](https://developer.tiliter.com/reference/create_store) |
| [Create Transaction Event](actions/create-transaction-event.md) | `POST /recognition/:recognition_id/transaction_events` | [docs](https://developer.tiliter.com/reference/create_transaction_event) |
| [Create Transaction Events Batch](actions/create-transaction-events-batch.md) | `POST /recognition/transaction_events/batch` | [docs](https://developer.tiliter.com/reference/create_transaction_events_in_batch) |
| [Delete Device](actions/delete-device.md) | `DELETE /devices/:device_id` | [docs](https://developer.tiliter.com/reference/delete_device) |
| [Delete Product](actions/delete-product.md) | `DELETE /products/:product_id` | [docs](https://developer.tiliter.com/reference/delete_product) |
| [Delete Product Mapping](actions/delete-product-mapping.md) | `DELETE /product_mappings/:product_id` | [docs](https://developer.tiliter.com/reference/delete_product_mapping) |
| [Delete Product Sample](actions/delete-product-sample.md) | `DELETE /products/:product_id/samples/:sample_id` | [docs](https://developer.tiliter.com/reference/delete_product_sample) |
| [Delete Store](actions/delete-store.md) | `DELETE /stores/:store_id` | [docs](https://developer.tiliter.com/reference/delete_store) |
| [Get Device](actions/get-device.md) | `GET /devices/:device_id` | [docs](https://developer.tiliter.com/reference/get_device) |
| [Get Product](actions/get-product.md) | `GET /products/:product_id` | [docs](https://developer.tiliter.com/reference/get_product) |
| [Get Product Mapping](actions/get-product-mapping.md) | `GET /product_mappings/:product_id` | [docs](https://developer.tiliter.com/reference/get_product_mapping) |
| [Get Product Sample](actions/get-product-sample.md) | `GET /products/:product_id/samples/:sample_id` | [docs](https://developer.tiliter.com/reference/get_product_sample) |
| [Get Store](actions/get-store.md) | `GET /stores/:store_id` | [docs](https://developer.tiliter.com/reference/get_store) |
| [Get Store Stock](actions/get-store-stock.md) | `GET /stores/:store_id/stock` | [docs](https://developer.tiliter.com/reference/get_store_stock) |
| [Health Check](actions/health-check.md) | `GET /` | [docs](https://developer.tiliter.com/reference/index) |
| [List Archetypes](actions/list-archetypes.md) | `GET /archetypes/` | [docs](https://developer.tiliter.com/reference/list_archetypes) |
| [List Devices](actions/list-devices.md) | `GET /devices/` | [docs](https://developer.tiliter.com/reference/list_devices) |
| [List Product Mappings](actions/list-product-mappings.md) | `GET /product_mappings/` | [docs](https://developer.tiliter.com/reference/list_product_mappings) |
| [List Products](actions/list-products.md) | `GET /products/` | [docs](https://developer.tiliter.com/reference/list_products) |
| [List Stores](actions/list-stores.md) | `GET /stores/` | [docs](https://developer.tiliter.com/reference/list_stores) |
| [Update Device](actions/update-device.md) | `PUT /devices/:device_id` | [docs](https://developer.tiliter.com/reference/update_device) |
| [Update Product](actions/update-product.md) | `PUT /products/:product_id` | [docs](https://developer.tiliter.com/reference/update_product) |
| [Update Product Mapping](actions/update-product-mapping.md) | `PUT /product_mappings/` | [docs](https://developer.tiliter.com/reference/update_product_mapping) |
| [Update Store](actions/update-store.md) | `PUT /stores/:store_id` | [docs](https://developer.tiliter.com/reference/update_store) |
| [Update Store Stock](actions/update-store-stock.md) | `PUT /stores/:store_id/stock` | [docs](https://developer.tiliter.com/reference/update_store_stock) |
