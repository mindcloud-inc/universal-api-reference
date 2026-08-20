# MarketTime: Native API Reference

A consolidated summary of MarketTime's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://publicapi.markettime.com/swagger-ui/index.html
- **OpenAPI specification:** https://publicapi.markettime.com/v3/api-docs/v1
- **API base URL:** `https://publicapi.markettime.com`

## Authentication

### API Key

Authenticate with a MarketTime Public API key.

### Credentials

- **API Key:** `apiKey` · required
- **Account ID:** `whoAmI` · required · Your MarketTime Manufacturer or RepGroup ID, such as M26662.

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://support.markettime.com/hc/en-us/articles/43441619857947-Generating-an-API-Key-for-your-MarketTime-Account)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `response`.

## Pagination

Use `recordSize` in the query string to set the page size (default 50; accepted range 1–250). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Item Inventory](actions/get-item-inventory.md) | `GET /mtpublic/api/v1/:whoAmI/items/inventory/:itemID` | [docs](https://publicapi.markettime.com/swagger-ui/index.html#/Item/getSingleItemInventoryDetail) |
| [List Item Inventory](actions/list-item-inventory.md) | `GET /mtpublic/api/v1/:whoAmI/items/inventory` | [docs](https://publicapi.markettime.com/swagger-ui/index.html#/Item/getItemInventoryDetails) |
| [List Items by Item ID](actions/list-items-by-item-id.md) | `GET /mtpublic/api/v1/:whoAmI/items/:itemID` | [docs](https://publicapi.markettime.com/swagger-ui/index.html#/Item/getItemsDetailsByItemID) |
| [Pull Orders](actions/pull-orders.md) | `POST /mtpublic/api/v1/:whoAmI/orders/get` | [docs](https://publicapi.markettime.com/swagger-ui/index.html#/Order/queryOrders) |
| [Update Item Inventory](actions/update-item-inventory.md) | `PUT /mtpublic/api/v1/:whoAmI/items/:whatItemDoIWantToUpdate` | [docs](https://publicapi.markettime.com/swagger-ui/index.html#/Item/updateItem) |
