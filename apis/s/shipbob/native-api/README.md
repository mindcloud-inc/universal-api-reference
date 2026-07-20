# ShipBob: Native API Reference

A consolidated summary of ShipBob's API configuration and 12 documented operations.

- **REST base URL:** `https://{apiSubdomain}.shipbob.com/`
- **REST - Cursor base URL:** `https://{apiSubdomain}.shipbob.com/`
- **REST no ChannelID base URL:** `https://{apiSubdomain}.shipbob.com/`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required
- **API Subdomain:** `apiSubdomain` · optional

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

## API conventions

### REST

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

### REST - Cursor

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

### REST no ChannelID

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Pagination

- **REST:** Use `Page` in the query string to choose the page; numbering starts at 1.
- **REST - Cursor:** Use `pageSize` in the query string to set the page size (default 50; accepted range 50–500). Use `cursor` in the query string as the pagination cursor.
- **REST no ChannelID:** Use `Limit` in the query string to set the page size (default 250; accepted range 50–250). Use `Page` in the query string to choose the page; numbering starts at 1.

## Endpoints (12 documented)

| Operation | API | Method & path | Vendor docs |
| --- | --- | --- | --- |
| [Get Fulfillment Centers](actions/get-fulfillment-centers.md) | REST | `GET 1.0/fulfillmentCenter` |  |
| [Get Inventory Level](actions/get-inventory-level.md) | REST | `GET /2025-07/inventory-level/{{inventoryId}}/locations` |  |
| [Get Multiple Products](actions/get-multiple-products.md) | REST | `GET 1.0/product` |  |
| [Get Multiple Warehouse Receiving Orders](actions/get-multiple-warehouse-receiving-orders.md) | REST | `GET 2.0/receiving-extended` |  |
| [Get Orders](actions/get-orders.md) | REST | `GET 2025-07/order` | [docs](https://developer.shipbob.com/api/2025-07/orders/get-orders) |
| [Get Product](actions/get-product.md) | REST | `GET 2025-07/product/{{productId}}` |  |
| [Get Warehouse Receiving Order](actions/get-warehouse-receiving-order.md) | REST | `GET https://api.shipbob.com/2026-01/receiving/:id` |  |
| [Get Warehouse Receivng Order Boxes](actions/get-warehouse-receivng-order-boxes.md) | REST | `GET 2026-01/receiving/{{id}}/boxes` |  |
| [List Inventory Items](actions/list-inventory-items.md) | REST | `GET 1.0/inventory` |  |
| [List Inventory Levels by Location](actions/list-inventory-levels-by-location.md) | REST - Cursor | `GET 2025-07/inventory-level/locations?` | [docs](https://developer.shipbob.com/) |
| [Post Product](actions/post-product.md) | REST | `POST 1.0/product` |  |
| [Post Warehouse Receiving Order (Extended)](actions/post-warehouse-receiving-order-extended.md) | REST | `POST 2.0/receiving-extended` |  |
