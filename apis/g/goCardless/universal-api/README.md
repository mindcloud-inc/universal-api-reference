# <img src="https://images.mindcloud.co/apps/icons/id-fq1u-huqa-1773340552301_1773340558571.png" alt="GoCardless logo" width="28" height="28"> GoCardless: Universal API

Collect payments, manage mandates, and track billing events

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/goCardless/latest
- **Category:** Commerce / Payments & Billing
- **Actions:** 27
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://gocardless.com
- **Vendor API docs:** https://developer.gocardless.com/api-reference/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Billing Request](actions/get-billing-request.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/get-billing-request?connectionId=$CONNECTION_ID&billingRequestId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (27)

### Billing Request

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Billing Request](actions/cancel-billing-request.md) | PUT | Cancels an existing billing request in GoCardless. |
| [Collect Billing Request Customer Details](actions/collect-billing-request-customer-details.md) | PUT | Collects customer details for a GoCardless billing request. |
| [Create Billing Request](actions/create-billing-request.md) | POST | Creates a new billing request in GoCardless. |
| [Get Billing Request](actions/get-billing-request.md) | GET | Retrieves a single billing request from GoCardless. |
| [List Billing Requests](actions/list-billing-requests.md) | GET | Finds billing requests in your GoCardless account. |

### Billing Request Flow

| Action | Method | Description |
| --- | --- | --- |
| [Create Billing Request Flow](actions/create-billing-request-flow.md) | POST | Creates a new billing request flow in GoCardless. |
| [Initialise Billing Request Flow](actions/initialise-billing-request-flow.md) | PUT | Initialises a GoCardless billing request flow. |

### Creditor

| Action | Method | Description |
| --- | --- | --- |
| [List Creditors](actions/list-creditors.md) | GET | Finds creditors in your GoCardless account. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a new customer in GoCardless. |
| [Get Customer](actions/get-customer.md) | GET | Retrieves a single customer from GoCardless. |
| [List Customers](actions/list-customers.md) | GET | Finds customers in your GoCardless account. |

### Customer Bank Account

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer Bank Account](actions/create-customer-bank-account.md) | POST | Creates a new customer bank account in GoCardless. |
| [List Customer Bank Accounts](actions/list-customer-bank-accounts.md) | GET | Finds customer bank accounts in GoCardless. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Get Event](actions/get-event.md) | GET | Retrieves a single event from GoCardless. |
| [List Events](actions/list-events.md) | GET | Finds events in your GoCardless account. |

### Mandate

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Mandate](actions/cancel-mandate.md) | PUT | Cancels an existing mandate in GoCardless. |
| [Create Mandate](actions/create-mandate.md) | POST | Creates a new mandate in GoCardless. |
| [Get Mandate](actions/get-mandate.md) | GET | Retrieves a single mandate from GoCardless. |
| [List Mandates](actions/list-mandates.md) | GET | Finds mandates in your GoCardless account. |

### Payment

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Payment](actions/cancel-payment.md) | PUT | Cancels an existing payment in GoCardless. |
| [Create Payment](actions/create-payment.md) | POST | Creates a new payment in GoCardless. |
| [Get Payment](actions/get-payment.md) | GET | Retrieves a single payment from GoCardless. |
| [List Payments](actions/list-payments.md) | GET | Finds payments in your GoCardless account. |
| [Retry Payment](actions/retry-payment.md) | PUT | Retries an existing payment in GoCardless. |

### Refund

| Action | Method | Description |
| --- | --- | --- |
| [List Refunds](actions/list-refunds.md) | GET | Finds refunds in your GoCardless account. |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Create Subscription](actions/create-subscription.md) | POST | Creates a new subscription in GoCardless. |
| [List Subscriptions](actions/list-subscriptions.md) | GET | Finds subscriptions in your GoCardless account. |

