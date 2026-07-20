# <img src="https://images.mindcloud.co/apps/icons/charge-over_1774019596579.png" alt="ChargeOver logo" width="28" height="28"> ChargeOver: Universal API

Manage customers, subscriptions, invoices, payments, and usage billing

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/chargeOver/latest
- **Category:** Commerce / Payments & Billing
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://chargeover.com/
- **Vendor API docs:** https://developer.chargeover.com/docs/api/chargeover-rest-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Customers](actions/list-customers.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargeOver/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Get Contact](actions/get-contact.md) | GET | Retrieves detailed contact records from ChargeOver. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves customer contact records from ChargeOver. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer](actions/get-customer.md) | GET | Retrieves detailed customer records from ChargeOver. |
| [List Customers](actions/list-customers.md) | GET | Retrieves customer account records from ChargeOver. |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [Email Invoice](actions/email-invoice.md) | PUT | Emails an existing invoice from ChargeOver. |
| [Get Invoice](actions/get-invoice.md) | GET | Retrieves detailed invoice records from ChargeOver. |
| [Get Invoice PDF](actions/get-invoice-pdf.md) | GET | Retrieves an invoice PDF from ChargeOver. |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves billing invoice records from ChargeOver. |
| [Void Invoice](actions/void-invoice.md) | PUT | Voids an existing invoice in ChargeOver. |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [Get Item](actions/get-item.md) | GET | Retrieves detailed item records from ChargeOver. |
| [List Items](actions/list-items.md) | GET | Retrieves catalog item records from ChargeOver. |

### Subscriptions

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Subscription](actions/cancel-subscription.md) | PUT | Cancels an existing subscription in ChargeOver. |
| [Get Subscription](actions/get-subscription.md) | GET | Retrieves detailed subscription records from ChargeOver. |
| [Invoice Subscription Now](actions/invoice-subscription-now.md) | PUT | Invoices an existing subscription immediately in ChargeOver. |
| [List Subscriptions](actions/list-subscriptions.md) | GET | Retrieves billing subscription records from ChargeOver. |
| [Suspend Subscription](actions/suspend-subscription.md) | PUT | Suspends an existing subscription in ChargeOver. |
| [Uncancel Subscription](actions/uncancel-subscription.md) | PUT | Reactivates a canceled subscription in ChargeOver. |
| [Unsuspend Subscription](actions/unsuspend-subscription.md) | PUT | Resumes a suspended subscription in ChargeOver. |

### Transactions

| Action | Method | Description |
| --- | --- | --- |
| [Email Receipt](actions/email-receipt.md) | PUT | Emails a transaction receipt from ChargeOver. |
| [Get Transaction](actions/get-transaction.md) | GET | Retrieves detailed transaction records from ChargeOver. |
| [List Transactions](actions/list-transactions.md) | GET | Retrieves billing transaction records from ChargeOver. |
| [Void Transaction](actions/void-transaction.md) | PUT | Voids an existing transaction in ChargeOver. |

### Usage Record

| Action | Method | Description |
| --- | --- | --- |
| [List Usage Records](actions/list-usage-records.md) | GET | Retrieves metered usage records from ChargeOver. |
| [Record Usage](actions/record-usage.md) | POST | Creates a new metered usage record in ChargeOver. |

