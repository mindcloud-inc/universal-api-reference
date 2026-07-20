# Goody: Native API Reference

A consolidated summary of Goody's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://developer.ongoody.com/commerce-api/overview
- **OpenAPI specification:** https://assets.ongoody.com/static/web/goody-api-openapi.json
- **API base URL:** `https://api.ongoody.com`

## Authentication

### Commerce API Key

Authenticate to the Goody Commerce API using a bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developer.ongoody.com/commerce-api/authentication)

## Pagination

Use `per_page` in the query string to set the page size (default 20; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Calculate Order Batch Price](actions/calculate-order-batch-price.md) | `POST /v1/order_batches/price` | [docs](https://developer.ongoody.com/api-reference/order-batches/calculate-the-price-for-an-order-batch) |
| [Cancel Order](actions/cancel-order.md) | `POST /v1/orders/:id/cancel` | [docs](https://developer.ongoody.com/api-reference/orders/cancel-an-order) |
| [Create Commerce User Payment Method](actions/create-commerce-user-payment-method.md) | `POST /v1/commerce_user_payment_methods` | [docs](https://developer.ongoody.com/api-reference/commerce-user-payment-methods/create-a-commerce-user-payment-method) |
| [Create Order Batch](actions/create-order-batch.md) | `POST /v1/order_batches` | [docs](https://developer.ongoody.com/api-reference/order-batches/create-an-order-batch) |
| [Create Webhook](actions/create-webhook.md) | `POST /v1/webhooks` | [docs](https://developer.ongoody.com/commerce-api/webhooks) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /v1/webhooks/:id` | [docs](https://developer.ongoody.com/commerce-api/webhooks) |
| [Get Current User](actions/get-current-user.md) | `GET /v1/me` | [docs](https://developer.ongoody.com/api-reference/retrieve-current-user) |
| [Get Order](actions/get-order.md) | `GET /v1/orders/:id` | [docs](https://developer.ongoody.com/api-reference/orders/retrieve-an-order) |
| [Get Order Batch](actions/get-order-batch.md) | `GET /v1/order_batches/:id` | [docs](https://developer.ongoody.com/api-reference/order-batches/retrieve-an-order-batch) |
| [Get Product](actions/get-product.md) | `GET /v1/products/:id` | [docs](https://developer.ongoody.com/api-reference/products/retrieve-a-product) |
| [List Cards](actions/list-cards.md) | `GET /v1/cards` | [docs](https://developer.ongoody.com/api-reference/cards/list-all-active-cards) |
| [List Order Activities](actions/list-order-activities.md) | `GET /v1/order_activities` | [docs](https://developer.ongoody.com/api-reference/order-activities/list-all-order-activities) |
| [List Order Batch Orders](actions/list-order-batch-orders.md) | `GET /v1/order_batches/:id/orders` | [docs](https://developer.ongoody.com/api-reference/order-batches/retrieve-orders-for-an-order-batch) |
| [List Order Batch Recipients](actions/list-order-batch-recipients.md) | `GET /v1/order_batches/:id/recipients` | [docs](https://developer.ongoody.com/api-reference/order-batches/retrieve-recipients-for-an-order-batch) |
| [List Order Batches](actions/list-order-batches.md) | `GET /v1/order_batches` | [docs](https://developer.ongoody.com/api-reference/order-batches/list-all-order-batches) |
| [List Orders](actions/list-orders.md) | `GET /v1/orders` | [docs](https://developer.ongoody.com/api-reference/orders/list-all-orders) |
| [List Payment Methods](actions/list-payment-methods.md) | `GET /v1/payment_methods` | [docs](https://developer.ongoody.com/api-reference/payment-methods/list-all-payment-methods) |
| [List Products](actions/list-products.md) | `GET /v1/products` | [docs](https://developer.ongoody.com/api-reference/products/list-all-active-products) |
| [List Workspaces](actions/list-workspaces.md) | `GET /v1/workspaces` | [docs](https://developer.ongoody.com/api-reference/workspaces/list-all-workspaces) |
| [Update Order Expiration](actions/update-order-expiration.md) | `POST /v1/orders/:id/update_expiration` | [docs](https://developer.ongoody.com/api-reference/orders/update-expiration-for-an-order) |
