# Keysender: Native API Reference

A consolidated summary of Keysender's API configuration and 39 documented operations, with links to official documentation.

- **Official docs:** https://panel.keysender.co.uk/api
- **OpenAPI specification:** https://panel.keysender.co.uk/api/v1.0.0/openapi
- **API base URL:** `https://panel.keysender.co.uk/api/v1.0`

## Authentication

### Bearer Token

Use a Keysender bearer access token generated from the API login endpoint.

### Credentials

- **Access Token:** `accessToken` · optional · Paste the bearer access token returned by POST /login.

Send these headers with each API request:

```http
Authorization: Bearer <accessToken>
```

[Official authentication documentation](https://panel.keysender.co.uk/api)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (39 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Custom Transaction](actions/add-custom-transaction.md) | `POST /transaction/addcustom` | [docs](https://panel.keysender.co.uk/api) |
| [Add Transaction From Source](actions/add-transaction-from-source.md) | `POST /transaction/add` | [docs](https://panel.keysender.co.uk/api) |
| [Cancel Order Item](actions/cancel-order-item.md) | `POST /catalog/order/cancel-item` | [docs](https://panel.keysender.co.uk/api) |
| [Create Customer](actions/create-customer.md) | `POST /customer` | [docs](https://panel.keysender.co.uk/api) |
| [Create Database](actions/create-database.md) | `POST /database` | [docs](https://panel.keysender.co.uk/api) |
| [Create Order From Reservation](actions/create-order-from-reservation.md) | `POST /catalog/order` | [docs](https://panel.keysender.co.uk/api) |
| [Delete Code](actions/delete-code.md) | `DELETE /code` | [docs](https://panel.keysender.co.uk/api) |
| [Delete Customer](actions/delete-customer.md) | `DELETE /customer` | [docs](https://panel.keysender.co.uk/api) |
| [Delete Database](actions/delete-database.md) | `DELETE /database` | [docs](https://panel.keysender.co.uk/api) |
| [Get Codes](actions/get-codes.md) | `GET /codes` | [docs](https://panel.keysender.co.uk/api) |
| [Get Customer](actions/get-customer.md) | `GET /customer` | [docs](https://panel.keysender.co.uk/api) |
| [Get Database](actions/get-database.md) | `GET /database` | [docs](https://panel.keysender.co.uk/api) |
| [Get Databases](actions/get-databases.md) | `GET /databases` | [docs](https://panel.keysender.co.uk/api) |
| [Get Order Details](actions/get-order-details.md) | `GET /catalog/order` | [docs](https://panel.keysender.co.uk/api) |
| [Get Product By SKU](actions/get-product-by-sku.md) | `GET /catalog/products/:sku` | [docs](https://panel.keysender.co.uk/api) |
| [List Discounted Products](actions/list-discounted-products.md) | `GET /catalog/products` | [docs](https://panel.keysender.co.uk/api) |
| [List Products](actions/list-products.md) | `GET /catalog/products` | [docs](https://panel.keysender.co.uk/api) |
| [List Products By Category](actions/list-products-by-category.md) | `GET /catalog/products` | [docs](https://panel.keysender.co.uk/api) |
| [List Products By Category And Region](actions/list-products-by-category-and-region.md) | `GET /catalog/products` | [docs](https://panel.keysender.co.uk/api) |
| [List Products By Language](actions/list-products-by-language.md) | `GET /catalog/products` | [docs](https://panel.keysender.co.uk/api) |
| [List Products By Maximum Price](actions/list-products-by-maximum-price.md) | `GET /catalog/products` | [docs](https://panel.keysender.co.uk/api) |
| [List Products By Minimum Price](actions/list-products-by-minimum-price.md) | `GET /catalog/products` | [docs](https://panel.keysender.co.uk/api) |
| [List Products By Minimum Quantity](actions/list-products-by-minimum-quantity.md) | `GET /catalog/products` | [docs](https://panel.keysender.co.uk/api) |
| [List Products By Price Range](actions/list-products-by-price-range.md) | `GET /catalog/products` | [docs](https://panel.keysender.co.uk/api) |
| [List Products By Region](actions/list-products-by-region.md) | `GET /catalog/products` | [docs](https://panel.keysender.co.uk/api) |
| [List Products By Region And Language](actions/list-products-by-region-and-language.md) | `GET /catalog/products` | [docs](https://panel.keysender.co.uk/api) |
| [List Products By Type](actions/list-products-by-type.md) | `GET /catalog/products` | [docs](https://panel.keysender.co.uk/api) |
| [List Products For Bulk Fulfillment](actions/list-products-for-bulk-fulfillment.md) | `GET /catalog/products` | [docs](https://panel.keysender.co.uk/api) |
| [List Products Sorted By Price Descending](actions/list-products-sorted-by-price-descending.md) | `GET /catalog/products` | [docs](https://panel.keysender.co.uk/api) |
| [List Products Updated Since](actions/list-products-updated-since.md) | `GET /catalog/products` | [docs](https://panel.keysender.co.uk/api) |
| [List Products With Additional Information](actions/list-products-with-additional-information.md) | `GET /catalog/products` | [docs](https://panel.keysender.co.uk/api) |
| [Reserve Catalog Items](actions/reserve-catalog-items.md) | `POST /catalog/reserve` | [docs](https://panel.keysender.co.uk/api) |
| [Search Products By Name](actions/search-products-by-name.md) | `GET /catalog/products` | [docs](https://panel.keysender.co.uk/api) |
| [Search Products By SKU](actions/search-products-by-sku.md) | `GET /catalog/products` | [docs](https://panel.keysender.co.uk/api) |
| [Top Up Order Item](actions/top-up-order-item.md) | `POST /catalog/order/top-up` | [docs](https://panel.keysender.co.uk/api) |
| [Update Code](actions/update-code.md) | `PUT /code` | [docs](https://panel.keysender.co.uk/api) |
| [Update Customer](actions/update-customer.md) | `PUT /customer` | [docs](https://panel.keysender.co.uk/api) |
| [Update Database](actions/update-database.md) | `PUT /database` | [docs](https://panel.keysender.co.uk/api) |
| [Upload Text Codes](actions/upload-text-codes.md) | `POST /code` | [docs](https://panel.keysender.co.uk/api) |
