# SureCart: Native API Reference

A consolidated summary of SureCart's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://developer.surecart.com/api-reference/introduction
- **API base URL:** `https://api.surecart.com`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developer.surecart.com/api-reference/authentication)

## Pagination

Use `limit` in the query string to set the page size (default 20; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort` in the query string. Only one sort field is accepted.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel/Pause Subscription](actions/cancel-pause-subscription.md) | `PATCH v1/subscriptions/:id/cancel` | [docs](https://developer.surecart.com/api-reference/subscriptions/cancelpause) |
| [Create Checkout](actions/create-checkout.md) | `POST v1/checkouts` | [docs](https://developer.surecart.com/api-reference/checkouts/create) |
| [Create Customer](actions/create-customer.md) | `POST v1/customers` | [docs](https://developer.surecart.com/api-reference/customers/create) |
| [Create Price](actions/create-price.md) | `POST v1/prices` | [docs](https://developer.surecart.com/api-reference/prices/create) |
| [Create Product](actions/create-product.md) | `POST v1/products` | [docs](https://developer.surecart.com/api-reference/products/create) |
| [Create Refund](actions/create-refund.md) | `POST v1/refunds` | [docs](https://developer.surecart.com/api-reference/refunds/create) |
| [Create Subscription](actions/create-subscription.md) | `POST v1/subscriptions` | [docs](https://developer.surecart.com/api-reference/subscriptions/create) |
| [Create Webhook Endpoint](actions/create-webhook-endpoint.md) | `POST v1/webhook_endpoints` | [docs](https://developer.surecart.com/api-reference/webhook-endpoints/create) |
| [Delete Customer](actions/delete-customer.md) | `DELETE v1/customers/:id` | [docs](https://developer.surecart.com/api-reference/customers/delete) |
| [Delete Price](actions/delete-price.md) | `DELETE v1/prices/:id` | [docs](https://developer.surecart.com/api-reference/prices/delete) |
| [Delete Product](actions/delete-product.md) | `DELETE v1/products/:id` | [docs](https://developer.surecart.com/api-reference/products/delete) |
| [List Checkouts](actions/list-checkouts.md) | `GET v1/checkouts` | [docs](https://developer.surecart.com/api-reference/checkouts/list) |
| [List Customers](actions/list-customers.md) | `GET v1/customers` | [docs](https://developer.surecart.com/api-reference/customers/list) |
| [List Orders](actions/list-orders.md) | `GET v1/orders` | [docs](https://developer.surecart.com/api-reference/orders/list) |
| [List Prices](actions/list-prices.md) | `GET v1/prices` | [docs](https://developer.surecart.com/api-reference/prices/list) |
| [List Products](actions/list-products.md) | `GET v1/products` | [docs](https://developer.surecart.com/api-reference/products/list) |
| [List Purchases](actions/list-purchases.md) | `GET v1/purchases` | [docs](https://developer.surecart.com/api-reference/purchases/list) |
| [List Refunds](actions/list-refunds.md) | `GET v1/refunds` | [docs](https://developer.surecart.com/api-reference/refunds/list) |
| [List Subscriptions](actions/list-subscriptions.md) | `GET v1/subscriptions` | [docs](https://developer.surecart.com/api-reference/subscriptions/list) |
| [List Webhook Endpoints](actions/list-webhook-endpoints.md) | `GET v1/webhook_endpoints` | [docs](https://developer.surecart.com/api-reference/webhook-endpoints/list) |
| [Retrieve Account](actions/retrieve-account.md) | `GET v1/account` | [docs](https://developer.surecart.com/api-reference/accounts/retrieve) |
| [Retrieve Checkout](actions/retrieve-checkout.md) | `GET v1/checkouts/:id` | [docs](https://developer.surecart.com/api-reference/checkouts/retrieve) |
| [Retrieve Customer](actions/retrieve-customer.md) | `GET v1/customers/:id` | [docs](https://developer.surecart.com/api-reference/customers/retrieve) |
| [Retrieve Order](actions/retrieve-order.md) | `GET v1/orders/:id` | [docs](https://developer.surecart.com/api-reference/orders/retrieve) |
| [Retrieve Price](actions/retrieve-price.md) | `GET v1/prices/:id` | [docs](https://developer.surecart.com/api-reference/prices/retrieve) |
| [Retrieve Product](actions/retrieve-product.md) | `GET v1/products/:id` | [docs](https://developer.surecart.com/api-reference/products/retrieve) |
| [Retrieve Purchase](actions/retrieve-purchase.md) | `GET v1/purchases/:id` | [docs](https://developer.surecart.com/api-reference/purchases/retrieve) |
| [Retrieve Refund](actions/retrieve-refund.md) | `GET v1/refunds/:id` | [docs](https://developer.surecart.com/api-reference/refunds/retrieve) |
| [Retrieve Subscription](actions/retrieve-subscription.md) | `GET v1/subscriptions/:id` | [docs](https://developer.surecart.com/api-reference/subscriptions/retrieve) |
| [Retrieve Webhook Endpoint](actions/retrieve-webhook-endpoint.md) | `GET v1/webhook_endpoints/:id` | [docs](https://developer.surecart.com/api-reference/webhook-endpoints/retrieve) |
| [Revoke Purchase](actions/revoke-purchase.md) | `PATCH v1/purchases/:id/revoke` | [docs](https://developer.surecart.com/api-reference/purchases/revoke) |
| [Test Webhook Endpoint](actions/test-webhook-endpoint.md) | `POST v1/webhook_endpoints/:id/test` | [docs](https://developer.surecart.com/api-reference/webhook-endpoints/test) |
| [Update Account](actions/update-account.md) | `PATCH v1/account` | [docs](https://developer.surecart.com/api-reference/accounts/update) |
| [Update Checkout](actions/update-checkout.md) | `PATCH v1/checkouts/:id` | [docs](https://developer.surecart.com/api-reference/checkouts/update) |
| [Update Customer](actions/update-customer.md) | `PATCH v1/customers/:id` | [docs](https://developer.surecart.com/api-reference/customers/update) |
| [Update Price](actions/update-price.md) | `PATCH v1/prices/:id` | [docs](https://developer.surecart.com/api-reference/prices/update) |
| [Update Product](actions/update-product.md) | `PATCH v1/products/:id` | [docs](https://developer.surecart.com/api-reference/products/update) |
| [Update Purchase](actions/update-purchase.md) | `PATCH v1/purchases/:id` | [docs](https://developer.surecart.com/api-reference/purchases/update) |
| [Update Subscription](actions/update-subscription.md) | `PATCH v1/subscriptions/:id` | [docs](https://developer.surecart.com/api-reference/subscriptions/update) |
| [Update Webhook Endpoint](actions/update-webhook-endpoint.md) | `PATCH v1/webhook_endpoints/:id` | [docs](https://developer.surecart.com/api-reference/webhook-endpoints/update) |
