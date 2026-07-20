# Big Cartel: Native API Reference

A consolidated summary of Big Cartel's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://developers.bigcartel.com/api/v1/
- **API base URL:** `https://api.bigcartel.com`

## Authentication

### Private Store Basic Auth

Private single-store HTTP Basic authentication using store subdomain and password.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://developers.bigcartel.com/api/v1)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.api+json` |
| `Content-Type` | `application/vnd.api+json` |
| `User-Agent` | `MindCloud/1.0 (https://mindcloud.co)` |

Responses from this API use JSON.

## Pagination

Use `page[limit]` in the query string to set the page size (default 20). Use `page[offset]` in the query string as the record offset; numbering starts at 0.

## Sorting

Set the sort field with `sort` in the query string. Set the direction separately with `sort_direction`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Category](actions/create-category.md) | `POST /v1/accounts/[:account-id]/categories` | [docs](https://developers.bigcartel.com/api/v1) |
| [Create Discount](actions/create-discount.md) | `POST /v1/accounts/[:account-id]/discounts` | [docs](https://developers.bigcartel.com/api/v1) |
| [Create Page](actions/create-page.md) | `POST /v1/accounts/[:account-id]/pages` | [docs](https://developers.bigcartel.com/api/v1) |
| [Create Shipment](actions/create-shipment.md) | `POST /v1/accounts/[:account-id]/orders/[:order-id]/shipments` | [docs](https://developers.bigcartel.com/api/v1) |
| [Delete Category](actions/delete-category.md) | `DELETE /v1/accounts/[:account-id]/categories/[:category-id]` | [docs](https://developers.bigcartel.com/api/v1) |
| [Delete Discount](actions/delete-discount.md) | `DELETE /v1/accounts/[:account-id]/discounts/[:discount-id]` | [docs](https://developers.bigcartel.com/api/v1) |
| [Delete Shipment](actions/delete-shipment.md) | `DELETE /v1/accounts/[:account-id]/orders/[:order-id]/shipments/[:shipment-id]` | [docs](https://developers.bigcartel.com/api/v1) |
| [Get Abandoned Cart](actions/get-abandoned-cart.md) | `GET /v1/accounts/[:account-id]/carts/[:cart-id]` | [docs](https://developers.bigcartel.com/api/v1) |
| [Get Account](actions/get-account.md) | `GET /v1/accounts` | [docs](https://developers.bigcartel.com/api/v1) |
| [Get All Abandoned Carts](actions/get-all-abandoned-carts.md) | `GET /v1/accounts/[:account-id]/carts` | [docs](https://developers.bigcartel.com/api/v1) |
| [Get All Categories](actions/get-all-categories.md) | `GET /v1/accounts/[:account-id]/categories` | [docs](https://developers.bigcartel.com/api/v1) |
| [Get All Discounts](actions/get-all-discounts.md) | `GET /v1/accounts/[:account-id]/discounts` | [docs](https://developers.bigcartel.com/api/v1) |
| [Get All Orders](actions/get-all-orders.md) | `GET /v1/accounts/[:account-id]/orders` | [docs](https://developers.bigcartel.com/api/v1) |
| [Get All Pages](actions/get-all-pages.md) | `GET /v1/accounts/[:account-id]/pages` | [docs](https://developers.bigcartel.com/api/v1) |
| [Get All Products](actions/get-all-products.md) | `GET /v1/accounts/[:account-id]/products` | [docs](https://developers.bigcartel.com/api/v1) |
| [Get All Shipments](actions/get-all-shipments.md) | `GET /v1/accounts/[:account-id]/orders/[:order-id]/shipments` | [docs](https://developers.bigcartel.com/api/v1) |
| [Get Category](actions/get-category.md) | `GET /v1/accounts/[:account-id]/categories/[:category-id]` | [docs](https://developers.bigcartel.com/api/v1) |
| [Get Discount](actions/get-discount.md) | `GET /v1/accounts/[:account-id]/discounts/[:discount-id]` | [docs](https://developers.bigcartel.com/api/v1) |
| [Get Order](actions/get-order.md) | `GET /v1/accounts/[:account-id]/orders/[:order-id]` | [docs](https://developers.bigcartel.com/api/v1) |
| [Get Page](actions/get-page.md) | `GET /v1/accounts/[:account-id]/pages/[:page-id]` | [docs](https://developers.bigcartel.com/api/v1) |
| [Get Product](actions/get-product.md) | `GET /v1/accounts/[:account-id]/products/[:product-id]` | [docs](https://developers.bigcartel.com/api/v1) |
| [Get Shipment](actions/get-shipment.md) | `GET /v1/accounts/[:account-id]/orders/[:order-id]/shipments/[:shipment-id]` | [docs](https://developers.bigcartel.com/api/v1) |
| [Reposition Categories](actions/reposition-categories.md) | `PATCH /v1/accounts/[:account-id]/relationships/categories` | [docs](https://developers.bigcartel.com/api/v1) |
| [Reposition Products](actions/reposition-products.md) | `PATCH /v1/accounts/[:account-id]/relationships/products` | [docs](https://developers.bigcartel.com/api/v1) |
| [Update Category](actions/update-category.md) | `PATCH /v1/accounts/[:account-id]/categories/[:category-id]` | [docs](https://developers.bigcartel.com/api/v1) |
| [Update Discount](actions/update-discount.md) | `PATCH /v1/accounts/[:account-id]/discounts/[:discount-id]` | [docs](https://developers.bigcartel.com/api/v1) |
| [Update Order](actions/update-order.md) | `PATCH /v1/accounts/[:account-id]/orders/[:order-id]` | [docs](https://developers.bigcartel.com/api/v1) |
| [Update Page](actions/update-page.md) | `PATCH /v1/accounts/[:account-id]/pages/[:page-id]` | [docs](https://developers.bigcartel.com/api/v1) |
| [Update Product](actions/update-product.md) | `PATCH /v1/accounts/[:account-id]/products/[:product-id]` | [docs](https://developers.bigcartel.com/api/v1) |
| [Update Shipment](actions/update-shipment.md) | `PATCH /v1/accounts/[:account-id]/orders/[:order-id]/shipments/[:shipment-id]` | [docs](https://developers.bigcartel.com/api/v1) |
