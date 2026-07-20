# SquareSpace: Native API Reference

A consolidated summary of SquareSpace's API configuration and 27 documented operations, with links to official documentation.

- **Official docs:** https://developers.squarespace.com/commerce-apis/overview
- **API base URL:** `https://api.squarespace.com`

## Authentication

### API Key

Use a Squarespace Commerce API key. The key is sent as a Bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.squarespace.com/commerce-apis/authentication-and-permissions)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

The next-page cursor is read from `pagination.nextPageCursor`.

## Pagination

Use `cursor` in the query string as the pagination cursor.

## Filtering

Send filters in the query string. Supported operators: `eq`.

## Sorting

Set the sort field with `sortField` in the query string. Set the direction separately with `sortDirection`. Use `ASC` for ascending order and `DESC` for descending order. Only one sort field is accepted.

## Retry behavior

Wait 5000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (27 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Adjust Stock Quantities](actions/adjust-stock-quantities.md) | `POST /1.0/commerce/inventory/adjustments` | [docs](https://developers.squarespace.com/commerce-apis/inventory#adjust-stock-quantities) |
| [Assign Product Image to Variant](actions/assign-product-image-to-variant.md) | `POST /v2/commerce/products/:productId/variants/:variantId/image` | [docs](https://developers.squarespace.com/commerce-apis/products#associate-variant-image) |
| [Create Order](actions/create-order.md) | `POST /1.0/commerce/orders` | [docs](https://developers.squarespace.com/commerce-apis/orders#create-order) |
| [Create Product](actions/create-product.md) | `POST /v2/commerce/products` | [docs](https://developers.squarespace.com/commerce-apis/products#create-product) |
| [Create Product Variant](actions/create-product-variant.md) | `POST /v2/commerce/products/:id/variants` | [docs](https://developers.squarespace.com/commerce-apis/products#create-product-variant) |
| [Delete Product](actions/delete-product.md) | `DELETE /v2/commerce/products/:id` | [docs](https://developers.squarespace.com/commerce-apis/products#delete-specified-product) |
| [Delete Product Image](actions/delete-product-image.md) | `DELETE /v2/commerce/products/:productId/images/:imageId` | [docs](https://developers.squarespace.com/commerce-apis/products#delete-one-product-image) |
| [Delete Product Variant](actions/delete-product-variant.md) | `DELETE /v2/commerce/products/:productId/variants/:variantId` | [docs](https://developers.squarespace.com/commerce-apis/products#delete-one-product-variant) |
| [Fulfill Order](actions/fulfill-order.md) | `POST /1.0/commerce/orders/:id/fulfillments` | [docs](https://developers.squarespace.com/commerce-apis/orders#fulfill-order) |
| [Get Image Processing Status](actions/get-image-processing-status.md) | `GET /v2/commerce/products/:productId/images/:imageId/status` | [docs](https://developers.squarespace.com/commerce-apis/products#get-image-processing-status) |
| [Get Inventory](actions/get-inventory.md) | `GET /1.0/commerce/inventory/:ids` | [docs](https://developers.squarespace.com/commerce-apis/inventory#get-inventory) |
| [Get Order](actions/get-order.md) | `GET /1.0/commerce/orders/:id` | [docs](https://developers.squarespace.com/commerce-apis/orders#get-order) |
| [Get Products](actions/get-products.md) | `GET /v2/commerce/products/:ids` | [docs](https://developers.squarespace.com/commerce-apis/products#get-products) |
| [Get Profiles](actions/get-profiles.md) | `GET /1.0/profiles/:ids` | [docs](https://developers.squarespace.com/commerce-apis/profiles#get-profiles) |
| [Get Transactions](actions/get-transactions.md) | `GET /1.0/commerce/transactions/:ids` | [docs](https://developers.squarespace.com/commerce-apis/transactions#get-transactions) |
| [List Inventory](actions/list-inventory.md) | `GET /1.0/commerce/inventory` | [docs](https://developers.squarespace.com/commerce-apis/inventory#list-inventory) |
| [List Orders](actions/list-orders.md) | `GET /1.0/commerce/orders` | [docs](https://developers.squarespace.com/commerce-apis/orders#list-orders) |
| [List Products](actions/list-products.md) | `GET /v2/commerce/products` | [docs](https://developers.squarespace.com/commerce-apis/products#list-products) |
| [List Profiles](actions/list-profiles.md) | `GET /1.0/profiles` | [docs](https://developers.squarespace.com/commerce-apis/profiles#list-profiles) |
| [List Store Pages](actions/list-store-pages.md) | `GET /1.0/commerce/store_pages` | [docs](https://developers.squarespace.com/commerce-apis/websites#list-store-pages) |
| [List Transactions](actions/list-transactions.md) | `GET /1.0/commerce/transactions` | [docs](https://developers.squarespace.com/commerce-apis/transactions#list-transactions) |
| [Reorder Product Image](actions/reorder-product-image.md) | `POST /v2/commerce/products/:productId/images/:imageId/order` | [docs](https://developers.squarespace.com/commerce-apis/products#update-product-image-order) |
| [Retrieve Basic Site Information](actions/retrieve-basic-site-information.md) | `GET /1.0/authorization/website` | [docs](https://developers.squarespace.com/commerce-apis/websites#retrieves-basic-details-about-the-website-that-owns-the-provided-api-key-or-oauth-token) |
| [Update Product](actions/update-product.md) | `POST /v2/commerce/products/:id` | [docs](https://developers.squarespace.com/commerce-apis/products#update-product) |
| [Update Product Image](actions/update-product-image.md) | `POST /v2/commerce/products/:productId/images/:imageId` | [docs](https://developers.squarespace.com/commerce-apis/products#update-product-image) |
| [Update Product Variant](actions/update-product-variant.md) | `POST /v2/commerce/products/:productId/variants/:variantId` | [docs](https://developers.squarespace.com/commerce-apis/products#update-product-variant) |
| [Upload Product Image](actions/upload-product-image.md) | `POST /v2/commerce/products/:id/images` | [docs](https://developers.squarespace.com/commerce-apis/products#upload-product-image) |
