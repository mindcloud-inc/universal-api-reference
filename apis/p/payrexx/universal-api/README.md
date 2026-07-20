# <img src="https://images.mindcloud.co/apps/icons/payrexx_1775671834583.png" alt="Payrexx logo" width="28" height="28"> Payrexx: Universal API

Payrexx is a payments platform for managing gateways, transactions, subscriptions, invoices, paylinks, payouts, and POS payment flows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/payrexx/latest
- **Category:** Commerce / Payments & Billing
- **Actions:** 33
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://payrexx.com/
- **Vendor API docs:** https://developers.payrexx.com/reference/rest-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Designs](actions/list-designs.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/payrexx/latest/actions/list-designs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (33)

### Design

| Action | Method | Description |
| --- | --- | --- |
| [Get Design](actions/get-design.md) | GET | Retrieves a design from Payrexx. |
| [List Designs](actions/list-designs.md) | GET | Retrieves designs from Payrexx. |

### Gateway

| Action | Method | Description |
| --- | --- | --- |
| [Create Gateway](actions/create-gateway.md) | POST | Creates a gateway in Payrexx. |
| [Delete Gateway](actions/delete-gateway.md) | DELETE | Deletes a gateway from Payrexx. |
| [Get Gateway](actions/get-gateway.md) | GET | Retrieves a gateway from Payrexx. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Create Invoice](actions/create-invoice.md) | POST | Creates an invoice in Payrexx. |
| [Delete Invoice](actions/delete-invoice.md) | DELETE | Deletes an invoice from Payrexx. |
| [Get Invoice](actions/get-invoice.md) | GET | Retrieves an invoice from Payrexx. |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves invoices from Payrexx. |
| [Update Invoice](actions/update-invoice.md) | PUT | Updates an invoice in Payrexx. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Helper Create Design](actions/helper-create-design.md) | POST | Creates a design in Payrexx. |

### Paylink

| Action | Method | Description |
| --- | --- | --- |
| [Create Paylink](actions/create-paylink.md) | POST | Creates a paylink in Payrexx. |
| [Delete Paylink](actions/delete-paylink.md) | DELETE | Deletes a paylink from Payrexx. |
| [Get Paylink](actions/get-paylink.md) | GET | Retrieves a paylink from Payrexx. |

### Payment Method

| Action | Method | Description |
| --- | --- | --- |
| [Get Payment Method](actions/get-payment-method.md) | GET | Retrieves a payment method from Payrexx. |
| [List Payment Methods](actions/list-payment-methods.md) | GET | Retrieves active payment methods from Payrexx. |

### Payment Provider

| Action | Method | Description |
| --- | --- | --- |
| [List Payment Providers](actions/list-payment-providers.md) | GET | Retrieves payment providers from Payrexx. |

### Payout

| Action | Method | Description |
| --- | --- | --- |
| [Create Manual Payout](actions/create-manual-payout.md) | POST | Creates a manual payout in Payrexx. |
| [List Payouts](actions/list-payouts.md) | GET | Retrieves payouts from Payrexx. |

### Qr Code

| Action | Method | Description |
| --- | --- | --- |
| [Create QR Code](actions/create-qr-code.md) | POST | Creates a QR code in Payrexx. |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Create Subscription](actions/create-subscription.md) | POST | Creates a subscription in Payrexx. |
| [List Subscriptions](actions/list-subscriptions.md) | GET | Retrieves subscriptions from Payrexx. |

### Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Waiting Transaction](actions/cancel-waiting-transaction.md) | PUT | Cancels a waiting transaction in Payrexx. |
| [Capture Transaction](actions/capture-transaction.md) | PUT | Captures a transaction in Payrexx. |
| [Charge Pre-Authorized Reserved Transaction](actions/charge-pre-authorized-reserved-transaction.md) | PUT | Charges a pre-authorized or reserved transaction in Payrexx. |
| [Delete Reserved Transaction](actions/delete-reserved-transaction.md) | DELETE | Deletes a reserved transaction from Payrexx. |
| [Get Transaction](actions/get-transaction.md) | GET | Retrieves a transaction from Payrexx. |
| [List Transactions](actions/list-transactions.md) | GET | Retrieves transactions from Payrexx. |
| [Pre-Authorize Tokenization](actions/pre-authorize-tokenization.md) | POST | Pre-authorizes a tokenization in Payrexx. |
| [Refund Transaction](actions/refund-transaction.md) | PUT | Refunds a transaction in Payrexx. |
| [Send Mail Receipt](actions/send-mail-receipt.md) | PUT | Sends a transaction receipt email from Payrexx. |
| [Update Pre-Authorization Tokenization Contact Details](actions/update-pre-authorization-tokenization-contact-details.md) | PUT | Updates pre-authorization or tokenization contact details in Payrexx. |
| [Update Tokenization](actions/update-tokenization.md) | PUT | Updates a tokenization in Payrexx. |

