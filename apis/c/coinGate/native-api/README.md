# CoinGate: Native API Reference

A consolidated summary of CoinGate's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://developer.coingate.com/reference/cryptocurrency-payment-api
- **API base URL:** `https://api.coingate.com/api/v2`

## Authentication

### API Key

Connect CoinGate with a merchant access token generated from the CoinGate dashboard.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developer.coingate.com/reference/api-authentication)

## Pagination

Use `per_page` in the query string to set the page size (default 50). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Checkout](actions/checkout.md) | `POST /orders/:id/checkout` | [docs](https://developer.coingate.com/reference/checkout) |
| [Create Beneficiary](actions/create-beneficiary.md) | `POST /beneficiaries` | [docs](https://developer.coingate.com/reference/create-beneficiary) |
| [Create Billing Contact](actions/create-billing-contact.md) | `POST /billing/contacts` | [docs](https://developer.coingate.com/reference/create-billing-contact) |
| [Create Billing Product](actions/create-billing-product.md) | `POST /billing/products` | [docs](https://developer.coingate.com/reference/create-billing-product) |
| [Create Billing Request](actions/create-billing-request.md) | `POST /billing/requests` | [docs](https://developer.coingate.com/reference/create-billing-request) |
| [Create Conversion](actions/create-conversion.md) | `POST /ledger/conversions` | [docs](https://developer.coingate.com/reference/create-conversion) |
| [Create Order](actions/create-order.md) | `POST /orders` | [docs](https://developer.coingate.com/reference/create-order) |
| [Create Order Refund](actions/create-order-refund.md) | `POST /orders/:order_id/refunds` | [docs](https://developer.coingate.com/reference/create-refund) |
| [Create Send Request](actions/create-send-request.md) | `POST /send_requests` | [docs](https://developer.coingate.com/reference/create-send) |
| [Get Beneficiary](actions/get-beneficiary.md) | `GET /beneficiaries/:id` | [docs](https://developer.coingate.com/reference/get-beneficiary) |
| [Get Billing Contact](actions/get-billing-contact.md) | `GET /billing/contacts/:id` | [docs](https://developer.coingate.com/reference/get-billing-contact) |
| [Get Billing Product](actions/get-billing-product.md) | `GET /billing/products/:id` | [docs](https://developer.coingate.com/reference/get-billing-product) |
| [Get Billing Request](actions/get-billing-request.md) | `GET /billing/requests/:id` | [docs](https://developer.coingate.com/reference/get-billing-request) |
| [Get Conversion](actions/get-conversion.md) | `GET /ledger/conversions/:id` | [docs](https://developer.coingate.com/reference/get-conversion) |
| [Get Ledger Account](actions/get-ledger-account.md) | `GET /ledger/accounts/:id` | [docs](https://developer.coingate.com/reference/get-ledger-account) |
| [Get Ledger Transaction](actions/get-ledger-transaction.md) | `GET /ledger/transactions/:id` | [docs](https://developer.coingate.com/reference/get-transaction) |
| [Get Order](actions/get-order.md) | `GET /orders/:id` | [docs](https://developer.coingate.com/reference/get-order) |
| [Get Order Refund](actions/get-order-refund.md) | `GET /orders/:order_id/refunds/:id` | [docs](https://developer.coingate.com/reference/get-order-refund) |
| [Get Order Transaction](actions/get-order-transaction.md) | `GET /orders/:order_id/blockchain_transactions/:id` | [docs](https://developer.coingate.com/reference/get-order-transaction) |
| [Get Send Request](actions/get-send-request.md) | `GET /send_requests/:id` | [docs](https://developer.coingate.com/reference/get-send) |
| [Get Withdrawal](actions/get-withdrawal.md) | `GET /withdrawals/:id` | [docs](https://developer.coingate.com/reference/get-withdrawal) |
| [List Beneficiaries](actions/list-beneficiaries.md) | `GET /beneficiaries` | [docs](https://developer.coingate.com/reference/list-beneficiaries) |
| [List Billing Contacts](actions/list-billing-contacts.md) | `GET /billing/contacts` | [docs](https://developer.coingate.com/reference/list-billing-contacts) |
| [List Billing Products](actions/list-billing-products.md) | `GET /billing/products` | [docs](https://developer.coingate.com/reference/list-billing-products) |
| [List Billing Requests](actions/list-billing-requests.md) | `GET /billing/requests` | [docs](https://developer.coingate.com/reference/list-billing-requests) |
| [List Conversion Rates](actions/list-conversion-rates.md) | `GET /ledger/conversions/rates` | [docs](https://developer.coingate.com/reference/conversion-rates) |
| [List Conversions](actions/list-conversions.md) | `GET /ledger/conversions` | [docs](https://developer.coingate.com/reference/list-conversions) |
| [List Exchange Rates](actions/list-exchange-rates.md) | `GET /rates` | [docs](https://developer.coingate.com/reference/list-rates) |
| [List Ledger Accounts](actions/list-ledger-accounts.md) | `GET /ledger/accounts` | [docs](https://developer.coingate.com/reference/ledger-accounts) |
| [List Ledger Transactions](actions/list-ledger-transactions.md) | `GET /ledger/transactions` | [docs](https://developer.coingate.com/reference/list-transactions) |
| [List Order Refunds](actions/list-order-refunds.md) | `GET /orders/:order_id/refunds` | [docs](https://developer.coingate.com/reference/get-refund) |
| [List Order Transactions](actions/list-order-transactions.md) | `GET /orders/:order_id/blockchain_transactions` | [docs](https://developer.coingate.com/reference/get-order-transactions) |
| [List Orders](actions/list-orders.md) | `GET /orders` | [docs](https://developer.coingate.com/reference/list-orders) |
| [List Refund Supported Currencies](actions/list-refund-supported-currencies.md) | `GET /refunds/supported-currencies` | [docs](https://developer.coingate.com/reference/refund-supported-currencies) |
| [List Refunds](actions/list-refunds.md) | `GET /refunds` | [docs](https://developer.coingate.com/reference/get-refunds) |
| [List Send Requests](actions/list-send-requests.md) | `GET /send_requests` | [docs](https://developer.coingate.com/reference/list-send) |
| [List Supported Deposit Currencies](actions/list-supported-deposit-currencies.md) | `GET /deposits/supported-currencies` | [docs](https://developer.coingate.com/reference/deposit-supported-currencies) |
| [List Supported Payment Currencies](actions/list-supported-payment-currencies.md) | `GET /currencies` | [docs](https://developer.coingate.com/reference/currencies) |
| [List Supported Payout Currencies](actions/list-supported-payout-currencies.md) | `GET /send_requests/supported-currencies` | [docs](https://developer.coingate.com/reference/supported-payout-currencies-and-crypto-platforms) |
| [List Withdrawals](actions/list-withdrawals.md) | `GET /withdrawals` | [docs](https://developer.coingate.com/reference/get-withdrawals) |
