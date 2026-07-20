# Fourthwall: Native API Reference

A consolidated summary of Fourthwall's API configuration and 21 documented operations, with links to official documentation.

- **Official docs:** https://docs.fourthwall.com/guides/overview
- **OpenAPI specification:** https://docs.fourthwall.com/openapi/platform.json
- **API base URL:** `https://api.fourthwall.com`

## Authentication

### OAuth2

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://my-shop.fourthwall.com/admin/platform-apps/a.d097a8ec-fd09-449d-98da-edbcd5fa7ff9/connect to approve access.
2. Exchange the returned authorization code with a POST request to https://api.fourthwall.com/open-api/v1.0/platform/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `shop_read offer_read offer_write order_read order_write fulfillment_write promotions_read promotions_write webhook_read webhook_write`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://api.fourthwall.com/open-api/v1.0/platform/token.

[Official authentication documentation](https://docs.fourthwall.com/docs/oauth-apps)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

The total page count is read from `totalPages`. The current page number is read from `page`.

## Pagination

Use `size` in the query string to set the page size (default 20). Use `page` in the query string to choose the page; numbering starts at 0.

## Endpoints (21 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Promotion](actions/create-promotion.md) | `POST /open-api/v1.0/promotions` | [docs](https://docs.fourthwall.com/api-reference/platform/promotions/create-promotion) |
| [Create Webhook](actions/create-webhook.md) | `POST /open-api/v1.0/webhooks` | [docs](https://docs.fourthwall.com/api-reference/platform/webhooks/create-webhook) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /open-api/v1.0/webhooks/:webhookConfigurationId` | [docs](https://docs.fourthwall.com/api-reference/platform/webhooks/delete-webhook) |
| [Get Current Shop](actions/get-current-shop.md) | `GET /open-api/v1.0/shops/current` | [docs](https://docs.fourthwall.com/api-reference/platform/shop/get-current-shop) |
| [Get External Order](actions/get-external-order.md) | `GET /open-api/v1.0/external-orders/:externalSource/:externalOrderId` | [docs](https://docs.fourthwall.com/api-reference/platform/external-orders/get-external-order) |
| [Get Order](actions/get-order.md) | `GET /open-api/v1.0/order/:orderId` | [docs](https://docs.fourthwall.com/api-reference/platform/orders/get-order) |
| [Get Order By Friendly ID](actions/get-order-by-friendly-id.md) | `GET /open-api/v1.0/order/by-friendly-id/:friendlyId` | [docs](https://docs.fourthwall.com/api-reference/platform/orders/get-order-by-friendly-id) |
| [Get Product](actions/get-product.md) | `GET /open-api/v1.0/products/:productId` | [docs](https://docs.fourthwall.com/api-reference/platform/products/get-product) |
| [Get Product Inventory](actions/get-product-inventory.md) | `GET /open-api/v1.0/products/:productId/inventory` | [docs](https://docs.fourthwall.com/api-reference/platform/products/get-product-inventory) |
| [Get Promotion](actions/get-promotion.md) | `GET /open-api/v1.0/promotions/:promotionId` | [docs](https://docs.fourthwall.com/api-reference/platform/promotions/get-promotion) |
| [Get Shop Contact Info](actions/get-shop-contact-info.md) | `GET /open-api/v1.0/shops/current/contact-info` | [docs](https://docs.fourthwall.com/api-reference/platform/shop/get-shop-contact-info) |
| [List Collections](actions/list-collections.md) | `GET /open-api/v1.0/collections` | [docs](https://docs.fourthwall.com/api-reference/platform/collections/list-collections) |
| [List External Orders](actions/list-external-orders.md) | `GET /open-api/v1.0/external-orders` | [docs](https://docs.fourthwall.com/api-reference/platform/external-orders/list-external-orders) |
| [List Orders](actions/list-orders.md) | `GET /open-api/v1.0/order` | [docs](https://docs.fourthwall.com/api-reference/platform/orders/list-orders) |
| [List Products](actions/list-products.md) | `GET /open-api/v1.0/products` | [docs](https://docs.fourthwall.com/api-reference/platform/products/list-products) |
| [List Promotions](actions/list-promotions.md) | `GET /open-api/v1.0/promotions` | [docs](https://docs.fourthwall.com/api-reference/platform/promotions/list-promotions) |
| [List Webhook Events](actions/list-webhook-events.md) | `GET /open-api/v1.0/webhook-events` | [docs](https://docs.fourthwall.com/api-reference/platform/webhooks/list-webhook-events) |
| [List Webhooks](actions/list-webhooks.md) | `GET /open-api/v1.0/webhooks` | [docs](https://docs.fourthwall.com/api-reference/platform/webhooks/list-webhooks) |
| [Update Product Availability](actions/update-product-availability.md) | `PUT /open-api/v1.0/products/:productId/availability` | [docs](https://docs.fourthwall.com/api-reference/platform/products/update-product-availability) |
| [Update Webhook](actions/update-webhook.md) | `PUT /open-api/v1.0/webhooks/:webhookConfigurationId` | [docs](https://docs.fourthwall.com/api-reference/platform/webhooks/update-webhook) |
| [Validate External Order](actions/validate-external-order.md) | `POST /open-api/v1.0/external-orders/validate` | [docs](https://docs.fourthwall.com/api-reference/platform/external-orders/validate-external-order) |
