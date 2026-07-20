# inFlow Inventory: Native API Reference

A consolidated summary of inFlow Inventory's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://cloudapi.inflowinventory.com/docs/index.html
- **OpenAPI specification:** https://cloudapi.inflowinventory.com/docs/api/swagger.json
- **API base URL:** `https://cloudapi.inflowinventory.com/{companyId}`

## Authentication

### API Key

Use your inFlow Inventory API key and company ID.

### Credentials

- **API Key:** `apiKey` · required
- **Company ID:** `companyId` · required · Your inFlow account companyId from the integrations page.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.inflowinventory.com/support/cloud/inflows-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json;version=2026-02-24` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `count` in the query string to set the page size (default 20; accepted range 1–100). Use `skip` in the query string as the record offset.

## Sorting

Set the sort field with `sort` in the query string. Set the direction separately with `sortDesc`. Use `false` for ascending order and `true` for descending order. Only one sort field is accepted.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Customer](actions/get-customer.md) | `GET /customers/:customerId` | [docs](https://cloudapi.inflowinventory.com/docs/index.html) |
| [Get Location](actions/get-location.md) | `GET /locations/:locationId` | [docs](https://cloudapi.inflowinventory.com/docs/index.html) |
| [Get Product](actions/get-product.md) | `GET /products/:productId` | [docs](https://cloudapi.inflowinventory.com/docs/index.html) |
| [Get Product Inventory Summary](actions/get-product-inventory-summary.md) | `GET /products/:productId/summary` | [docs](https://cloudapi.inflowinventory.com/docs/index.html) |
| [Get Purchase Order](actions/get-purchase-order.md) | `GET /purchase-orders/:purchaseOrderId` | [docs](https://cloudapi.inflowinventory.com/docs/index.html) |
| [Get Sales Order](actions/get-sales-order.md) | `GET /sales-orders/:salesOrderId` | [docs](https://cloudapi.inflowinventory.com/docs/index.html) |
| [Get Stock Adjustment](actions/get-stock-adjustment.md) | `GET /stock-adjustments/:stockAdjustmentId` | [docs](https://cloudapi.inflowinventory.com/docs/index.html) |
| [Get Stock Transfer](actions/get-stock-transfer.md) | `GET /stock-transfers/:stockTransferId` | [docs](https://cloudapi.inflowinventory.com/docs/index.html) |
| [Get Vendor](actions/get-vendor.md) | `GET /vendors/:vendorId` | [docs](https://cloudapi.inflowinventory.com/docs/index.html) |
| [Insert or Update Customer](actions/insert-or-update-customer.md) | `PUT /customers` | [docs](https://cloudapi.inflowinventory.com/docs/index.html) |
| [Insert or Update Product](actions/insert-or-update-product.md) | `PUT /products` | [docs](https://cloudapi.inflowinventory.com/docs/index.html) |
| [Insert or Update Purchase Order](actions/insert-or-update-purchase-order.md) | `PUT /purchase-orders` | [docs](https://cloudapi.inflowinventory.com/docs/index.html) |
| [Insert or Update Sales Order](actions/insert-or-update-sales-order.md) | `PUT /sales-orders` | [docs](https://cloudapi.inflowinventory.com/docs/index.html) |
| [Insert or Update Stock Transfer](actions/insert-or-update-stock-transfer.md) | `PUT /stock-transfers` | [docs](https://cloudapi.inflowinventory.com/docs/index.html) |
| [Insert or Update Vendor](actions/insert-or-update-vendor.md) | `PUT /vendors` | [docs](https://cloudapi.inflowinventory.com/docs/index.html) |
| [List Customers](actions/list-customers.md) | `GET /customers` | [docs](https://cloudapi.inflowinventory.com/docs/index.html) |
| [List Locations](actions/list-locations.md) | `GET /locations` | [docs](https://cloudapi.inflowinventory.com/docs/index.html) |
| [List Multiple Product Inventory Summaries](actions/list-multiple-product-inventory-summaries.md) | `POST /products/summary` | [docs](https://cloudapi.inflowinventory.com/docs/index.html) |
| [List Products](actions/list-products.md) | `GET /products` | [docs](https://cloudapi.inflowinventory.com/docs/index.html) |
| [List Purchase Orders](actions/list-purchase-orders.md) | `GET /purchase-orders` | [docs](https://cloudapi.inflowinventory.com/docs/index.html) |
| [List Sales Orders](actions/list-sales-orders.md) | `GET /sales-orders` | [docs](https://cloudapi.inflowinventory.com/docs/index.html) |
| [List Stock Adjustments](actions/list-stock-adjustments.md) | `GET /stock-adjustments` | [docs](https://cloudapi.inflowinventory.com/docs/index.html) |
| [List Stock Transfers](actions/list-stock-transfers.md) | `GET /stock-transfers` | [docs](https://cloudapi.inflowinventory.com/docs/index.html) |
| [List Vendors](actions/list-vendors.md) | `GET /vendors` | [docs](https://cloudapi.inflowinventory.com/docs/index.html) |
