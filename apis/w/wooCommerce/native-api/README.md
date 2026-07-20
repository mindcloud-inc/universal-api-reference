# WooCommerce: Native API Reference

A consolidated summary of WooCommerce's API configuration and 26 documented operations, with links to official documentation.

- **Official docs:** https://woocommerce.github.io/woocommerce-rest-api-docs/
- **API base URL:** `{siteUrl}/wp-json/wc/v3`

## Authentication

### Consumer Key + Secret (Basic Auth)

Authenticate with your WooCommerce store URL, consumer key, and consumer secret over HTTPS.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required
- **Site URL:** `siteUrl` · required · Base URL of your WooCommerce store (for example https://example.com).

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://woocommerce.github.io/woocommerce-rest-api-docs/#authentication-over-https)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size (default 10; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `orderby` in the query string. Set the direction separately with `order`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (26 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Coupon](actions/create-coupon.md) | `POST /coupons` | [docs](https://woocommerce.github.io/woocommerce-rest-api-docs/#create-a-coupon) |
| [Create Customer](actions/create-customer.md) | `POST /customers` | [docs](https://woocommerce.github.io/woocommerce-rest-api-docs/#create-a-customer) |
| [Create Order](actions/create-order.md) | `POST /orders` | [docs](https://woocommerce.github.io/woocommerce-rest-api-docs/#create-an-order) |
| [Create Order Note](actions/create-order-note.md) | `POST /orders/:id/notes` | [docs](https://woocommerce.github.io/woocommerce-rest-api-docs/#update-an-order) |
| [Create Product](actions/create-product.md) | `POST /products` | [docs](https://woocommerce.github.io/woocommerce-rest-api-docs/#create-a-product) |
| [Create Product Category](actions/create-product-category.md) | `POST /products/categories` | [docs](https://woocommerce.github.io/woocommerce-rest-api-docs/#create-a-product-category) |
| [Delete Coupon](actions/delete-coupon.md) | `DELETE /coupons/:id` | [docs](https://woocommerce.github.io/woocommerce-rest-api-docs/#delete-a-coupon) |
| [Delete Customer](actions/delete-customer.md) | `DELETE /customers/:id` | [docs](https://woocommerce.github.io/woocommerce-rest-api-docs/#delete-a-customer) |
| [Delete Order](actions/delete-order.md) | `DELETE /orders/:id` | [docs](https://woocommerce.github.io/woocommerce-rest-api-docs/#delete-an-order) |
| [Delete Product](actions/delete-product.md) | `DELETE /products/:id` | [docs](https://woocommerce.github.io/woocommerce-rest-api-docs/#delete-a-product) |
| [Duplicate Product](actions/duplicate-product.md) | `POST /products/:productId/duplicate` | [docs](https://woocommerce.github.io/woocommerce-rest-api-docs/#duplicate-product) |
| [Get Order Note](actions/get-order-note.md) | `GET /orders/:id/notes` | [docs](https://woocommerce.github.io/woocommerce-rest-api-docs/#update-an-order) |
| [List Coupons](actions/list-coupons.md) | `GET /coupons` | [docs](https://woocommerce.github.io/woocommerce-rest-api-docs/#list-all-coupons) |
| [List Customers](actions/list-customers.md) | `GET /customers` | [docs](https://woocommerce.github.io/woocommerce-rest-api-docs/#list-all-customers) |
| [List Orders](actions/list-orders.md) | `GET /orders` | [docs](https://woocommerce.github.io/woocommerce-rest-api-docs/#list-all-orders) |
| [List Product Categories](actions/list-product-categories.md) | `GET /products/categories` | [docs](https://woocommerce.github.io/woocommerce-rest-api-docs/#list-all-product-categories) |
| [List Products](actions/list-products.md) | `GET /products` | [docs](https://woocommerce.github.io/woocommerce-rest-api-docs/#list-all-products) |
| [Retrieve Coupon](actions/retrieve-coupon.md) | `GET /coupons/:id` | [docs](https://woocommerce.github.io/woocommerce-rest-api-docs/#retrieve-a-coupon) |
| [Retrieve Customer](actions/retrieve-customer.md) | `GET /customers/:id` | [docs](https://woocommerce.github.io/woocommerce-rest-api-docs/#retrieve-a-customer) |
| [Retrieve Order](actions/retrieve-order.md) | `GET /orders/:id` | [docs](https://woocommerce.github.io/woocommerce-rest-api-docs/#retrieve-an-order) |
| [Retrieve Product](actions/retrieve-product.md) | `GET /products/:id` | [docs](https://woocommerce.github.io/woocommerce-rest-api-docs/#retrieve-a-product) |
| [Retrieve Product Category](actions/retrieve-product-category.md) | `GET /products/categories/:id` | [docs](https://woocommerce.github.io/woocommerce-rest-api-docs/#retrieve-a-product-category) |
| [Update Coupon](actions/update-coupon.md) | `PUT /coupons/:id` | [docs](https://woocommerce.github.io/woocommerce-rest-api-docs/#update-a-coupon) |
| [Update Customer](actions/update-customer.md) | `PUT /customers/:id` | [docs](https://woocommerce.github.io/woocommerce-rest-api-docs/#update-a-customer) |
| [Update Order](actions/update-order.md) | `PUT /orders/:id` | [docs](https://woocommerce.github.io/woocommerce-rest-api-docs/#update-an-order) |
| [Update Product](actions/update-product.md) | `PUT /products/:id` | [docs](https://woocommerce.github.io/woocommerce-rest-api-docs/#update-a-product) |
