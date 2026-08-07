# ShipBob: Native API Reference

A consolidated summary of ShipBob's API configuration and 14 documented operations.

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

## Sorting

- **REST - Cursor:** Set the sort field with `Sortby` in the query string. Set the direction separately with `SortOrder`. Use `Asc` for ascending order and `Desc` for descending order. Only one sort field is accepted.

## Endpoints (14 documented)

| Operation | API | Method & path | Vendor docs |
| --- | --- | --- | --- |
| [Get Fulfillment Centers](actions/get-fulfillment-centers.md) | REST | `GET 2026-07/fulfillment-center` |  |
| [Get Inventory Level](actions/get-inventory-level.md) | REST | `GET /2026-07/inventory-level/{{inventoryId}}/locations` |  |
| [Get Multiple Products](actions/get-multiple-products.md) | REST | `GET 2026-07/product` |  |
| [Get Multiple Warehouse Receiving Orders](actions/get-multiple-warehouse-receiving-orders.md) | REST | `GET 2026-07/receiving` |  |
| [Get Orders](actions/get-orders.md) | REST | `GET 2026-07/order` | [docs](https://developer.shipbob.com/api/2025-07/orders/get-orders) |
| [Get Product](actions/get-product.md) | REST | `GET 2026-07/product/{{productId}}` |  |
| [Get Return Order](actions/get-return-order.md) | REST - Cursor | `GET 2026-07/return/:id` | [docs](https://developer.shipbob.com/api/returns/get-return-order) |
| [Get Warehouse Receiving Order](actions/get-warehouse-receiving-order.md) | REST | `GET https://api.shipbob.com/2026-01/receiving/:id` |  |
| [Get Warehouse Receivng Order Boxes](actions/get-warehouse-receivng-order-boxes.md) | REST | `GET 2026-07/receiving/{{id}}/boxes` |  |
| [List Inventory Items](actions/list-inventory-items.md) | REST | `GET 2026-07/inventory` |  |
| [List Inventory Levels by Location](actions/list-inventory-levels-by-location.md) | REST - Cursor | `GET 2026-07/inventory-level/locations?` | [docs](https://developer.shipbob.com/) |
| [List Return Orders](actions/list-return-orders.md) | REST - Cursor | `GET 2026-07/return` | [docs](https://developer.shipbob.com/api/returns/get-return-orders) |
| [Post Product](actions/post-product.md) | REST | `POST 2026-07/product` | [docs](https://developer-stage.shipbob.dev/2026-07/api/products/create-product) |
| [Post Warehouse Receiving Order](actions/post-warehouse-receiving-order.md) | REST | `POST 2026-07/receiving` | [docs](https://developer.shipbob.com/api/receiving/create-warehouse-receiving-order) |
