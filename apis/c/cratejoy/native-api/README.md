# Cratejoy: Native API Reference

A consolidated summary of Cratejoy's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.cratejoy.com/reference/introduction-1
- **API base URL:** `https://api.cratejoy.com`

## Authentication

### Basic Auth

Authenticate Cratejoy Merchant API requests with Client ID and Client Secret.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required
- **Client ID:** `clientId` · required · Your Cratejoy Merchant API Client ID.
- **Client Secret:** `clientSecret` · required · Your Cratejoy Merchant API Client Secret.

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://docs.cratejoy.com/reference/authorization)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `results`.

## Pagination

Use `limit` in the query string to set the page size. Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Subscription](actions/cancel-subscription.md) | `PUT /v1/subscriptions/:subscriptionId/cancel/` | [docs](https://docs.cratejoy.com/reference/subscription-methods) |
| [Create Customer Address](actions/create-customer-address.md) | `POST /v1/customers/:customerId/addresses/` | [docs](https://docs.cratejoy.com/reference/methods-customer) |
| [Create Order](actions/create-order.md) | `POST /v1/orders/` | [docs](https://docs.cratejoy.com/reference/order-methods) |
| [Get Customer](actions/get-customer.md) | `GET /v1/customers/:customerId/` | [docs](https://docs.cratejoy.com/reference/methods-customer) |
| [Get Order](actions/get-order.md) | `GET /v1/orders/:orderId/` | [docs](https://docs.cratejoy.com/reference/order-methods) |
| [Get Product](actions/get-product.md) | `GET /v1/products/:productId/` | [docs](https://docs.cratejoy.com/reference/product-methods) |
| [Get Shipment](actions/get-shipment.md) | `GET /v1/shipments/:shipId/` | [docs](https://docs.cratejoy.com/reference/shipment-methods-1) |
| [Get Subscription](actions/get-subscription.md) | `GET /v1/subscriptions/:subscriptionId/` | [docs](https://docs.cratejoy.com/reference/subscription-methods) |
| [Get Transaction](actions/get-transaction.md) | `GET /v1/transactions/:transactionId/` | [docs](https://docs.cratejoy.com/reference/transaction-methods) |
| [List Customer Addresses](actions/list-customer-addresses.md) | `GET /v1/customers/:customerId/addresses/` | [docs](https://docs.cratejoy.com/reference/methods-customer) |
| [List Customers](actions/list-customers.md) | `GET /v1/customers/` | [docs](https://docs.cratejoy.com/reference/methods-customer) |
| [List Inventory Levels](actions/list-inventory-levels.md) | `GET /v1/inventory/` | [docs](https://docs.cratejoy.com/reference/inventory-methods) |
| [List Orders](actions/list-orders.md) | `GET /v1/orders/` | [docs](https://docs.cratejoy.com/reference/order-methods) |
| [List Products](actions/list-products.md) | `GET /v1/products/` | [docs](https://docs.cratejoy.com/reference/product-methods) |
| [List Shipments](actions/list-shipments.md) | `GET /v1/shipments/` | [docs](https://docs.cratejoy.com/reference/shipment-methods-1) |
| [List Subscriptions](actions/list-subscriptions.md) | `GET /v1/subscriptions/` | [docs](https://docs.cratejoy.com/reference/subscription-methods) |
| [List Transactions](actions/list-transactions.md) | `GET /v1/transactions/` | [docs](https://docs.cratejoy.com/reference/transaction-methods) |
| [Reactivate Subscription](actions/reactivate-subscription.md) | `PUT /v1/subscriptions/:subscriptionId/reactivate/` | [docs](https://docs.cratejoy.com/reference/subscription-methods) |
| [Skip Subscription](actions/skip-subscription.md) | `PUT /v1/subscriptions/:subscriptionId/skip/` | [docs](https://docs.cratejoy.com/reference/subscription-methods) |
| [Update Customer](actions/update-customer.md) | `PUT /v1/customers/:customerId/` | [docs](https://docs.cratejoy.com/reference/methods-customer) |
| [Update Order](actions/update-order.md) | `PUT /v1/orders/:orderId/` | [docs](https://docs.cratejoy.com/reference/order-methods) |
| [Update Product](actions/update-product.md) | `PUT /v1/products/:productId/` | [docs](https://docs.cratejoy.com/reference/product-methods) |
| [Update Shipment](actions/update-shipment.md) | `PUT /v1/shipments/:shipId/` | [docs](https://docs.cratejoy.com/reference/shipment-methods-1) |
| [Update Subscription](actions/update-subscription.md) | `PUT /v1/subscriptions/:subscriptionId/` | [docs](https://docs.cratejoy.com/reference/subscription-methods) |
