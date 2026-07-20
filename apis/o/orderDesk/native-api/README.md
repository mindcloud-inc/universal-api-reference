# Order Desk: Native API Reference

A consolidated summary of Order Desk's API configuration and 18 documented operations, with links to official documentation.

- **Official docs:** https://apidocs.orderdesk.com/
- **API base URL:** `https://app.orderdesk.me/api/v2`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required
- **Store ID:** `storeId` · required · Your Order Desk store ID.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://apidocs.orderdesk.com/)

## Pagination

Use `limit` in the query string to set the page size (default 50). Use `offset` in the query string as the record offset.

## Endpoints (18 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Inventory Item](actions/create-inventory-item.md) | `POST /inventory-items` | [docs](https://apidocs.orderdesk.com/?shell=#create-an-inventory-item) |
| [Create Multiple Shipments](actions/create-multiple-shipments.md) | `POST /batch-shipments` | [docs](https://apidocs.orderdesk.com/?shell=#create-multiple-shipments) |
| [Create Order](actions/create-order.md) | `POST /orders` | [docs](https://apidocs.orderdesk.com/?shell=#create-an-order) |
| [Create Shipment](actions/create-shipment.md) | `POST /orders/:orderId/shipments` | [docs](https://apidocs.orderdesk.com/?shell=#create-a-shipment) |
| [Delete Inventory Item](actions/delete-inventory-item.md) | `DELETE /inventory-items/:inventoryItemId` | [docs](https://apidocs.orderdesk.com/?shell=#delete-an-inventory-item) |
| [Delete Shipment](actions/delete-shipment.md) | `DELETE /orders/:orderId/shipments/:shipmentId` | [docs](https://apidocs.orderdesk.com/?shell=#delete-a-shipment) |
| [Get Inventory Item](actions/get-inventory-item.md) | `GET /inventory-items/:inventoryItemId` | [docs](https://apidocs.orderdesk.com/?shell=#get-a-single-inventory-item) |
| [Get Order](actions/get-order.md) | `GET /orders/:orderId` | [docs](https://apidocs.orderdesk.com/?shell=#get-a-single-order) |
| [Get Order Item](actions/get-order-item.md) | `GET /orders/:orderId/order-items/:orderItemId` | [docs](https://apidocs.orderdesk.com/?shell=#get-a-single-order-item) |
| [Get Shipment](actions/get-shipment.md) | `GET /orders/:orderId/shipments/:shipmentId` | [docs](https://apidocs.orderdesk.com/?shell=#get-a-single-shipment) |
| [Get Store Settings](actions/get-store-settings.md) | `GET /store` | [docs](https://apidocs.orderdesk.com/?shell=#store-settings) |
| [List Inventory Items](actions/list-inventory-items.md) | `GET /inventory-items` | [docs](https://apidocs.orderdesk.com/?shell=#get-all-inventory-items) |
| [List Order Items](actions/list-order-items.md) | `GET /orders/:orderId/order-items` | [docs](https://apidocs.orderdesk.com/?shell=#get-all-order-items) |
| [List Orders](actions/list-orders.md) | `GET /orders` | [docs](https://apidocs.orderdesk.com/?shell=#get-multiple-orders) |
| [List Shipments](actions/list-shipments.md) | `GET /orders/:orderId/shipments` | [docs](https://apidocs.orderdesk.com/?shell=#get-all-shipments) |
| [Update Inventory Item](actions/update-inventory-item.md) | `PUT /inventory-items/:inventoryItemId` | [docs](https://apidocs.orderdesk.com/?shell=#update-a-single-inventory-item) |
| [Update Multiple Inventory Items](actions/update-multiple-inventory-items.md) | `PUT /batch-inventory-items` | [docs](https://apidocs.orderdesk.com/?shell=#update-multiple-inventory-items) |
| [Update Shipment](actions/update-shipment.md) | `PUT /orders/:orderId/shipments/:shipmentId` | [docs](https://apidocs.orderdesk.com/?shell=#update-a-shipment) |
