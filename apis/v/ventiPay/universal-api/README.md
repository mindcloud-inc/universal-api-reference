# <img src="https://images.mindcloud.co/apps/icons/venti-pay_1774299187193.png" alt="VentiPay logo" width="28" height="28"> VentiPay: Universal API

Manage payments, subscriptions, customers, and payment methods

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/ventiPay/latest
- **Category:** Commerce / Payments & Billing
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://ventipay.com
- **Vendor API docs:** https://docs.ventipay.com/docs/welcome

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Balance](actions/get-balance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ventiPay/latest/actions/get-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer](actions/get-customer.md) | GET | Retrieves a customer from VentiPay. |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from VentiPay. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a new customer in VentiPay. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves invoices from VentiPay. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Get Balance](actions/get-balance.md) | GET | Retrieves the current merchant balance from VentiPay. |

### Payment

| Action | Method | Description |
| --- | --- | --- |
| [List Payments](actions/list-payments.md) | GET | Retrieves payments from VentiPay. |

### Payment Method

| Action | Method | Description |
| --- | --- | --- |
| [List Payment Methods](actions/list-payment-methods.md) | GET | Retrieves payment methods from VentiPay. |

### Payout

| Action | Method | Description |
| --- | --- | --- |
| [List Payouts](actions/list-payouts.md) | GET | Retrieves payouts from VentiPay. |

### Plan

| Action | Method | Description |
| --- | --- | --- |
| [List Plans](actions/list-plans.md) | GET | Retrieves plans from VentiPay. |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [List Subscriptions](actions/list-subscriptions.md) | GET | Retrieves subscriptions from VentiPay. |

