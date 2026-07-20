# Extensiv Order Manager: Native API Reference

A consolidated summary of Extensiv Order Manager's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://documentation.skubana.com/pages/order-manager.html
- **API base URL:** `https://api.skubana.com`

## Authentication

### Bearer Access Token

Use an Extensiv Order Manager API bearer token for requests to the Order Manager API.

### Credentials

- **Access Token:** `accessToken` · optional · Extensiv Order Manager API bearer token. Enter the token value without the Bearer prefix.

Send these headers with each API request:

```http
Authorization: Bearer <accessToken>
```

[Official authentication documentation](https://documentation.skubana.com/pages/order-manager.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 10–1000). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create External Shipment](actions/create-external-shipment.md) | `PUT /v1.1/shipment/external` | [docs](https://documentation.skubana.com/pages/order-manager.html#tag/Shipment/operation/putExternalShipmentUsingPUT_1) |
| [Create Order](actions/create-order.md) | `PUT /v1/order` | [docs](https://documentation.skubana.com/pages/order-manager.html#tag/Order/operation/putOrderUsingPUT) |
| [Create Standard Shipment](actions/create-standard-shipment.md) | `PUT /v1.1/shipment/standard` | [docs](https://documentation.skubana.com/pages/order-manager.html#tag/Shipment/operation/putShipmentUsingPUT_1) |
| [Get Order](actions/get-order.md) | `GET /v1.1/orders/:orderId` | [docs](https://documentation.skubana.com/pages/order-manager.html#tag/Order/operation/getOrderUsingGET_1) |
| [List Orders](actions/list-orders.md) | `GET /v1.1/orders` | [docs](https://documentation.skubana.com/pages/order-manager.html#tag/Order/operation/getOrdersUsingGET_1) |
| [List Product Listings](actions/list-product-listings.md) | `GET /v1/listings` | [docs](https://documentation.skubana.com/pages/order-manager.html#tag/Listings/operation/getListingsUsingGET) |
| [List Shipments](actions/list-shipments.md) | `GET /v1/shipments` | [docs](https://documentation.skubana.com/pages/order-manager.html#tag/Shipment/operation/getShipmentsUsingGET) |
| [Update Orders](actions/update-orders.md) | `POST /v1.1/orders` | [docs](https://documentation.skubana.com/pages/order-manager.html#tag/Order/operation/postOrderUsingPOST_1) |
