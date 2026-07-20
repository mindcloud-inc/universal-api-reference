# Paddle: Native API Reference

A consolidated summary of Paddle's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://developer.paddle.com/api-reference/overview
- **OpenAPI specification:** https://raw.githubusercontent.com/PaddleHQ/paddle-openapi/refs/heads/main/v1/openapi.yaml
- **API base URL:** `https://api.paddle.com`

## Authentication

### API Key

Paddle Billing API key authentication

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developer.paddle.com/api-reference/about/api-keys)

## Pagination

Use `per_page` in the query string to set the page size (default 50; maximum 200). Use `after` in the query string as the pagination cursor. Follow the complete next-page URL returned by the API.

## Filtering

Send filters in the query string.

## Sorting

Set the sort field with `order_by` in the query string. Use `ASC]` for ascending order and `DESC]` for descending order. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429`. Wait 60000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 1 after each failed attempt.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Subscription](actions/cancel-subscription.md) | `POST subscriptions/{subscription_id}/cancel` | [docs](https://developer.paddle.com/api-reference/subscriptions/cancel-subscription) |
| [Create Customer](actions/create-customer.md) | `POST customers` | [docs](https://developer.paddle.com/api-reference/customers/create-customer) |
| [Create Customer Portal Session](actions/create-customer-portal-session.md) | `POST customers/{customer_id}/portal-sessions` | [docs](https://developer.paddle.com/api-reference/customer-portals/create-customer-portal-session) |
| [Create Discount](actions/create-discount.md) | `POST discounts` | [docs](https://developer.paddle.com/api-reference/discounts/create-discount) |
| [Create Notification Setting](actions/create-notification-setting.md) | `POST notification-settings` | [docs](https://developer.paddle.com/api-reference/notification-settings/create-notification-setting) |
| [Create Price](actions/create-price.md) | `POST prices` | [docs](https://developer.paddle.com/api-reference/prices/create-price) |
| [Create Product](actions/create-product.md) | `POST products` | [docs](https://developer.paddle.com/api-reference/products/create-product) |
| [Create Transaction](actions/create-transaction.md) | `POST transactions` | [docs](https://developer.paddle.com/api-reference/transactions/create-transaction) |
| [Get Customer](actions/get-customer.md) | `GET customers/{customer_id}` | [docs](https://developer.paddle.com/api-reference/customers/get-customer) |
| [Get Discount](actions/get-discount.md) | `GET discounts/{discount_id}` | [docs](https://developer.paddle.com/api-reference/discounts/get-discount) |
| [Get Price](actions/get-price.md) | `GET prices/{price_id}` | [docs](https://developer.paddle.com/api-reference/prices/get-price) |
| [Get Product](actions/get-product.md) | `GET products/{product_id}` | [docs](https://developer.paddle.com/api-reference/products/get-product) |
| [Get Subscription](actions/get-subscription.md) | `GET subscriptions/{subscription_id}` | [docs](https://developer.paddle.com/api-reference/subscriptions/get-subscription) |
| [Get Transaction](actions/get-transaction.md) | `GET transactions/{transaction_id}` | [docs](https://developer.paddle.com/api-reference/transactions/get-transaction) |
| [List Customers](actions/list-customers.md) | `GET customers` | [docs](https://developer.paddle.com/api-reference/customers/list-customers) |
| [List Discounts](actions/list-discounts.md) | `GET discounts` | [docs](https://developer.paddle.com/api-reference/discounts/list-discounts) |
| [List Event Types](actions/list-event-types.md) | `GET event-types` | [docs](https://developer.paddle.com/api-reference/event-types/overview) |
| [List Notification Settings](actions/list-notification-settings.md) | `GET notification-settings` | [docs](https://developer.paddle.com/api-reference/notification-settings/list-notification-settings) |
| [List Notifications](actions/list-notifications.md) | `GET notifications` | [docs](https://developer.paddle.com/api-reference/notifications/list-notifications) |
| [List Prices](actions/list-prices.md) | `GET prices` | [docs](https://developer.paddle.com/api-reference/prices/list-prices) |
| [List Products](actions/list-products.md) | `GET products` | [docs](https://developer.paddle.com/api-reference/products/list-products) |
| [List Subscriptions](actions/list-subscriptions.md) | `GET subscriptions` | [docs](https://developer.paddle.com/api-reference/subscriptions/list-subscriptions) |
| [List Transactions](actions/list-transactions.md) | `GET transactions` | [docs](https://developer.paddle.com/api-reference/transactions/list-transactions) |
| [Preview Prices](actions/preview-prices.md) | `POST pricing-preview` | [docs](https://developer.paddle.com/api-reference/pricing-preview/preview-prices) |
| [Update Customer](actions/update-customer.md) | `PATCH customers/{customer_id}` | [docs](https://developer.paddle.com/api-reference/customers/update-customer) |
| [Update Discount](actions/update-discount.md) | `PATCH discounts/{discount_id}` | [docs](https://developer.paddle.com/api-reference/discounts/update-discount) |
| [Update Price](actions/update-price.md) | `PATCH prices/{price_id}` | [docs](https://developer.paddle.com/api-reference/prices/update-price) |
| [Update Product](actions/update-product.md) | `PATCH products/{product_id}` | [docs](https://developer.paddle.com/api-reference/products/update-product) |
| [Update Subscription](actions/update-subscription.md) | `PATCH subscriptions/{subscription_id}` | [docs](https://developer.paddle.com/api-reference/subscriptions/update-subscription) |
| [Update Transaction](actions/update-transaction.md) | `PATCH transactions/{transaction_id}` | [docs](https://developer.paddle.com/api-reference/transactions/update-transaction) |
