# Faire: Native API Reference

A consolidated summary of Faire's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://faire.github.io/external-api-docs/#introduction
- **OpenAPI specification:** https://faire.github.io/external-api-docs/#introduction
- **API base URL:** `https://www.faire.com/external-api/v2/`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-FAIRE-ACCESS-TOKEN: <apiKey>
```

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

Responses from this API use plain text. The next-page cursor is read from `cursor`.

## Pagination

Use `limit` in the query string to set the page size (default 50; minimum 50). Use `cursor` in the query string as the pagination cursor.

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Shipments to Order](actions/add-shipments-to-order.md) | `POST orders/:orderId/shipments` | [docs](https://developers.faire.com/docs#/paths/orders-order_id--shipments/post) |
| [Get product inventory by SKUs](actions/get-product-inventory-by-skus.md) | `GET product-inventory/by-skus` | [docs](https://developers.faire.com/docs#/paths/product-inventory-by-skus/get) |
| [List a single Order](actions/list-a-single-order.md) | `GET orders/:id` | [docs](https://faire.github.io/external-api-docs/#get-all-orders) |
| [List Orders](actions/list-orders.md) | `GET orders` | [docs](https://faire.github.io/external-api-docs/#get-all-orders) |
| [Update inventory by SKUs](actions/update-inventory.md) | `PATCH product-inventory/by-skus` | [docs](https://faire.github.io/external-api-docs/#get-all-orders) |
