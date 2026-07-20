# Ecwid: Native API Reference

A consolidated summary of Ecwid's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.ecwid.com/api-reference
- **API base URL:** `https://app.ecwid.com/api/v3`

## Authentication

### Public + Secret Token

Connect with your Ecwid store ID, public token, and secret token.

### Credentials

- **API Key:** `apiKey` · required
- **Store ID:** `storeId` · required · Your Ecwid store ID.
- **Public Token:** `publicToken` · required · Your Ecwid public token for safe storefront reads.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.ecwid.com/api-reference/rest-api/app-settings)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `items`.

## Pagination

Use `limit` in the query string to set the page size (default 100; maximum 100). Use `offset` in the query string as the record offset.

## Sorting

Set the sort field with `sortBy` in the query string. Only one sort field is accepted.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Adjust Product Stock](actions/adjust-product-stock.md) | `PUT /:storeId/products/:productId/inventory` | [docs](https://docs.ecwid.com/api-reference/rest-api/products/adjust-product-stock) |
| [Get Abandoned Cart](actions/get-abandoned-cart.md) | `GET /:storeId/carts/:cartId` | [docs](https://docs.ecwid.com/api-reference/rest-api/orders/abandonned-carts/get-abandoned-cart) |
| [Get Category](actions/get-category.md) | `GET /:storeId/categories/:categoryId` | [docs](https://docs.ecwid.com/api-reference/rest-api/categories/get-category) |
| [Get Customer](actions/get-customer.md) | `GET /:storeId/customers/:customerId` | [docs](https://docs.ecwid.com/api-reference/rest-api/customers/get-customer) |
| [Get Customer Group](actions/get-customer-group.md) | `GET /:storeId/customer_groups/:groupId` | [docs](https://docs.ecwid.com/api-reference/rest-api/customers/customer-groups/get-customer-group) |
| [Get Last Order](actions/get-last-order.md) | `GET /:storeId/orders/last` | [docs](https://docs.ecwid.com/api-reference/rest-api/orders/get-last-order) |
| [Get Order](actions/get-order.md) | `GET /:storeId/orders/:orderId` | [docs](https://docs.ecwid.com/api-reference/rest-api/orders/get-order) |
| [Get Order Status](actions/get-order-status.md) | `GET /:storeId/profile/order_status/:statusId` | [docs](https://docs.ecwid.com/api-reference/rest-api/orders/order-statuses/get-order-status) |
| [Get Product](actions/get-product.md) | `GET /:storeId/products/:productId` | [docs](https://docs.ecwid.com/api-reference/rest-api/products/get-product) |
| [Get Recently Used Product Swatches](actions/get-recently-used-product-swatches.md) | `GET /:storeId/swatches` | [docs](https://docs.ecwid.com/api-reference/rest-api/products/get-recently-used-product-swatches) |
| [Get Repeat Order URL](actions/get-repeat-order-url.md) | `GET /:storeId/orders/:orderId/repeatURL` | [docs](https://docs.ecwid.com/api-reference/rest-api/orders/get-repeat-order-url) |
| [Get Store Profile](actions/get-store-profile.md) | `GET /:storeId/profile` | [docs](https://docs.ecwid.com/api-reference/rest-api/store-profile/get-store-profile) |
| [Search Abandoned Carts](actions/search-abandoned-carts.md) | `GET /:storeId/carts` | [docs](https://docs.ecwid.com/api-reference/rest-api/orders/abandonned-carts/search-abandoned-carts) |
| [Search Categories](actions/search-categories.md) | `GET /:storeId/categories` | [docs](https://docs.ecwid.com/api-reference/rest-api/categories/search-categories) |
| [Search Categories by Path](actions/search-categories-by-path.md) | `GET /:storeId/categoriesByPath` | [docs](https://docs.ecwid.com/api-reference/rest-api/categories/search-categories-by-path) |
| [Search Customer Groups](actions/search-customer-groups.md) | `GET /:storeId/customer_groups` | [docs](https://docs.ecwid.com/api-reference/rest-api/customers/customer-groups/search-customer-groups) |
| [Search Customers](actions/search-customers.md) | `GET /:storeId/customers` | [docs](https://docs.ecwid.com/api-reference/rest-api/customers/search-customers) |
| [Search Discount Coupons](actions/search-discount-coupons.md) | `GET /:storeId/discount_coupons` | [docs](https://docs.ecwid.com/api-reference/rest-api/discounts/discount-coupons/search-discount-coupons) |
| [Search Order Extra Fields](actions/search-order-extra-fields.md) | `GET /:storeId/orders/:orderId/extraFields` | [docs](https://docs.ecwid.com/api-reference/rest-api/orders/order-extra-fields/search-order-extra-fields) |
| [Search Order Statuses](actions/search-order-statuses.md) | `GET /:storeId/profile/order_statuses` | [docs](https://docs.ecwid.com/api-reference/rest-api/orders/order-statuses/search-order-statuses) |
| [Search Orders](actions/search-orders.md) | `GET /:storeId/orders` | [docs](https://docs.ecwid.com/api-reference/rest-api/orders/search-orders) |
| [Search Product Brands](actions/search-product-brands.md) | `GET /:storeId/brands` | [docs](https://docs.ecwid.com/api-reference/rest-api/products/search-product-brands) |
| [Search Products](actions/search-products.md) | `GET /:storeId/products` | [docs](https://docs.ecwid.com/api-reference/rest-api/products/search-products) |
| [Search Shipping Options](actions/search-shipping-options.md) | `GET /:storeId/profile/shippingOptions` | [docs](https://docs.ecwid.com/api-reference/rest-api/shipping-options/search-shipping-options) |
