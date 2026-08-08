# Stripe: Native API Reference

A consolidated summary of Stripe's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.stripe.com/api
- **API base URL:** `https://api.stripe.com/v1`

## Authentication

### Basic

Stripe uses your secret API key as the HTTP Basic username. Leave the password empty.

### Credentials

- **Secret API key:** `username` · required
- **Password:** `password` · optional · Leave this empty.

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://docs.stripe.com/keys)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–100). Use `starting_after` in the query string as the pagination cursor.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Payment Intent](actions/cancel-payment-intent.md) | `POST payment_intents/:intent/cancel` | [docs](https://docs.stripe.com/api/payment_intents/cancel) |
| [Cancel Subscription](actions/cancel-subscription.md) | `DELETE subscriptions/:subscription_exposed_id` | [docs](https://docs.stripe.com/api/subscriptions/cancel) |
| [Capture Payment Intent](actions/capture-payment-intent.md) | `POST payment_intents/:intent/capture` | [docs](https://docs.stripe.com/api/payment_intents/capture) |
| [Confirm Payment Intent](actions/confirm-payment-intent.md) | `POST payment_intents/:intent/confirm` | [docs](https://docs.stripe.com/api/payment_intents/confirm) |
| [Create Checkout Session](actions/create-checkout-session.md) | `POST checkout/sessions` | [docs](https://docs.stripe.com/api/checkout/sessions/create) |
| [Create Customer](actions/create-customer.md) | `POST customers` | [docs](https://docs.stripe.com/api/customers/create) |
| [Create Payment Intent](actions/create-payment-intent.md) | `POST payment_intents` | [docs](https://docs.stripe.com/api/payment_intents/create) |
| [Create Subscription](actions/create-subscription.md) | `POST subscriptions` | [docs](https://docs.stripe.com/api/subscriptions/create) |
| [Expire Checkout Session](actions/expire-checkout-session.md) | `POST checkout/sessions/:session/expire` | [docs](https://docs.stripe.com/api/checkout/sessions/expire) |
| [Get Balance Transactions](actions/get-balance-transactions.md) | `GET /balance_transactions?payout={{payoutId}}&limit={{limit}}&expand[]=data.source&expand[]=data.source.charge` |  |
| [Get Payment Intent](actions/get-payment-intent.md) | `GET payment_intents/:intent` | [docs](https://docs.stripe.com/api/payment_intents/retrieve) |
| [List Checkout Session Line Items](actions/list-checkout-session-line-items.md) | `GET checkout/sessions/:session/line_items` | [docs](https://docs.stripe.com/api/checkout/sessions/line_items) |
| [List Customers](actions/list-customers.md) | `GET customers` | [docs](https://docs.stripe.com/api/customers/list) |
| [List Invoices](actions/list-invoices.md) | `GET invoices` | [docs](https://docs.stripe.com/api/invoices/list) |
| [List Payment Intents](actions/list-payment-intents.md) | `GET payment_intents` | [docs](https://docs.stripe.com/api/payment_intents/list) |
| [List Payouts](actions/list-payouts.md) | `GET /payouts?arrival_date[gte]={{arrivalDateGte}}&arrival_date[lte]={{arrivalDateLte}}&status={{status}}&limit={{limit}}` |  |
| [Retrieve Payment Method](actions/new-action1.md) | `GET payment_methods/:paymentMethodId` |  |
| [Retrieve Checkout Session](actions/retrieve-checkout-session.md) | `GET checkout/sessions/:session` | [docs](https://docs.stripe.com/api/checkout/sessions/retrieve) |
| [Retrieve Customer](actions/retrieve-customer.md) | `GET customers/:customer` | [docs](https://docs.stripe.com/api/customers/retrieve) |
| [Retrieve Subscription](actions/retrieve-subscription.md) | `GET subscriptions/:subscription_exposed_id` | [docs](https://docs.stripe.com/api/subscriptions/retrieve) |
| [Search Customers](actions/search-customers.md) | `GET customers/search` | [docs](https://docs.stripe.com/api/customers/search) |
| [Search Payment Intents](actions/search-payment-intents.md) | `GET payment_intents/search` | [docs](https://docs.stripe.com/api/payment_intents/search) |
| [Update Customer](actions/update-customer.md) | `POST customers/:customer` | [docs](https://docs.stripe.com/api/customers/update) |
| [Update Subscription](actions/update-subscription.md) | `POST subscriptions/:subscription_exposed_id` | [docs](https://docs.stripe.com/api/subscriptions/update) |
