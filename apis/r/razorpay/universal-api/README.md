# <img src="https://images.mindcloud.co/apps/icons/razorpay_1773345944567.png" alt="Razorpay logo" width="28" height="28"> Razorpay: Universal API

Accept, capture, refund, and reconcile payments with Razorpay APIs

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/razorpay/latest
- **Category:** Commerce / Payments & Billing
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://razorpay.com/
- **Vendor API docs:** https://razorpay.com/docs/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Dispute](actions/get-dispute.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/razorpay/latest/actions/get-dispute?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a new customer in Razorpay. |
| [List Customers](actions/list-customers.md) | GET | Retrieves all customer records from Razorpay. |
| [Update Customer](actions/update-customer.md) | PUT | Updates an existing customer in Razorpay. |

### Disputes

| Action | Method | Description |
| --- | --- | --- |
| [Accept Dispute](actions/accept-dispute.md) | PUT | Accepts a dispute in Razorpay as lost. |
| [Get Dispute](actions/get-dispute.md) | GET | Retrieves a dispute from Razorpay by ID. |
| [List Disputes](actions/list-disputes.md) | GET | Retrieves all dispute records from Razorpay. |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [Create Order](actions/create-order.md) | POST | Creates a new order in Razorpay. |
| [Get Order](actions/get-order.md) | GET | Retrieves an order from Razorpay by ID. |
| [List Orders](actions/list-orders.md) | GET | Retrieves all order records from Razorpay. |

### Payments

| Action | Method | Description |
| --- | --- | --- |
| [Capture Payment](actions/capture-payment.md) | PUT | Captures an authorized payment in Razorpay. |
| [Create Payment Link](actions/create-payment-link.md) | POST | Creates a new payment link in Razorpay. |
| [Get Payment](actions/get-payment.md) | GET | Retrieves a payment from Razorpay by ID. |
| [Get Payment Card Details](actions/get-payment-card-details.md) | GET | Retrieves card details for a payment from Razorpay. |
| [Get Payment Link](actions/get-payment-link.md) | GET | Retrieves a payment link from Razorpay by ID. |
| [List Order Payments](actions/list-order-payments.md) | GET | Retrieves payments for a specific order from Razorpay. |
| [List Payment Links](actions/list-payment-links.md) | GET | Retrieves payment link records from Razorpay. |
| [List Payments](actions/list-payments.md) | GET | Retrieves all payment records from Razorpay. |
| [Update Payment Link](actions/update-payment-link.md) | PUT | Updates an existing payment link in Razorpay. |

### Refunds

| Action | Method | Description |
| --- | --- | --- |
| [Create Payment Refund](actions/create-payment-refund.md) | POST | Creates a refund for a payment in Razorpay. |
| [Get Refund](actions/get-refund.md) | GET | Retrieves a refund from Razorpay by ID. |
| [List Payment Refunds](actions/list-payment-refunds.md) | GET | Retrieves refunds for a specific payment from Razorpay. |
| [List Refunds](actions/list-refunds.md) | GET | Retrieves all refund records from Razorpay. |

### Settlements

| Action | Method | Description |
| --- | --- | --- |
| [Get Settlement](actions/get-settlement.md) | GET | Retrieves a settlement from Razorpay by ID. |
| [List Settlements](actions/list-settlements.md) | GET | Retrieves all settlement records from Razorpay. |

