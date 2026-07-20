# YouCan: Native API Reference

A consolidated summary of YouCan's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://developer.youcan.shop/store-admin/introduction/oauth
- **API base URL:** `https://api.youcan.shop`

## Authentication

### YouCan OAuth2

Set the final App URL and production Allowed redirect URLs in the YouCan partner dashboard before install testing.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://seller-area.youcan.shop/admin/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://api.youcan.shop/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `*`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://api.youcan.shop/oauth/token.

[Official authentication documentation](https://developer.youcan.shop/store-admin/introduction/oauth)

## Pagination

Use `limit` in the query string to set the page size. Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string.

## Sorting

Set the sort field with `sort_field` in the query string. Set the direction separately with `sort_order`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Close Order](actions/close-order.md) | `PUT /orders/{id}/close` | [docs](https://developer.youcan.shop/store-admin/orders/close) |
| [Create Coupon](actions/create-coupon.md) | `POST /coupons` | [docs](https://developer.youcan.shop/store-admin/coupons/create) |
| [Create Customer](actions/create-customer.md) | `POST /customers` | [docs](https://developer.youcan.shop/store-admin/customers/create) |
| [Create Customer Address](actions/create-customer-address.md) | `POST /customers/{id}/addresses` | [docs](https://developer.youcan.shop/store-admin/customers/addresses/create) |
| [Create Order](actions/create-order.md) | `POST /orders` | [docs](https://developer.youcan.shop/store-admin/orders/create) |
| [Create Page](actions/create-page.md) | `POST /pages` | [docs](https://developer.youcan.shop/store-admin/pages/create) |
| [Create Product](actions/create-product.md) | `POST /products` | [docs](https://developer.youcan.shop/store-admin/products/create) |
| [Delete Coupon](actions/delete-coupon.md) | `DELETE /coupons/{id}` | [docs](https://developer.youcan.shop/store-admin/coupons/delete) |
| [Delete Customer](actions/delete-customer.md) | `DELETE /customers/{id}` | [docs](https://developer.youcan.shop/store-admin/customers/delete) |
| [Delete Page](actions/delete-page.md) | `DELETE /pages/{id}` | [docs](https://developer.youcan.shop/store-admin/pages/delete) |
| [Delete Product](actions/delete-product.md) | `DELETE /products/{id}` | [docs](https://developer.youcan.shop/store-admin/products/delete) |
| [Fulfill Order](actions/fulfill-order.md) | `PUT /orders/{id}/fulfill` | [docs](https://developer.youcan.shop/store-admin/orders/fulfill) |
| [Get Coupon](actions/get-coupon.md) | `GET /coupons/{id}` | [docs](https://developer.youcan.shop/store-admin/coupons/get) |
| [Get Customer](actions/get-customer.md) | `GET /customers/{id}` | [docs](https://developer.youcan.shop/store-admin/customers/get) |
| [Get Order](actions/get-order.md) | `GET /orders/{id}` | [docs](https://developer.youcan.shop/store-admin/orders/get) |
| [Get Page](actions/get-page.md) | `GET /pages/{id}` | [docs](https://developer.youcan.shop/store-admin/pages/get) |
| [Get Product](actions/get-product.md) | `GET /products/{id}` | [docs](https://developer.youcan.shop/store-admin/products/get) |
| [List Coupons](actions/list-coupons.md) | `GET /coupons` | [docs](https://developer.youcan.shop/store-admin/coupons/listing) |
| [List Customers](actions/list-customers.md) | `GET /customers` | [docs](https://developer.youcan.shop/store-admin/customers/listing) |
| [List Orders](actions/list-orders.md) | `GET /orders` | [docs](https://developer.youcan.shop/store-admin/orders/listing) |
| [List Pages](actions/list-pages.md) | `GET /pages` | [docs](https://developer.youcan.shop/store-admin/pages/listing) |
| [List Products](actions/list-products.md) | `GET /products` | [docs](https://developer.youcan.shop/store-admin/products/listing) |
| [Mark Order As Paid](actions/mark-order-as-paid.md) | `PUT /orders/{id}/pay` | [docs](https://developer.youcan.shop/store-admin/orders/pay) |
| [Order Statuses](actions/order-statuses.md) | `GET /orders/settings` | [docs](https://developer.youcan.shop/store-admin/orders/statuses) |
| [Update Coupon](actions/update-coupon.md) | `PUT /coupons/{id}` | [docs](https://developer.youcan.shop/store-admin/coupons/update) |
| [Update Customer](actions/update-customer.md) | `PUT /customers/{id}` | [docs](https://developer.youcan.shop/store-admin/customers/update) |
| [Update Customer Address](actions/update-customer-address.md) | `PUT /customers/{id}/addresses/{addressId}` | [docs](https://developer.youcan.shop/store-admin/customers/addresses/update) |
| [Update Order Status](actions/update-order-status.md) | `PUT /orders/{id}/status/{context}` | [docs](https://developer.youcan.shop/store-admin/orders/update_status) |
| [Update Page](actions/update-page.md) | `POST /pages/{id}` | [docs](https://developer.youcan.shop/store-admin/pages/update) |
| [Update Product](actions/update-product.md) | `POST /products/update/{id}` | [docs](https://developer.youcan.shop/store-admin/products/update) |
