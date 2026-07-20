# Global Payments WebPay: Native API Reference

A consolidated summary of Global Payments WebPay's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://developer.globalpayments.com/docs/integration-options/api
- **API base URL:** `https://apis.globalpay.com/ucp`

## Authentication

### App Key

Global Payments app key used with an App ID to create short-lived bearer access tokens.

### Credentials

- **API Key:** `apiKey` · required
- **App ID:** `appId` · required · The Global Payments app ID used when creating access tokens.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developer.globalpayments.com/docs/getting-started/generate-token)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `page_size` in the query string to set the page size (default 25; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Accept Dispute](actions/accept-dispute.md) | `POST /disputes/{id}/acceptance` | [docs](https://developer.globalpayments.com/api/disputes) |
| [Adjust Transaction](actions/adjust-transaction.md) | `POST /transactions/{id}/adjustment` | [docs](https://developer.globalpayments.com/api/transactions) |
| [Capture Sale Transaction](actions/capture-sale-transaction.md) | `POST /transactions/{id}/capture` | [docs](https://developer.globalpayments.com/api/transactions) |
| [Challenge Dispute](actions/challenge-dispute.md) | `POST /disputes/{id}/challenge` | [docs](https://developer.globalpayments.com/api/disputes) |
| [Confirm Transaction](actions/confirm-transaction.md) | `POST /transactions/{id}/confirmation` | [docs](https://developer.globalpayments.com/api/transactions) |
| [Create Link](actions/create-link.md) | `POST /links` | [docs](https://developer.globalpayments.com/api/links) |
| [Create Payer](actions/create-payer.md) | `POST /payers` | [docs](https://developer.globalpayments.com/api/payers) |
| [Create Payment Method](actions/create-payment-method.md) | `POST /payment-methods` | [docs](https://developer.globalpayments.com/api/payment-methods-tokenization) |
| [Create Sale Or Refund Transaction](actions/create-sale-or-refund-transaction.md) | `POST /transactions` | [docs](https://developer.globalpayments.com/api/transactions) |
| [Create Verification](actions/create-verification.md) | `POST /verifications` | [docs](https://developer.globalpayments.com/api/verifications) |
| [Delete Payer](actions/delete-payer.md) | `DELETE /payers/{id}` | [docs](https://developer.globalpayments.com/api/payers) |
| [Delete Payment Method](actions/delete-payment-method.md) | `DELETE /payment-methods/{id}` | [docs](https://developer.globalpayments.com/api/payment-methods-tokenization) |
| [Detokenize Payment Method](actions/detokenize-payment-method.md) | `POST /payment-methods/{id}/detokenize` | [docs](https://developer.globalpayments.com/api/payment-methods-tokenization) |
| [Get Account](actions/get-account.md) | `GET /accounts/{id}` | [docs](https://developer.globalpayments.com/api/accounts) |
| [Get Dispute](actions/get-dispute.md) | `GET /disputes/{id}` | [docs](https://developer.globalpayments.com/api/disputes) |
| [Get Link](actions/get-link.md) | `GET /links/{id}` | [docs](https://developer.globalpayments.com/api/links) |
| [Get Merchant](actions/get-merchant.md) | `GET /merchants/{id}` | [docs](https://developer.globalpayments.com/api/merchants) |
| [Get Payer](actions/get-payer.md) | `GET /payers/{id}` | [docs](https://developer.globalpayments.com/api/payers) |
| [Get Payment Method](actions/get-payment-method.md) | `GET /payment-methods/{id}` | [docs](https://developer.globalpayments.com/api/payment-methods-tokenization) |
| [Get Settlement Deposit](actions/get-settlement-deposit.md) | `GET /settlement/deposits/{id}` | [docs](https://developer.globalpayments.com/api/settlement-reporting) |
| [Get Transaction](actions/get-transaction.md) | `GET /transactions/{id}` | [docs](https://developer.globalpayments.com/api/transactions) |
| [Get Transaction Summary Report](actions/get-transaction-summary-report.md) | `GET /reports` | [docs](https://developer.globalpayments.com/api/reports) |
| [Increment Transaction](actions/increment-transaction.md) | `POST /transactions/{id}/incremental` | [docs](https://developer.globalpayments.com/api/transactions) |
| [List Accounts](actions/list-accounts.md) | `GET /accounts` | [docs](https://developer.globalpayments.com/api/accounts) |
| [List Disputes](actions/list-disputes.md) | `GET /disputes` | [docs](https://developer.globalpayments.com/api/disputes) |
| [List Links](actions/list-links.md) | `GET /links` | [docs](https://developer.globalpayments.com/api/links) |
| [List Merchants](actions/list-merchants.md) | `GET /merchants` | [docs](https://developer.globalpayments.com/api/merchants) |
| [List Payers](actions/list-payers.md) | `GET /payers` | [docs](https://developer.globalpayments.com/api/payers) |
| [List Payment Methods](actions/list-payment-methods.md) | `GET /payment-methods` | [docs](https://developer.globalpayments.com/api/payment-methods-tokenization) |
| [List Settled Disputes](actions/list-settled-disputes.md) | `GET /settlement/disputes` | [docs](https://developer.globalpayments.com/api/settlement-reporting) |
| [List Settled Transactions](actions/list-settled-transactions.md) | `GET /settlement/transactions` | [docs](https://developer.globalpayments.com/api/settlement-reporting) |
| [List Settlement Deposits](actions/list-settlement-deposits.md) | `GET /settlement/deposits` | [docs](https://developer.globalpayments.com/api/settlement-reporting) |
| [List Transactions](actions/list-transactions.md) | `GET /transactions` | [docs](https://developer.globalpayments.com/api/transactions) |
| [Reauthorize Transaction](actions/reauthorize-transaction.md) | `POST /transactions/{id}/reauthorization` | [docs](https://developer.globalpayments.com/api/transactions) |
| [Refund Sale Transaction](actions/refund-sale-transaction.md) | `POST /transactions/{id}/refund` | [docs](https://developer.globalpayments.com/api/transactions) |
| [Reverse Transaction](actions/reverse-transaction.md) | `POST /transactions/{id}/reversal` | [docs](https://developer.globalpayments.com/api/transactions) |
| [Search Payment Methods](actions/search-payment-methods.md) | `POST /payment-methods/search` | [docs](https://developer.globalpayments.com/api/payment-methods-tokenization) |
| [Update Account](actions/update-account.md) | `PATCH /accounts/{id}` | [docs](https://developer.globalpayments.com/api/accounts) |
| [Update Payer](actions/update-payer.md) | `PATCH /payers/{id}` | [docs](https://developer.globalpayments.com/api/payers) |
| [Update Payment Method](actions/update-payment-method.md) | `PATCH /payment-methods/{id}` | [docs](https://developer.globalpayments.com/api/payment-methods-tokenization) |
