# Stripe: Native API Reference

A consolidated summary of Stripe's API configuration and 56 documented operations, with links to official documentation.

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

## Endpoints (56 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Payment Intent](actions/cancel-payment-intent.md) | `POST payment_intents/:intent/cancel` | [docs](https://docs.stripe.com/api/payment_intents/cancel) |
| [Cancel Subscription](actions/cancel-subscription.md) | `DELETE subscriptions/:subscription_exposed_id` | [docs](https://docs.stripe.com/api/subscriptions/cancel) |
| [Capture Payment Intent](actions/capture-payment-intent.md) | `POST payment_intents/:intent/capture` | [docs](https://docs.stripe.com/api/payment_intents/capture) |
| [Confirm Payment Intent](actions/confirm-payment-intent.md) | `POST payment_intents/:intent/confirm` | [docs](https://docs.stripe.com/api/payment_intents/confirm) |
| [Create Billing Portal Session](actions/create-billing-portal-session.md) | `POST billing_portal/sessions` | [docs](https://docs.stripe.com/api/customer_portal/sessions/create) |
| [Create Checkout Session](actions/create-checkout-session.md) | `POST checkout/sessions` | [docs](https://docs.stripe.com/api/checkout/sessions/create) |
| [Create Variable-Amount Checkout Session](actions/create-checkout-session-copy.md) | `POST checkout/sessions` | [docs](https://docs.stripe.com/api/checkout/sessions/create) |
| [Create Customer](actions/create-customer.md) | `POST customers` | [docs](https://docs.stripe.com/api/customers/create) |
| [Create Payment Intent](actions/create-payment-intent.md) | `POST payment_intents` | [docs](https://docs.stripe.com/api/payment_intents/create) |
| [Create Preview Invoice](actions/create-preview-invoice.md) | `POST invoices/create_preview` | [docs](https://docs.stripe.com/api/invoices/create_preview) |
| [Create Setup Checkout Session – Stripe to Aspire Sync](actions/create-setup-checkout-session-stripe-to-aspire-sync.md) | `POST checkout/sessions` | [docs](https://docs.stripe.com/api/checkout/sessions/create) |
| [Create Subscription](actions/create-subscription.md) | `POST subscriptions` | [docs](https://docs.stripe.com/api/subscriptions/create) |
| [Expire Checkout Session](actions/expire-checkout-session.md) | `POST checkout/sessions/:session/expire` | [docs](https://docs.stripe.com/api/checkout/sessions/expire) |
| [Get Balance Transactions](actions/get-balance-transactions.md) | `GET /balance_transactions?payout={{payoutId}}&limit={{limit}}&expand[]=data.source&expand[]=data.source.charge` |  |
| [Get Payment Intent](actions/get-payment-intent.md) | `GET payment_intents/:intent` | [docs](https://docs.stripe.com/api/payment_intents/retrieve) |
| [Get Payment Intent sync](actions/get-payment-intent-sync.md) | `GET payment_intents/:intent` | [docs](https://docs.stripe.com/api/payment_intents/retrieve) |
| [Get Product](actions/get-product.md) | `GET products/:id` | [docs](https://docs.stripe.com/api/products/retrieve) |
| [List Charges](actions/list-charges.md) | `GET charges` | [docs](https://docs.stripe.com/api/charges/list) |
| [List Checkout Session Line Items](actions/list-checkout-session-line-items.md) | `GET checkout/sessions/:session/line_items` | [docs](https://docs.stripe.com/api/checkout/sessions/line_items) |
| [List Checkout Sessions](actions/list-checkout-sessions.md) | `GET checkout/sessions` | [docs](https://docs.stripe.com/api/checkout/sessions/list) |
| [List Credit Notes](actions/list-credit-notes.md) | `GET credit_notes` | [docs](https://docs.stripe.com/api/credit_notes/list) |
| [List Customer Payment Methods](actions/list-customer-payment-methods.md) | `GET customers/:customer/payment_methods` | [docs](https://docs.stripe.com/api/payment_methods/customer_list) |
| [List Customers](actions/list-customers.md) | `GET customers` | [docs](https://docs.stripe.com/api/customers/list) |
| [List Disputes](actions/list-disputes.md) | `GET disputes` | [docs](https://docs.stripe.com/api/disputes/list) |
| [List Events](actions/list-events.md) | `GET events` | [docs](https://docs.stripe.com/api/events/list) |
| [List Invoice Line Items](actions/list-invoice-line-items.md) | `GET invoices/:invoice/lines` | [docs](https://docs.stripe.com/api/invoice-line-item/retrieve) |
| [List Invoices](actions/list-invoices.md) | `GET invoices` | [docs](https://docs.stripe.com/api/invoices/list) |
| [List Payment Intents](actions/list-payment-intents.md) | `GET payment_intents` | [docs](https://docs.stripe.com/api/payment_intents/list) |
| [List Payouts](actions/list-payouts.md) | `GET /payouts?arrival_date[gte]={{arrivalDateGte}}&arrival_date[lte]={{arrivalDateLte}}&status={{status}}&limit={{limit}}` |  |
| [List Prices](actions/list-prices.md) | `GET prices` | [docs](https://docs.stripe.com/api/prices/list) |
| [List Products](actions/list-products.md) | `GET products` | [docs](https://docs.stripe.com/api/products/list) |
| [List Refunds](actions/list-refunds.md) | `GET refunds` | [docs](https://docs.stripe.com/api/refunds/list) |
| [List Subscription Schedules](actions/list-subscription-schedules.md) | `GET subscription_schedules` | [docs](https://docs.stripe.com/api/subscription_schedules/list) |
| [List Subscriptions](actions/list-subscriptions.md) | `GET subscriptions` | [docs](https://docs.stripe.com/api/subscriptions/list) |
| [Retrieve Payment Method](actions/new-action1.md) | `GET payment_methods/:paymentMethodId` |  |
| [Retrieve Balance](actions/retrieve-balance.md) | `GET balance` | [docs](https://docs.stripe.com/api/balance/balance_retrieve) |
| [Retrieve Charge](actions/retrieve-charge.md) | `GET charges/:charge` | [docs](https://docs.stripe.com/api/charges/retrieve) |
| [Retrieve Checkout Session](actions/retrieve-checkout-session.md) | `GET checkout/sessions/:session` | [docs](https://docs.stripe.com/api/checkout/sessions/retrieve) |
| [Retrieve Credit Note](actions/retrieve-credit-note.md) | `GET credit_notes/:creditNote` | [docs](https://docs.stripe.com/api/credit_notes/retrieve) |
| [Retrieve Customer](actions/retrieve-customer.md) | `GET customers/:customer` | [docs](https://docs.stripe.com/api/customers/retrieve) |
| [Retrieve Dispute](actions/retrieve-dispute.md) | `GET disputes/:dispute` | [docs](https://docs.stripe.com/api/disputes/retrieve) |
| [Retrieve Event](actions/retrieve-event.md) | `GET events/:event` | [docs](https://docs.stripe.com/api/events/retrieve) |
| [Retrieve Invoice](actions/retrieve-invoice.md) | `GET invoices/:invoice` | [docs](https://docs.stripe.com/api/invoices/retrieve) |
| [Retrieve Payment Method sync](actions/retrieve-payment-method-sync.md) | `GET payment_methods/:paymentMethodId` | [docs](https://docs.stripe.com/api/payment_methods/retrieve) |
| [Retrieve Price](actions/retrieve-price.md) | `GET prices/:price` | [docs](https://docs.stripe.com/api/prices/retrieve) |
| [Retrieve Refund](actions/retrieve-refund.md) | `GET refunds/:refund` | [docs](https://docs.stripe.com/api/refunds/retrieve) |
| [Retrieve SetupIntent](actions/retrieve-setup-intent.md) | `GET setup_intents/:setupIntent` | [docs](https://docs.stripe.com/api/setup_intents/retrieve) |
| [Retrieve Subscription](actions/retrieve-subscription.md) | `GET subscriptions/:subscription_exposed_id` | [docs](https://docs.stripe.com/api/subscriptions/retrieve) |
| [Retrieve Subscription Schedule](actions/retrieve-subscription-schedule.md) | `GET subscription_schedules/:schedule` | [docs](https://docs.stripe.com/api/subscription_schedules/retrieve) |
| [Search Customers](actions/search-customers.md) | `GET customers/search` | [docs](https://docs.stripe.com/api/customers/search) |
| [Search Invoices](actions/search-invoices.md) | `GET invoices/search` | [docs](https://docs.stripe.com/api/invoices/search) |
| [Search Payment Intents](actions/search-payment-intents.md) | `GET payment_intents/search` | [docs](https://docs.stripe.com/api/payment_intents/search) |
| [Search Prices](actions/search-prices.md) | `GET prices/search` | [docs](https://docs.stripe.com/api/prices/search) |
| [Search Products](actions/search-products.md) | `GET products/search` | [docs](https://docs.stripe.com/api/products/search) |
| [Update Customer](actions/update-customer.md) | `POST customers/:customer` | [docs](https://docs.stripe.com/api/customers/update) |
| [Update Subscription](actions/update-subscription.md) | `POST subscriptions/:subscription_exposed_id` | [docs](https://docs.stripe.com/api/subscriptions/update) |
