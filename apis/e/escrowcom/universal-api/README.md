# <img src="https://images.mindcloud.co/apps/icons/escrowcom_1776265582362.png" alt="Escrow.com logo" width="28" height="28"> Escrow.com: Universal API

Create, fund, and manage escrow transactions

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/escrowcom/latest
- **Category:** Commerce / Payments & Billing
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.escrow.com
- **Vendor API docs:** https://www.escrow.com/api/docs/basics

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current Customer](actions/get-current-customer.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/get-current-customer?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Buyer Payment

| Action | Method | Description |
| --- | --- | --- |
| [Post Buyer Payment Details](actions/post-buyer-payment-details.md) | POST | Submits buyer payment details in Escrow.com. |

### Check Details

| Action | Method | Description |
| --- | --- | --- |
| [Get Check Details](actions/get-check-details.md) | GET | Retrieves check payment details from Escrow.com. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a new customer in Escrow.com. |
| [Get Current Customer](actions/get-current-customer.md) | GET | Retrieves current customer details from Escrow.com. |
| [Get Customer](actions/get-customer.md) | GET | Retrieves a customer from Escrow.com. |
| [Update Current Customer](actions/update-current-customer.md) | PUT | Updates the current customer in Escrow.com. |

### Disbursement Method

| Action | Method | Description |
| --- | --- | --- |
| [Get Transaction Disbursement Methods](actions/get-transaction-disbursement-methods.md) | GET | Retrieves transaction disbursement methods from Escrow.com. |
| [Patch Transaction Disbursement Method](actions/patch-transaction-disbursement-method.md) | PUT | Updates a transaction disbursement method in Escrow.com. |

### Landing Page

| Action | Method | Description |
| --- | --- | --- |
| [Get Milestone Item Web URL](actions/get-milestone-item-web-url.md) | GET | Retrieves a milestone item web URL from Escrow.com. |
| [Get PayPal Landing URL](actions/get-paypal-landing-url.md) | GET | Retrieves a PayPal landing URL from Escrow.com. |
| [Get Transaction Web URL](actions/get-transaction-web-url.md) | GET | Retrieves a transaction web URL from Escrow.com. |

### Milestone Item

| Action | Method | Description |
| --- | --- | --- |
| [Perform Milestone Item Action](actions/perform-milestone-item-action.md) | PUT | Performs a milestone item action in Escrow.com. |

### Partner Customer

| Action | Method | Description |
| --- | --- | --- |
| [List Partner Customers](actions/list-partner-customers.md) | GET | Retrieves partner customers from Escrow.com. |

### Partner Report

| Action | Method | Description |
| --- | --- | --- |
| [Generate Partner Report](actions/generate-partner-report.md) | POST | Creates a partner report in Escrow.com. |

### Partner Transaction

| Action | Method | Description |
| --- | --- | --- |
| [List Partner Transactions](actions/list-partner-transactions.md) | GET | Retrieves partner transactions from Escrow.com. |

### Payment Method

| Action | Method | Description |
| --- | --- | --- |
| [Get Transaction Payment Methods](actions/get-transaction-payment-methods.md) | GET | Retrieves transaction payment methods from Escrow.com. |
| [Select Payment Method](actions/select-payment-method.md) | POST | Selects a transaction payment method in Escrow.com. |

### Timeline Entry

| Action | Method | Description |
| --- | --- | --- |
| [Get Transaction Timeline Entries](actions/get-transaction-timeline-entries.md) | GET | Retrieves transaction timeline entries from Escrow.com. |

### Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Create Transaction](actions/create-transaction.md) | POST | Creates a new transaction in Escrow.com. |
| [Get Transaction](actions/get-transaction.md) | GET | Retrieves a transaction from Escrow.com. |
| [Get Transaction by Reference](actions/get-transaction-by-reference.md) | GET | Retrieves a transaction from Escrow.com by reference. |
| [List Transactions](actions/list-transactions.md) | GET | Retrieves transaction records from Escrow.com. |
| [Perform Transaction Action](actions/perform-transaction-action.md) | PUT | Performs a transaction action in Escrow.com. |

### Wire Transfer Details

| Action | Method | Description |
| --- | --- | --- |
| [Get Wire Transfer Details](actions/get-wire-transfer-details.md) | GET | Retrieves wire transfer details from Escrow.com. |

