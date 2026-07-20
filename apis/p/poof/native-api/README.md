# Poof: Native API Reference

A consolidated summary of Poof's API configuration and 18 documented operations, with links to official documentation.

- **Official docs:** https://docs.poof.io/reference/poof-api
- **API base URL:** `https://www.poof.io/api/v2`

## Authentication

### API Key

Use your Poof API key for authenticated API requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://www.poof.io/crosschain-json-rpc)

## API conventions

Responses from this API use JSON.

## Endpoints (18 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Balance](actions/check-balance.md) | `POST /balance` | [docs](https://docs.poof.io/reference/check_balance) |
| [Check Transfer Status](actions/check-transfer-status.md) | `POST https://www.poof.io/api/v2/transfer_status` | [docs](https://docs.poof.io/reference/ach-transfer-status) |
| [Create Wallet](actions/create-a-wallet.md) | `POST https://www.poof.io/api/v2/create_wallet` | [docs](https://docs.poof.io/reference/crypto-wallet-api) |
| [Create ACH Debit](actions/create-ach-debit.md) | `POST https://www.poof.io/api/v2/ach_debit` | [docs](https://docs.poof.io/reference/ach-debit-api) |
| [Create Charge](actions/create-charge.md) | `POST https://www.poof.io/api/v1/create_fiat_charge` | [docs](https://docs.poof.io/reference/createcharge) |
| [Create Checkout](actions/create-checkout.md) | `POST https://www.poof.io/api/v1/checkout` | [docs](https://docs.poof.io/reference/poof-checkout) |
| [Create Deposit Address](actions/create-deposit-address.md) | `POST https://www.poof.io/api/v2/create_charge` | [docs](https://docs.poof.io/reference/create_address) |
| [Create Invoice](actions/create-invoice.md) | `POST https://www.poof.io/api/v1/create_fiat_invoice` | [docs](https://docs.poof.io/reference/createinvoice) |
| [Create Payment Link](actions/create-payment-link.md) | `POST /create_invoice` | [docs](https://docs.poof.io/reference/createinvoice-1) |
| [Fetch All Transactions](actions/fetch-all-transactions.md) | `POST https://www.poof.io/api/v1/fetch_transactions` | [docs](https://docs.poof.io/reference/fetch-transaction-list) |
| [Fetch Gas Price](actions/fetch-gas-price.md) | `POST /gas_price` | [docs](https://docs.poof.io/reference/fetchgasprice) |
| [Fetch Price](actions/fetch-price.md) | `POST /price` | [docs](https://docs.poof.io/reference/fetchprice) |
| [Fetch Product](actions/fetch-product.md) | `POST /fetch_product` | [docs](https://docs.poof.io/reference/fetchproduct) |
| [Fetch Smart Contracts](actions/fetch-smart-contracts.md) | `POST /gas_price` | [docs](https://docs.poof.io/reference/fetchsmartcontracts) |
| [Fetch Transaction](actions/fetch-transaction.md) | `POST https://www.poof.io/api/v1/transaction` | [docs](https://docs.poof.io/reference/fetch-transaction) |
| [Receive Notifications](actions/receive-notifications.md) | `POST https://www.poof.io/api/v1/create_webhook` | [docs](https://docs.poof.io/reference/notifications-api) |
| [Send Transaction](actions/send-transaction.md) | `POST /payouts` | [docs](https://docs.poof.io/reference/sendtransaction) |
| [Transaction Query](actions/transaction-query.md) | `POST /transaction_query` | [docs](https://docs.poof.io/reference/transaction_query) |
