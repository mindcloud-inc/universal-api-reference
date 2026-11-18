# Brightpearl: Native API Reference

A consolidated summary of Brightpearl's API configuration and 17 documented operations, with links to official documentation.

- **Official docs:** https://api-docs.brightpearl.com/
- **API base URL:** `https://{apiDomain}/public-api/{account}`

## Authentication

### Access Token

Use an OAuth access token from your approved Brightpearl integration. Renew the token and API domain manually when it expires.

### Credentials

- **Access Token:** `apiKey` · required
- **Account Code:** `account` · required · Brightpearl account code associated with the token.
- **API Domain:** `apiDomain` · required · Exact api_domain hostname from the token response, without https:// or a path.
- **Developer Reference:** `developerRef` · required · Developer reference for the approved integration.
- **App Reference:** `appRef` · required · App reference (client_id) for the approved integration.

Send these headers with each API request:

```http
brightpearl-app-ref: <appRef>
brightpearl-dev-ref: <developerRef>
```

[Official authentication documentation](https://api-docs.brightpearl.com/utilities/oauth-token/post.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `response`.

## Pagination

Use `pageSize` in the query string to set the page size (default 500; maximum 500). Use `firstResult` in the query string as the record offset; numbering starts at 1.

## Filtering

Send filters in the query string. Supported operators: `eq`.

## Sorting

Set the sort field with `sort` in the query string. Use `ASC` for ascending order and `DESC` for descending order. Multiple sort fields can be combined.

## Endpoints (17 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Goods-Out Note Events](actions/add-goods-out-note-events.md) | `POST /warehouse-service/goods-note/goods-out/:goodsOutNoteId/event` | [docs](https://api-docs.brightpearl.com/warehouse/goods-out-note%20event/post.html) |
| [Create Goods-In Note](actions/create-goods-in-note.md) | `POST /warehouse-service/order/:orderId/goods-note/goods-in` | [docs](https://api-docs.brightpearl.com/warehouse/goods-in-note/post.html) |
| [Create Goods-Out Notes](actions/create-goods-out-notes.md) | `POST /warehouse-service/order/:orderId/goods-note/goods-out` | [docs](https://api-docs.brightpearl.com/warehouse/goods-out-note/post.html) |
| [Create Order](actions/create-order.md) | `POST /order-service/order/` | [docs](https://api-docs.brightpearl.com/order/order/post.html) |
| [Create Stock Corrections](actions/create-stock-corrections.md) | `POST /warehouse-service/warehouse/:warehouseId/stock-correction` | [docs](https://api-docs.brightpearl.com/warehouse/stock-correction/post.html) |
| [Delete Goods-In Note](actions/delete-goods-in-note.md) | `DELETE /warehouse-service/goods-note/goods-in/:goodsInNoteId` | [docs](https://api-docs.brightpearl.com/warehouse/goods-in-note/delete.html) |
| [Delete Goods-Out Note](actions/delete-goods-out-note.md) | `DELETE /warehouse-service/order/:orderId/goods-note/goods-out/:goodsOutNoteId` | [docs](https://api-docs.brightpearl.com/warehouse/goods-out-note/delete.html) |
| [List Goods-In Notes](actions/list-goods-in-notes.md) | `GET /warehouse-service/goods-in-search` | [docs](https://api-docs.brightpearl.com/warehouse/goods-in-note/search.html) |
| [List Goods-In Notes by ID](actions/list-goods-in-notes-by-id.md) | `GET /warehouse-service/order/:orderIds/goods-note/goods-in/:goodsInNoteIds` | [docs](https://api-docs.brightpearl.com/warehouse/goods-in-note/get.html) |
| [List Goods-Out Notes](actions/list-goods-out-notes.md) | `GET /warehouse-service/goods-note/goods-out-search` | [docs](https://api-docs.brightpearl.com/warehouse/goods-out-note/search.html) |
| [List Goods-Out Notes by ID](actions/list-goods-out-notes-by-id.md) | `GET /warehouse-service/order/:orderIds/goods-note/goods-out/:goodsOutNoteIds` | [docs](https://api-docs.brightpearl.com/warehouse/goods-out-note/get.html) |
| [List Orders](actions/list-orders.md) | `GET /order-service/order-search` | [docs](https://api-docs.brightpearl.com/order/order/search.html) |
| [List Orders by ID](actions/list-orders-by-id.md) | `GET /order-service/order/:orderIds` | [docs](https://api-docs.brightpearl.com/order/order/get.html) |
| [List Product Availability](actions/list-product-availability.md) | `GET /warehouse-service/product-availability/:productIds` | [docs](https://api-docs.brightpearl.com/warehouse/product-availability/get.html) |
| [List Stock Corrections by ID](actions/list-stock-corrections-by-id.md) | `GET /warehouse-service/warehouse/:warehouseId/stock-correction/:stockCorrectionIds` | [docs](https://api-docs.brightpearl.com/warehouse/stock-correction/get.html) |
| [Update Goods-Out Note](actions/update-goods-out-note.md) | `PUT /warehouse-service/goods-note/goods-out/:goodsOutNoteId` | [docs](https://api-docs.brightpearl.com/warehouse/goods-out-note/put.html) |
| [Update Order](actions/update-order.md) | `PATCH /order-service/order/:orderId` | [docs](https://api-docs.brightpearl.com/order/order/patch.html) |
