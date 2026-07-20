# ChargeDesk: Native API Reference

A consolidated summary of ChargeDesk's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://chargedesk.com/api-docs
- **API base URL:** `https://api.chargedesk.com/v1`

## Authentication

### Secret Key

HTTP Basic authentication using the ChargeDesk company secret key as the username. ChargeDesk does not require a password.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://chargedesk.com/api-docs#information-api-authentication)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

Responses from this API use JSON.

## Pagination

Use `count` in the query string to set the page size (default 100; minimum 1). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Charge](actions/create-charge.md) | `POST /charges` | [docs](https://chargedesk.com/api-docs#charges-create) |
| [Create Customer](actions/create-customer.md) | `POST /customers` | [docs](https://chargedesk.com/api-docs#customers-create) |
| [Create Product](actions/create-product.md) | `POST /products` | [docs](https://chargedesk.com/api-docs#products-create) |
| [Create Subscription](actions/create-subscription.md) | `POST /subscriptions` | [docs](https://chargedesk.com/api-docs#subscriptions-create) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks` | [docs](https://chargedesk.com/api-docs#webhooks-create) |
| [Email Charge](actions/email-charge.md) | `POST /charges/:CHARGE_ID/email` | [docs](https://chargedesk.com/api-docs#charges-email-charge) |
| [Group Customers](actions/group-customers.md) | `GET /customers/grouped` | [docs](https://chargedesk.com/api-docs#customers-grouped) |
| [List Agent Activity](actions/list-agent-activity.md) | `GET /log/activity` | [docs](https://chargedesk.com/api-docs#logs-agent-activity) |
| [List Charges](actions/list-charges.md) | `GET /charges` | [docs](https://chargedesk.com/api-docs#charges-list-all) |
| [List Customers](actions/list-customers.md) | `GET /customers` | [docs](https://chargedesk.com/api-docs#customers-list-all) |
| [List Products](actions/list-products.md) | `GET /products` | [docs](https://chargedesk.com/api-docs#products-list-all) |
| [List Subscription Cancellations](actions/list-subscription-cancellations.md) | `GET /log/cancellations` | [docs](https://chargedesk.com/api-docs#logs-subscription-cancellations) |
| [List Subscriptions](actions/list-subscriptions.md) | `GET /subscriptions` | [docs](https://chargedesk.com/api-docs#subscriptions-list-all) |
| [List Webhook Notifications](actions/list-webhook-notifications.md) | `GET /webhooks/notifications` | [docs](https://chargedesk.com/api-docs#webhooks-notifications) |
| [Preview Charge](actions/preview-charge.md) | `GET /charges/preview` | [docs](https://chargedesk.com/api-docs#charges-preview-charge) |
| [Retrieve Charge](actions/retrieve-charge.md) | `GET /charges/:CHARGE_ID` | [docs](https://chargedesk.com/api-docs#charges-retrieve) |
| [Retrieve Charge Items](actions/retrieve-charge-items.md) | `GET /charges/:CHARGE_ID/items` | [docs](https://chargedesk.com/api-docs#charges-retrieve-items) |
| [Retrieve Customer](actions/retrieve-customer.md) | `GET /customers/:CUSTOMER_ID` | [docs](https://chargedesk.com/api-docs#customers-retrieve) |
| [Retrieve Product](actions/retrieve-product.md) | `GET /products/:PRODUCT_ID` | [docs](https://chargedesk.com/api-docs#products-retrieve) |
| [Retrieve Subscription](actions/retrieve-subscription.md) | `GET /subscriptions/:SUBSCRIPTION_ID` | [docs](https://chargedesk.com/api-docs#subscriptions-retrieve) |
| [Update Charge](actions/update-charge.md) | `POST /charges/:CHARGE_ID` | [docs](https://chargedesk.com/api-docs#charges-update) |
| [Update Customer](actions/update-customer.md) | `POST /customers/:CUSTOMER_ID` | [docs](https://chargedesk.com/api-docs#customers-update) |
| [Update Product](actions/update-product.md) | `POST /products/:PRODUCT_ID` | [docs](https://chargedesk.com/api-docs#products-update) |
| [Update Subscription](actions/update-subscription.md) | `POST /subscriptions/:SUBSCRIPTION_ID` | [docs](https://chargedesk.com/api-docs#subscriptions-update) |
