# Logiwa Legacy WMS: Native API Reference

A consolidated summary of Logiwa Legacy WMS's API configuration and 16 documented operations, with links to official documentation.

- **Official docs:** https://developer.logiwa.com/?id=5df0da39e6466c2eec992f3f
- **API base URL:** `https://{uRL}.logiwa.com/`

## Authentication

### Custom

### Credentials

- **Site Name:** `uRL` · required
- **username:** `username` · optional
- **password:** `password` · optional

Send these headers with each API request:

```http
Authorization: Bearer <custom.accessToken>
```

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Pagination

Use `PageSize` in the request body to set the page size (default 50; accepted range 1–200). Use `SelectedPageIndex` in the request body to choose the page; numbering starts at 1.

## Endpoints (16 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get a Product ID](actions/get-a-product-id.md) | `POST /en/api/IntegrationApi/InventoryItemGetID` | [docs](https://developer.logiwa.com/?id=5df0dab3e6466c2eec992f45#!#requestContent) |
| [List Pack Types (SEARCH)](actions/get-pack-type-info.md) | `POST /en/api/IntegrationApi/InventoryItemPackTypeSearch` | [docs](https://developer.logiwa.com/?id=5e71514fe6466c0c70d9c50a) |
| [Get Receipt Report](actions/get-receipt-report.md) | `POST en/api/IntegrationApi/ReceiptAllSearch` | [docs](https://developer.logiwa.com/?id=5f7c281ce6466c3884d36b24) |
| [Insert Purchase Order](actions/insert-purchase-order.md) | `POST en/api/IntegrationApi/PurchaseOrderBulkInsert` | [docs](https://developer.logiwa.com/?id=5df0dc03e6466c2eec992f5f) |
| [Insert Receipt Order](actions/insert-receipt-order.md) | `POST en/api/IntegrationApi/WarehouseReceiptBulkInsert` | [docs](https://developer.logiwa.com/?id=5df0dd05e6466c2eec992f69) |
| [Insert Shipment Order](actions/insert-shipment-order.md) | `POST en/api/IntegrationApi/:methodName` | [docs](https://developer.logiwa.com/?id=5df0db19e6466c2eec992f4d) |
| [List Inventory](actions/list-inventory.md) | `POST en/api/IntegrationApi/ListingInventoryReport` | [docs](https://mydeveloper.logiwa.com/#tag/Inventory/paths/~1v3.1~1Inventory~1list~1i~1%7Bindex%7D~1s~1%7Bsize%7D/get) |
| [List Inventory Stock Levels](actions/list-inventory-stock-levels.md) | `POST en/api/IntegrationApi/GetAvailableStockInfo` | [docs](https://developer.logiwa.com/?id=5ed03a00e6466c102c89922a) |
| [List Locations](actions/list-locations.md) | `POST en/api/IntegrationApi/LocationSearch` | [docs](https://developer.logiwa.com/?id=63b437efe6466c3cdcb7321a) |
| [List Pack Types (GET)](actions/list-pack-types-get.md) | `POST /en/api/IntegrationApi/InventoryItemPackTypeGET` | [docs](https://developer.logiwa.com/?id=5e71514fe6466c0c70d9c50a) |
| [List Products](actions/list-products.md) | `POST en/api/IntegrationApi/InventoryItemSearch` | [docs](https://developer.logiwa.com/?id=5df0daa0e6466c2eec992f43) |
| [List Purchase Orders](actions/list-purchase-orders.md) | `POST en/api/IntegrationApi/PurchaseOrderSearch` | [docs](https://developer.logiwa.com/?id=5df0dbf9e6466c2eec992f5d) |
| [List Receipt Orders](actions/list-receipt-orders.md) | `POST en/api/IntegrationApi/WarehouseReceiptSearch` | [docs](https://developer.logiwa.com/?id=5df0dcafe6466c2eec992f67) |
| [List Shipment Info - Import](actions/list-shipment-info-import.md) | `POST en/api/IntegrationApi/ShipmentReportAllSearch` |  |
| [List Shipment Orders](actions/list-shipment-orders.md) | `POST en/api/IntegrationApi/WarehouseOrderSearch` | [docs](https://developer.logiwa.com/?id=5df0db0be6466c2eec992f4b) |
| [Update Receipt Order Detail](actions/update-receipt-order-detail.md) | `POST en/api/IntegrationApi/WarehouseReceiptDetailUpdate` | [docs](https://developer.logiwa.com/?id=62c7ce4be6466c3080236a04) |
