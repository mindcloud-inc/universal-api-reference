# Cin7 Core: Native API Reference

A consolidated summary of Cin7 Core's API configuration and 15 documented operations, with links to official documentation.

- **Official docs:** https://dearinventory.docs.apiary.io/#
- **API base URL:** `https://inventory.dearsystems.com/externalapi/v2/`

## Authentication

### Custom

The REST API uses the following headers for authentication: 
- api-auth-accountid 
- api-auth-applicationkey

### Credentials

- **Account Id:** `accountId` · required
- **Application Key:** `applicationKey` · required

Send these headers with each API request:

```http
api-auth-accountid: <accountId>
api-auth-applicationkey: <applicationKey>
```

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Pagination

Use `Limit` in the query string to set the page size (default 100; accepted range 1–1000). Use `Page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string. Supported operators: `between`, `contain`, `empty`, `eq`, `exist`, `gt`, `gte`, `includes`, `lt`, `lte`, `ncontain`, `ne`, `nempty`, `nexist`.

## Endpoints (15 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Carrier](actions/create-carrier.md) | `POST ref/carrier` | [docs](https://dearinventory.docs.apiary.io/#reference/sale/sale-fulfilment-pack/post) |
| [Create Sale Fulfillment Pack](actions/create-sale-fulfillment-pack.md) | `POST sale/fulfilment/pack` | [docs](https://dearinventory.docs.apiary.io/#reference/sale/sale-fulfilment-pack/post) |
| [Create Sale Fulfillment Pick](actions/create-sale-fulfillment-pick.md) | `POST sale/fulfilment/pick` | [docs](https://dearinventory.docs.apiary.io/#reference/sale/sale-fulfilment-pack/post) |
| [Create Sale Fulfillment Ship](actions/create-sale-fulfillment-ship.md) | `POST sale/fulfilment/ship` | [docs](https://dearinventory.docs.apiary.io/#reference/sale/sale-fulfilment-ship/post) |
| [Get Sale](actions/get-sale.md) | `GET sale` | [docs](https://dearinventory.docs.apiary.io/#reference/sale/sale/get) |
| [Get Sale Attachment](actions/get-sale-attachments.md) | `GET sale/attachment` | [docs](https://dearinventory.docs.apiary.io/#reference/sale/sale/get) |
| [Get Sale Fulfillment](actions/get-sale-fulfillment.md) | `GET sale/fulfilment` | [docs](https://dearinventory.docs.apiary.io/#reference/sale/sale-fulfilment/get) |
| [Get Sale Fulfillment Pack](actions/get-sale-fulfillment-pack.md) | `GET sale/fulfilment/pack` | [docs](https://dearinventory.docs.apiary.io/#reference/sale/sale-fulfilment-pack/get) |
| [Get Sale Fulfillment Ship](actions/get-sale-fulfillment-ship.md) | `GET sale/fulfilment/ship` | [docs](https://dearinventory.docs.apiary.io/#reference/sale/sale-fulfilment-ship/get) |
| [Get Sale Order](actions/get-sale-order.md) | `GET sale/order` | [docs](https://dearinventory.docs.apiary.io/#reference/sale/sale-fulfilment/get) |
| [List Carriers](actions/list-carriers.md) | `GET ref/carrier` | [docs](https://dearinventory.docs.apiary.io/#reference/sale/sale-fulfilment/get) |
| [List Sales](actions/list-sales.md) | `GET saleList` | [docs](https://dearinventory.docs.apiary.io/#reference/sale/sale-list) |
| [List Products](actions/new-action1.md) | `GET product` | [docs](https://dearinventory.docs.apiary.io/#reference/product/product/get) |
| [Update Sale Fulfillment Pack](actions/update-sale-fulfillment-pack.md) | `PUT sale/fulfilment/pack` | [docs](https://dearinventory.docs.apiary.io/#reference/sale/sale-fulfilment-pack/put) |
| [Update Sale Fulfillment Ship](actions/update-sale-fulfillment-ship.md) | `PUT sale/fulfilment/ship` | [docs](https://dearinventory.docs.apiary.io/#reference/sale/sale-fulfilment-ship/put) |
