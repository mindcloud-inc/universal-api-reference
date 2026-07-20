# Shopkit: Native API Reference

A consolidated summary of Shopkit's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://shopk.it/developers/api
- **API base URL:** `https://api.shopk.it/v1`

## Authentication

### API Key

Authenticate Shopkit with an API key sent in the X-API-KEY header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://shopk.it/developers/api#header-authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `limit` in the query string to set the page size (default 25; accepted range 1–50). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Brand](actions/create-brand.md) | `POST /brand` | [docs](https://shopk.it/developers/api#brands-post-brand-post) |
| [Create Category](actions/create-category.md) | `POST /category` | [docs](https://shopk.it/developers/api#categories-post-category-post) |
| [Create Client](actions/create-client.md) | `POST /client` | [docs](https://shopk.it/developers/api#client-post-client-post) |
| [Create Coupon](actions/create-coupon.md) | `POST /coupon` | [docs](https://shopk.it/developers/api#coupons-post-coupon-post) |
| [Create Product](actions/create-product.md) | `POST /product` | [docs](https://shopk.it/developers/api#products-post-product-post) |
| [Create Product Option Group](actions/create-product-option-group.md) | `POST /product/:id/option_group` | [docs](https://shopk.it/developers/api#product-option-groups-post-product-option-group-post) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhook` | [docs](https://shopk.it/developers/api#webhooks-post-webhook-post) |
| [Delete Brand](actions/delete-brand.md) | `DELETE /brand/:id` | [docs](https://shopk.it/developers/api#brands-delete-brand-delete) |
| [Delete Category](actions/delete-category.md) | `DELETE /category/:id` | [docs](https://shopk.it/developers/api#categories-delete-category-delete) |
| [Delete Client](actions/delete-client.md) | `DELETE /client/:id` | [docs](https://shopk.it/developers/api#client-delete-client-delete) |
| [Delete Coupon](actions/delete-coupon.md) | `DELETE /coupon/:id` | [docs](https://shopk.it/developers/api#coupons-delete-coupon-delete) |
| [Delete Order](actions/delete-order.md) | `DELETE /order/:id` | [docs](https://shopk.it/developers/api#orders-delete-order-delete) |
| [Delete Product](actions/delete-product.md) | `DELETE /product/:id` | [docs](https://shopk.it/developers/api#products-delete-product-delete) |
| [Delete Product Option](actions/delete-product-option.md) | `DELETE /product/:id/option/:id_option` | [docs](https://shopk.it/developers/api#product-options-delete-product-option-delete) |
| [Delete Product Option Group](actions/delete-product-option-group.md) | `DELETE /product/:id/option_group/:id_option_group` | [docs](https://shopk.it/developers/api#product-option-groups-delete-product-option-group-delete) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /webhook/:id` | [docs](https://shopk.it/developers/api#webhooks-delete-webhook-delete) |
| [Get Stats](actions/get-stats.md) | `GET /stats` | [docs](https://shopk.it/developers/api#stats-get-stats-get) |
| [Get Store](actions/get-store.md) | `GET /store` | [docs](https://shopk.it/developers/api#store-get-store-get) |
| [List Brands](actions/list-brands.md) | `GET /brand` | [docs](https://shopk.it/developers/api#brands-get-brand-get) |
| [List Categories](actions/list-categories.md) | `GET /category` | [docs](https://shopk.it/developers/api#categories-get-category-get) |
| [List Clients](actions/list-clients.md) | `GET /client` | [docs](https://shopk.it/developers/api#client-get-client-get) |
| [List Coupons](actions/list-coupons.md) | `GET /coupon` | [docs](https://shopk.it/developers/api#coupons-get-coupon-get) |
| [List Media](actions/list-media.md) | `GET /media` | [docs](https://shopk.it/developers/api#media-get-media-get) |
| [List Orders](actions/list-orders.md) | `GET /order` | [docs](https://shopk.it/developers/api#orders-get-order-get) |
| [List Product Option Groups](actions/list-product-option-groups.md) | `GET /product/:id/option_group` | [docs](https://shopk.it/developers/api#product-option-groups-get-product-option-group-get) |
| [List Product Options](actions/list-product-options.md) | `GET /product/:id/option` | [docs](https://shopk.it/developers/api#product-options-get-product-option-get) |
| [List Products](actions/list-products.md) | `GET /product` | [docs](https://shopk.it/developers/api#products-get-product-get) |
| [List Shipments](actions/list-shipments.md) | `GET /shipment` | [docs](https://shopk.it/developers/api#shipment-get-shipment-get) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhook` | [docs](https://shopk.it/developers/api#webhooks-get-webhook-get) |
| [Search Products](actions/search-products.md) | `GET /product/search` | [docs](https://shopk.it/developers/api#products-get-product-search-get) |
| [Update Brand](actions/update-brand.md) | `PUT /brand/:id` | [docs](https://shopk.it/developers/api#brands-put-brand-put) |
| [Update Category](actions/update-category.md) | `PUT /category/:id` | [docs](https://shopk.it/developers/api#categories-put-category-put) |
| [Update Client](actions/update-client.md) | `PUT /client/:id` | [docs](https://shopk.it/developers/api#client-put-client-put) |
| [Update Coupon](actions/update-coupon.md) | `PUT /coupon` | [docs](https://shopk.it/developers/api#coupons-put-coupon-put) |
| [Update Order](actions/update-order.md) | `PUT /order/:id` | [docs](https://shopk.it/developers/api#orders-put-order-put) |
| [Update Orders in Bulk](actions/update-orders-in-bulk.md) | `PUT /order/bulk` | [docs](https://shopk.it/developers/api#orders-put-order-bulk-put) |
| [Update Product](actions/update-product.md) | `PUT /product/:id` | [docs](https://shopk.it/developers/api#products-put-product-put) |
| [Update Product Option](actions/update-product-option.md) | `PUT /product/:id/option/:id_option` | [docs](https://shopk.it/developers/api#product-options-put-product-option-put) |
| [Update Product Option Group](actions/update-product-option-group.md) | `PUT /product/:id/option_group/:id_option_group` | [docs](https://shopk.it/developers/api#product-option-groups-put-product-option-group-put) |
| [Upload Media](actions/upload-media.md) | `POST /media` | [docs](https://shopk.it/developers/api#media-post-media-post) |
