# Swell: Native API Reference

A consolidated summary of Swell's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://developers.swell.is/backend-api/introduction
- **API base URL:** `https://api.swell.store`

## Authentication

### Basic

Use your Swell store ID and secret key for Backend API access.

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

[Official authentication documentation](https://developers.swell.is/backend-api/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The total page count is read from `page_count`. The current page number is read from `page`.

## Pagination

Use `limit` in the query string to set the page size (default 15; accepted range 1–1000). Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string. Supported operators: `eq`, `gt`, `gte`, `lt`, `lte`, `ne`.

## Sorting

Set the sort field with `sort` in the query string. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Account](actions/create-account.md) | `POST /accounts` | [docs](https://developers.swell.is/backend-api/accounts/create-an-account) |
| [Create Cart](actions/create-cart.md) | `POST /carts` | [docs](https://developers.swell.is/backend-api/carts/create-a-cart) |
| [Create Category](actions/create-category.md) | `POST /categories` | [docs](https://developers.swell.is/backend-api/categories/create-a-category) |
| [Create Coupon](actions/create-coupon.md) | `POST /coupons` | [docs](https://developers.swell.is/backend-api/coupons/create-a-coupon) |
| [Create Order](actions/create-order.md) | `POST /orders` | [docs](https://developers.swell.is/backend-api/orders/create-an-order) |
| [Create Product](actions/create-product.md) | `POST /products` | [docs](https://developers.swell.is/backend-api/products/create-a-product) |
| [Create Promotion](actions/create-promotion.md) | `POST /promotions` | [docs](https://developers.swell.is/backend-api/promotions/create-a-promotion) |
| [Create Variant](actions/create-variant.md) | `POST /products\:variants` | [docs](https://developers.swell.is/backend-api/variants/create-a-variant) |
| [Delete Account](actions/delete-account.md) | `DELETE /accounts/:id` | [docs](https://developers.swell.is/backend-api/accounts/delete-an-account) |
| [Delete Cart](actions/delete-cart.md) | `DELETE /carts/:id` | [docs](https://developers.swell.is/backend-api/carts/delete-a-cart) |
| [Delete Category](actions/delete-category.md) | `DELETE /categories/:id` | [docs](https://developers.swell.is/backend-api/categories/delete-a-category) |
| [Delete Coupon](actions/delete-coupon.md) | `DELETE /coupons/:id` | [docs](https://developers.swell.is/backend-api/coupons/delete-a-coupon) |
| [Delete Order](actions/delete-order.md) | `DELETE /orders/:id` | [docs](https://developers.swell.is/backend-api/orders/delete-an-order) |
| [Delete Product](actions/delete-product.md) | `DELETE /products/:id` | [docs](https://developers.swell.is/backend-api/products/delete-a-product) |
| [Delete Promotion](actions/delete-promotion.md) | `DELETE /promotions/:id` | [docs](https://developers.swell.is/backend-api/promotions/delete-a-promotion) |
| [Delete Variant](actions/delete-variant.md) | `DELETE /products\:variants/:id` | [docs](https://developers.swell.is/backend-api/variants/delete-a-variant) |
| [Get Account](actions/get-account.md) | `GET /accounts/:id` | [docs](https://developers.swell.is/backend-api/accounts/retrieve-an-account) |
| [Get Cart](actions/get-cart.md) | `GET /carts/:id` | [docs](https://developers.swell.is/backend-api/carts/retrieve-a-cart) |
| [Get Category](actions/get-category.md) | `GET /categories/:id` | [docs](https://developers.swell.is/backend-api/categories/retrieve-a-category) |
| [Get Coupon](actions/get-coupon.md) | `GET /coupons/:id` | [docs](https://developers.swell.is/backend-api/coupons/retrieve-a-coupon) |
| [Get Order](actions/get-order.md) | `GET /orders/:id` | [docs](https://developers.swell.is/backend-api/orders/retrieve-an-order) |
| [Get Product](actions/get-product.md) | `GET /products/:id` | [docs](https://developers.swell.is/backend-api/products/retrieve-a-product) |
| [Get Promotion](actions/get-promotion.md) | `GET /promotions/:id` | [docs](https://developers.swell.is/backend-api/promotions/retrieve-a-promotion) |
| [Get Variant](actions/get-variant.md) | `GET /products\:variants/:id` | [docs](https://developers.swell.is/backend-api/variants/retrieve-a-variant) |
| [List Accounts](actions/list-accounts.md) | `GET /accounts` | [docs](https://developers.swell.is/backend-api/accounts/list-all-accounts) |
| [List Carts](actions/list-carts.md) | `GET /carts` | [docs](https://developers.swell.is/backend-api/carts/list-all-carts) |
| [List Categories](actions/list-categories.md) | `GET /categories` | [docs](https://developers.swell.is/backend-api/categories/list-all-categories) |
| [List Coupons](actions/list-coupons.md) | `GET /coupons` | [docs](https://developers.swell.is/backend-api/coupons/list-all-coupons) |
| [List Orders](actions/list-orders.md) | `GET /orders` | [docs](https://developers.swell.is/backend-api/orders/list-all-orders) |
| [List Products](actions/list-products.md) | `GET /products` | [docs](https://developers.swell.is/backend-api/products/list-all-products) |
| [List Promotions](actions/list-promotions.md) | `GET /promotions` | [docs](https://developers.swell.is/backend-api/promotions/list-all-promotions) |
| [List Variants](actions/list-variants.md) | `GET /products\:variants` | [docs](https://developers.swell.is/backend-api/variants/list-all-variants) |
| [Update Account](actions/update-account.md) | `PUT /accounts/:id` | [docs](https://developers.swell.is/backend-api/accounts/update-an-account) |
| [Update Cart](actions/update-cart.md) | `PUT /carts/:id` | [docs](https://developers.swell.is/backend-api/carts/update-a-cart) |
| [Update Category](actions/update-category.md) | `PUT /categories/:id` | [docs](https://developers.swell.is/backend-api/categories/update-a-category) |
| [Update Coupon](actions/update-coupon.md) | `PUT /coupons/:id` | [docs](https://developers.swell.is/backend-api/coupons/update-a-coupon) |
| [Update Order](actions/update-order.md) | `PUT /orders/:id` | [docs](https://developers.swell.is/backend-api/orders/update-an-order) |
| [Update Product](actions/update-product.md) | `PUT /products/:id` | [docs](https://developers.swell.is/backend-api/products/update-a-product) |
| [Update Promotion](actions/update-promotion.md) | `PUT /promotions/:id` | [docs](https://developers.swell.is/backend-api/promotions/update-a-promotion) |
| [Update Variant](actions/update-variant.md) | `PUT /products\:variants/:id` | [docs](https://developers.swell.is/backend-api/variants/update-a-variant) |
