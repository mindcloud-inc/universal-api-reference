# <img src="https://images.mindcloud.co/apps/icons/stripe-1776710109471_1777995197269.png" alt="Stripe logo" width="28" height="28"> Stripe: Universal API

Accept payments, manage subscriptions, invoice customers, and reconcile revenue.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/stripe/latest
- **Category:** Commerce / Payments & Billing
- **Actions:** 56
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

## Actions (56)

### Balance

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Balance](actions/retrieve-balance.md) | GET |  |

### Billing Portal Session

| Action | Method | Description |
| --- | --- | --- |
| [Create Billing Portal Session](actions/create-billing-portal-session.md) | POST |  |

### Charge

| Action | Method | Description |
| --- | --- | --- |
| [List Charges](actions/list-charges.md) | GET |  |
| [Retrieve Charge](actions/retrieve-charge.md) | GET |  |

### Checkout Session

| Action | Method | Description |
| --- | --- | --- |
| [List Checkout Sessions](actions/list-checkout-sessions.md) | GET |  |

### Checkout Session Line Item

| Action | Method | Description |
| --- | --- | --- |
| [List Checkout Session Line Items](actions/list-checkout-session-line-items.md) | GET | Retrieves line items for a Stripe checkout session. |

### Checkout.session

| Action | Method | Description |
| --- | --- | --- |
| [Create Checkout Session](actions/create-checkout-session.md) | POST | Creates a new checkout session in Stripe. |
| [Create Variable-Amount Checkout Session](actions/create-checkout-session-copy.md) | POST | Creates a new checkout session in Stripe. |
| [Create Setup Checkout Session – Stripe to Aspire Sync](actions/create-setup-checkout-session-stripe-to-aspire-sync.md) | POST |  |
| [Expire Checkout Session](actions/expire-checkout-session.md) | PUT | Expires an existing checkout session in Stripe. |
| [Retrieve Checkout Session](actions/retrieve-checkout-session.md) | GET | Retrieves a checkout session from Stripe. |

### Credit Note

| Action | Method | Description |
| --- | --- | --- |
| [List Credit Notes](actions/list-credit-notes.md) | GET |  |
| [Retrieve Credit Note](actions/retrieve-credit-note.md) | GET |  |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a new customer in Stripe. |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from your Stripe account. |
| [Retrieve Customer](actions/retrieve-customer.md) | GET | Retrieves a customer from your Stripe account. |
| [Search Customers](actions/search-customers.md) | GET | Finds customers in Stripe by search query. |
| [Update Customer](actions/update-customer.md) | PUT | Updates an existing customer in Stripe. |

### Dispute

| Action | Method | Description |
| --- | --- | --- |
| [List Disputes](actions/list-disputes.md) | GET |  |
| [Retrieve Dispute](actions/retrieve-dispute.md) | GET |  |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [List Events](actions/list-events.md) | GET |  |
| [Retrieve Event](actions/retrieve-event.md) | GET |  |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Create Preview Invoice](actions/create-preview-invoice.md) | POST |  |
| [Retrieve Invoice](actions/retrieve-invoice.md) | GET |  |
| [Search Invoices](actions/search-invoices.md) | GET |  |

### Invoice Line Item

| Action | Method | Description |
| --- | --- | --- |
| [List Invoice Line Items](actions/list-invoice-line-items.md) | GET |  |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves invoices from your Stripe account. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Get Balance Transactions](actions/get-balance-transactions.md) | GET |  |
| [List Payouts](actions/list-payouts.md) | GET |  |
| [Retrieve SetupIntent](actions/retrieve-setup-intent.md) | GET |  |

### Payment Method

| Action | Method | Description |
| --- | --- | --- |
| [List Customer Payment Methods](actions/list-customer-payment-methods.md) | GET |  |

### Payment Methods

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Payment Method](actions/new-action1.md) | GET |  |
| [Retrieve Payment Method sync](actions/retrieve-payment-method-sync.md) | GET |  |

### Price

| Action | Method | Description |
| --- | --- | --- |
| [List Prices](actions/list-prices.md) | GET |  |
| [Retrieve Price](actions/retrieve-price.md) | GET |  |
| [Search Prices](actions/search-prices.md) | GET |  |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Get Product](actions/get-product.md) | GET |  |
| [List Products](actions/list-products.md) | GET |  |
| [Search Products](actions/search-products.md) | GET |  |

### Refund

| Action | Method | Description |
| --- | --- | --- |
| [List Refunds](actions/list-refunds.md) | GET |  |
| [Retrieve Refund](actions/retrieve-refund.md) | GET |  |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Subscription](actions/cancel-subscription.md) | DELETE | Cancels an existing subscription in Stripe. |
| [Create Subscription](actions/create-subscription.md) | POST | Creates a new subscription in Stripe. |
| [List Subscriptions](actions/list-subscriptions.md) | GET |  |
| [Retrieve Subscription](actions/retrieve-subscription.md) | GET | Retrieves a subscription from your Stripe account. |
| [Update Subscription](actions/update-subscription.md) | PUT | Updates an existing subscription in Stripe. |

### Subscription Schedule

| Action | Method | Description |
| --- | --- | --- |
| [List Subscription Schedules](actions/list-subscription-schedules.md) | GET |  |
| [Retrieve Subscription Schedule](actions/retrieve-subscription-schedule.md) | GET |  |

### Transactions

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Payment Intent](actions/cancel-payment-intent.md) | PUT | Cancels an existing payment intent in Stripe. |
| [Capture Payment Intent](actions/capture-payment-intent.md) | PUT | Captures an existing payment intent in Stripe. |
| [Confirm Payment Intent](actions/confirm-payment-intent.md) | PUT | Confirms an existing payment intent in Stripe. |
| [Create Payment Intent](actions/create-payment-intent.md) | POST | Creates a new payment intent in Stripe. |
| [Get Payment Intent](actions/get-payment-intent.md) | GET | Retrieves a payment intent from your Stripe account. |
| [Get Payment Intent sync](actions/get-payment-intent-sync.md) | GET |  |
| [List Payment Intents](actions/list-payment-intents.md) | GET | Retrieves payment intents from your Stripe account. |
| [Search Payment Intents](actions/search-payment-intents.md) | GET | Finds payment intents in Stripe by search query. |

