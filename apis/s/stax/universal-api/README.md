# <img src="https://images.mindcloud.co/apps/icons/images-6_1774366084506.png" alt="Stax logo" width="28" height="28"> Stax: Universal API

Stax is a payments platform for processing merchant payments, customers, transactions, invoices, payment methods, and related billing workflows through the Stax Pay API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/stax/latest
- **Category:** Commerce / Payments & Billing
- **Actions:** 41
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://staxpayments.com
- **Vendor API docs:** https://docs.staxpayments.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Customers](actions/list-customers.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stax/latest/actions/list-customers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (41)

### Ach Rejection Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Statement ACH Rejections](actions/get-statement-ach-rejections.md) | GET | Retrieves statement ACH rejections from Stax. |

### Card Processing Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Statement Card Processing](actions/get-statement-card-processing.md) | GET | Retrieves statement card processing totals from Stax. |

### Card Type Volume Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Statement Volumes by Card Type](actions/get-statement-volumes-by-card-type.md) | GET | Retrieves statement volumes by card type from Stax. |

### Charge

| Action | Method | Description |
| --- | --- | --- |
| [Charge Payment Method](actions/charge-payment-method.md) | POST | Charges a payment method in Stax. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a customer in Stax. |
| [Delete Customer](actions/delete-customer.md) | DELETE | Soft deletes a customer from Stax. |
| [Get Customer](actions/get-customer.md) | GET | Retrieves a customer from Stax. |
| [Update Customer](actions/update-customer.md) | PUT | Updates a customer in Stax. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from Stax. |

### Daily Sales

| Action | Method | Description |
| --- | --- | --- |
| [Get Daily Sales](actions/get-daily-sales.md) | GET | Retrieves daily sales totals from Stax. |

### Deposit Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Deposit Details](actions/get-deposit-details.md) | GET | Retrieves details for a deposit in Stax. |
| [List Deposits](actions/list-deposits.md) | GET | Retrieves deposits from Stax. |

### Dispute Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Statement Disputes](actions/get-statement-disputes.md) | GET | Retrieves statement disputes from Stax. |

### Funding Instructions

| Action | Method | Description |
| --- | --- | --- |
| [Get Transaction Funding Instructions](actions/get-transaction-funding-instructions.md) | GET | Retrieves funding instructions for a transaction in Stax. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Get Invoice](actions/get-invoice.md) | GET | Retrieves an invoice from Stax. |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves invoices from Stax. |

### Merchant Account

| Action | Method | Description |
| --- | --- | --- |
| [Get User and Team Info](actions/get-user-and-team-info.md) | GET | Retrieves your user and team details from Stax. |

### Payment Link

| Action | Method | Description |
| --- | --- | --- |
| [Create Payment Link](actions/create-payment-link.md) | POST | Creates a payment link in Stax. |
| [Delete Payment Link](actions/delete-payment-link.md) | DELETE | Deletes a payment link from Stax. |
| [Get Payment Link](actions/get-payment-link.md) | GET | Retrieves a payment link from Stax. |
| [Get Payment Link Active Status](actions/get-payment-link-active-status.md) | GET | Retrieves a payment link's active status in Stax. |
| [List Payment Links](actions/list-payment-links.md) | GET | Retrieves payment links from Stax. |
| [Update Payment Link](actions/update-payment-link.md) | PUT | Updates or deactivates a payment link in Stax. |

### Payment Method

| Action | Method | Description |
| --- | --- | --- |
| [Create Card Payment Method](actions/create-card-payment-method.md) | POST | Creates a card payment method in Stax. |
| [Delete Payment Method](actions/delete-payment-method.md) | DELETE | Deletes a payment method from Stax. |
| [Get Payment Method](actions/get-payment-method.md) | GET | Retrieves a payment method from Stax. |
| [List Customer Payment Methods](actions/list-customer-payment-methods.md) | GET | Retrieves a customer's payment methods from Stax. |
| [List Merchant Payment Methods](actions/list-merchant-payment-methods.md) | GET | Retrieves merchant payment methods from Stax. |
| [Update Payment Method](actions/update-payment-method.md) | PUT | Updates a payment method in Stax. |
| [Verify Payment Method](actions/verify-payment-method.md) | POST | Verifies a payment method in Stax. |

### Refund Adjustment Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Statement Refunds and Adjustments](actions/get-statement-refunds-and-adjustments.md) | GET | Retrieves statement refunds and adjustments from Stax. |

### Statement Fees

| Action | Method | Description |
| --- | --- | --- |
| [Get Statement Fees](actions/get-statement-fees.md) | GET | Retrieves statement fee details from Stax. |

### Surcharge Review

| Action | Method | Description |
| --- | --- | --- |
| [Review Transaction Surcharge](actions/review-transaction-surcharge.md) | GET | Calculates surcharge details for a transaction in Stax. |

### Surcharging Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Statement Surcharging](actions/get-statement-surcharging.md) | GET | Retrieves statement surcharging totals from Stax. |

### Team Summary

| Action | Method | Description |
| --- | --- | --- |
| [Get Team Summary](actions/get-team-summary.md) | GET | Retrieves team summary statistics from Stax. |

### Team User

| Action | Method | Description |
| --- | --- | --- |
| [List Team Users](actions/list-team-users.md) | GET | Retrieves team users from Stax. |

### Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Capture Pre-Auth Transaction](actions/capture-pre-auth-transaction.md) | PUT | Captures a pre-authorized transaction in Stax. |
| [Get Related Transactions](actions/get-related-transactions.md) | GET | Retrieves related transactions for a transaction in Stax. |
| [Get Transaction](actions/get-transaction.md) | GET | Retrieves a transaction from Stax. |
| [Void or Refund Transaction](actions/void-or-refund-transaction.md) | POST | Voids or refunds a transaction in Stax. |

### Transactions

| Action | Method | Description |
| --- | --- | --- |
| [List Transactions](actions/list-transactions.md) | GET | Retrieves transactions from Stax. |

