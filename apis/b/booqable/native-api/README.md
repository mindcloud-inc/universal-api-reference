# Booqable: Native API Reference

A consolidated summary of Booqable's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://developers.booqable.com/
- **API base URL:** `https://mindcloud.booqable.com/api/4`

## Authentication

### API Key

Authenticate Booqable requests with a personal access token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.booqable.com/#introduction/access-token)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `page[size]` in the query string to set the page size. Use `page[number]` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string. Supported operators: `eq`, `gt`, `gte`, `lt`, `lte`, `ne`.

## Sorting

Set the sort field with `sort` in the query string. Prefix the field name to select its direction. Multiple sort fields can be combined.

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | `POST /customers` | [docs](https://developers.booqable.com/#customers-create-a-customer) |
| [Create Order](actions/create-order.md) | `POST /orders` | [docs](https://developers.booqable.com/#orders-create-an-order) |
| [Create Product](actions/create-product.md) | `POST /products` | [docs](https://developers.booqable.com/#products-create-a-product) |
| [Get Customer](actions/get-customer.md) | `GET /customers/:id` | [docs](https://developers.booqable.com/#customers-fetch-a-customer) |
| [Get Item](actions/get-item.md) | `GET /items/:id` | [docs](https://developers.booqable.com/#items-fetch-an-item) |
| [Get New Order](actions/get-new-order.md) | `GET /orders/new` | [docs](https://developers.booqable.com/#orders-new-order) |
| [Get Order](actions/get-order.md) | `GET /orders/:id` | [docs](https://developers.booqable.com/#orders-fetch-an-order) |
| [Get Product](actions/get-product.md) | `GET /products/:id` | [docs](https://developers.booqable.com/#products-fetch-a-product) |
| [Get Product Availability](actions/get-product-availability.md) | `GET /availabilities` | [docs](https://developers.booqable.com/#availabilities-fetch-availability-for-a-product) |
| [Get Stock Item](actions/get-stock-item.md) | `GET /stock_items/:id` | [docs](https://developers.booqable.com/#stock-items-fetch-a-stock_item) |
| [List Customers](actions/list-customers.md) | `GET /customers` | [docs](https://developers.booqable.com/#customers-list-customers) |
| [List Items](actions/list-items.md) | `GET /items` | [docs](https://developers.booqable.com/#items-list-items) |
| [List Orders](actions/list-orders.md) | `GET /orders` | [docs](https://developers.booqable.com/#orders-list-orders) |
| [List Products](actions/list-products.md) | `GET /products` | [docs](https://developers.booqable.com/#products-list-products) |
| [List Stock Items](actions/list-stock-items.md) | `GET /stock_items` | [docs](https://developers.booqable.com/#stock-items-list-stock_items) |
| [Search Customers](actions/search-customers.md) | `POST /customers/search` | [docs](https://developers.booqable.com/#customers-search-customers) |
| [Search Items](actions/search-items.md) | `POST /items/search` | [docs](https://developers.booqable.com/#items-search-items) |
| [Search Orders](actions/search-orders.md) | `POST /orders/search` | [docs](https://developers.booqable.com/#orders-search-orders) |
| [Search Products](actions/search-products.md) | `POST /products/search` | [docs](https://developers.booqable.com/#products-search-products) |
| [Update Customer](actions/update-customer.md) | `PUT /customers/:id` | [docs](https://developers.booqable.com/#customers-update-a-customer) |
| [Update Order](actions/update-order.md) | `PUT /orders/:id` | [docs](https://developers.booqable.com/#orders-update-an-order) |
| [Update Product](actions/update-product.md) | `PUT /products/:id` | [docs](https://developers.booqable.com/#products-update-a-product) |
| [Update Stock Item](actions/update-stock-item.md) | `PUT /stock_items/:id` | [docs](https://developers.booqable.com/#stock-items-update-a-stock_item) |
