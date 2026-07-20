# <img src="https://images.mindcloud.co/apps/icons/global-payments-1_1776102825115.png" alt="Global Payments WebPay logo" width="28" height="28"> Global Payments WebPay: Universal API

Global Payments WebPay wrapper for REST API operations across transactions, payment methods, payers, disputes, settlement reporting, merchants, accounts, links, orders, funds, and transfers.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/globalPaymentsWebPay/latest
- **Category:** Commerce / Payments & Billing
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.globalpayments.com/
- **Vendor API docs:** https://developer.globalpayments.com/docs/integration-options/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Accounts](actions/list-accounts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/globalPaymentsWebPay/latest/actions/list-accounts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Checkouts

| Action | Method | Description |
| --- | --- | --- |
| [Create Link](actions/create-link.md) | POST | Creates a payment link in Global Payments WebPay. |
| [Get Link](actions/get-link.md) | GET | Retrieves a payment link from Global Payments WebPay. |
| [List Links](actions/list-links.md) | GET | Retrieves payment links from Global Payments WebPay. |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Get Merchant](actions/get-merchant.md) | GET | Retrieves a merchant from Global Payments WebPay. |
| [List Merchants](actions/list-merchants.md) | GET | Retrieves merchants from Global Payments WebPay. |

### CRM Accounts

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves an account from Global Payments WebPay. |
| [List Accounts](actions/list-accounts.md) | GET | Retrieves accounts from Global Payments WebPay. |
| [Update Account](actions/update-account.md) | PUT | Updates an account in Global Payments WebPay. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Create Payer](actions/create-payer.md) | POST | Creates a payer in Global Payments WebPay. |
| [Delete Payer](actions/delete-payer.md) | DELETE | Deletes a payer from Global Payments WebPay. |
| [Get Payer](actions/get-payer.md) | GET | Retrieves a payer from Global Payments WebPay. |
| [List Payers](actions/list-payers.md) | GET | Retrieves payers from Global Payments WebPay. |
| [Update Payer](actions/update-payer.md) | PUT | Updates a payer in Global Payments WebPay. |

### Disputes

| Action | Method | Description |
| --- | --- | --- |
| [Accept Dispute](actions/accept-dispute.md) | PUT | Updates a dispute by accepting it in Global Payments WebPay. |
| [Challenge Dispute](actions/challenge-dispute.md) | PUT | Updates a dispute by challenging it in Global Payments WebPay. |
| [Get Dispute](actions/get-dispute.md) | GET | Retrieves a dispute from Global Payments WebPay. |
| [List Disputes](actions/list-disputes.md) | GET | Retrieves disputes from Global Payments WebPay. |

### Payment Methods

| Action | Method | Description |
| --- | --- | --- |
| [Create Payment Method](actions/create-payment-method.md) | POST | Creates a payment method in Global Payments WebPay. |
| [Create Verification](actions/create-verification.md) | POST | Creates a payment method verification in Global Payments WebPay. |
| [Delete Payment Method](actions/delete-payment-method.md) | DELETE | Deletes a payment method from Global Payments WebPay. |
| [Detokenize Payment Method](actions/detokenize-payment-method.md) | GET | Retrieves detokenized payment method details from Global Payments WebPay. |
| [Get Payment Method](actions/get-payment-method.md) | GET | Retrieves a payment method from Global Payments WebPay. |
| [List Payment Methods](actions/list-payment-methods.md) | GET | Retrieves payment methods from Global Payments WebPay. |
| [Search Payment Methods](actions/search-payment-methods.md) | GET | Finds payment methods in Global Payments WebPay by search criteria. |
| [Update Payment Method](actions/update-payment-method.md) | PUT | Updates a payment method in Global Payments WebPay. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Transaction Summary Report](actions/get-transaction-summary-report.md) | GET | Retrieves a transaction summary report from Global Payments WebPay. |

### Settlements

| Action | Method | Description |
| --- | --- | --- |
| [Get Settlement Deposit](actions/get-settlement-deposit.md) | GET | Retrieves a settlement deposit from Global Payments WebPay. |
| [List Settled Disputes](actions/list-settled-disputes.md) | GET | Retrieves settled disputes from Global Payments WebPay. |
| [List Settled Transactions](actions/list-settled-transactions.md) | GET | Retrieves settled transactions from Global Payments WebPay. |
| [List Settlement Deposits](actions/list-settlement-deposits.md) | GET | Retrieves settlement deposits from Global Payments WebPay. |

### Transactions

| Action | Method | Description |
| --- | --- | --- |
| [Adjust Transaction](actions/adjust-transaction.md) | PUT | Updates a transaction by adjusting it in Global Payments WebPay. |
| [Capture Sale Transaction](actions/capture-sale-transaction.md) | PUT | Updates a sale transaction by capturing it in Global Payments WebPay. |
| [Confirm Transaction](actions/confirm-transaction.md) | PUT | Updates a transaction by confirming it in Global Payments WebPay. |
| [Create Sale Or Refund Transaction](actions/create-sale-or-refund-transaction.md) | POST | Creates a sale or refund transaction in Global Payments WebPay. |
| [Get Transaction](actions/get-transaction.md) | GET | Retrieves a transaction from Global Payments WebPay. |
| [Increment Transaction](actions/increment-transaction.md) | PUT | Updates a transaction by incrementing it in Global Payments WebPay. |
| [List Transactions](actions/list-transactions.md) | GET | Retrieves transactions from Global Payments WebPay. |
| [Reauthorize Transaction](actions/reauthorize-transaction.md) | PUT | Updates a transaction by reauthorizing it in Global Payments WebPay. |
| [Refund Sale Transaction](actions/refund-sale-transaction.md) | POST | Creates a refund for a sale transaction in Global Payments WebPay. |
| [Reverse Transaction](actions/reverse-transaction.md) | PUT | Updates a transaction by reversing it in Global Payments WebPay. |

