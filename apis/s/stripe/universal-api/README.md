# <img src="https://images.mindcloud.co/apps/icons/stripe-1776710109471_1777995197269.png" alt="Stripe logo" width="28" height="28"> Stripe: Universal API

Accept payments, manage subscriptions, invoice customers, and reconcile revenue.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/stripe/latest
- **Category:** Commerce / Payments & Billing
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://stripe.com
- **Vendor API docs:** https://docs.stripe.com/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Customers](actions/list-customers.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stripe/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Checkout Session Line Item

| Action | Method | Description |
| --- | --- | --- |
| [List Checkout Session Line Items](actions/list-checkout-session-line-items.md) | GET | Retrieves line items for a Stripe checkout session. |

### Checkout.session

| Action | Method | Description |
| --- | --- | --- |
| [Create Checkout Session](actions/create-checkout-session.md) | POST | Creates a new checkout session in Stripe. |
| [Create Variable-Amount Checkout Session](actions/create-checkout-session-copy.md) | POST | Creates a new checkout session in Stripe. |
| [Expire Checkout Session](actions/expire-checkout-session.md) | PUT | Expires an existing checkout session in Stripe. |
| [Retrieve Checkout Session](actions/retrieve-checkout-session.md) | GET | Retrieves a checkout session from Stripe. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a new customer in Stripe. |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from your Stripe account. |
| [Retrieve Customer](actions/retrieve-customer.md) | GET | Retrieves a customer from your Stripe account. |
| [Search Customers](actions/search-customers.md) | GET | Finds customers in Stripe by search query. |
| [Update Customer](actions/update-customer.md) | PUT | Updates an existing customer in Stripe. |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves invoices from your Stripe account. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Get Balance Transactions](actions/get-balance-transactions.md) | GET |  |
| [List Payouts](actions/list-payouts.md) | GET |  |
| [Retrieve Payment Method](actions/new-action1.md) | GET |  |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Subscription](actions/cancel-subscription.md) | DELETE | Cancels an existing subscription in Stripe. |
| [Create Subscription](actions/create-subscription.md) | POST | Creates a new subscription in Stripe. |
| [Retrieve Subscription](actions/retrieve-subscription.md) | GET | Retrieves a subscription from your Stripe account. |
| [Update Subscription](actions/update-subscription.md) | PUT | Updates an existing subscription in Stripe. |

### Transactions

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Payment Intent](actions/cancel-payment-intent.md) | PUT | Cancels an existing payment intent in Stripe. |
| [Capture Payment Intent](actions/capture-payment-intent.md) | PUT | Captures an existing payment intent in Stripe. |
| [Confirm Payment Intent](actions/confirm-payment-intent.md) | PUT | Confirms an existing payment intent in Stripe. |
| [Create Payment Intent](actions/create-payment-intent.md) | POST | Creates a new payment intent in Stripe. |
| [Get Payment Intent](actions/get-payment-intent.md) | GET | Retrieves a payment intent from your Stripe account. |
| [List Payment Intents](actions/list-payment-intents.md) | GET | Retrieves payment intents from your Stripe account. |
| [Search Payment Intents](actions/search-payment-intents.md) | GET | Finds payment intents in Stripe by search query. |

