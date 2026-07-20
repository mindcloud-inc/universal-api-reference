# <img src="https://images.mindcloud.co/apps/icons/poof_1774983240301.png" alt="Poof logo" width="28" height="28"> Poof: Universal API

Create wallets, fetch crypto prices, and manage crypto payments

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/poof/latest
- **Category:** Commerce / Payments & Billing
- **Actions:** 18
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.poof.io
- **Vendor API docs:** https://docs.poof.io/reference/poof-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Fetch Price](actions/fetch-price.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/poof/latest/actions/fetch-price?connectionId=$CONNECTION_ID&crypto=bitcoin" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (18)

### Ach Debit

| Action | Method | Description |
| --- | --- | --- |
| [Create ACH Debit](actions/create-ach-debit.md) | POST | Creates a new ACH debit in Poof. |

### Balance

| Action | Method | Description |
| --- | --- | --- |
| [Check Balance](actions/check-balance.md) | GET | Retrieves wallet balance details from Poof. |

### Charge

| Action | Method | Description |
| --- | --- | --- |
| [Create Charge](actions/create-charge.md) | POST | Creates a new fiat charge in Poof. |

### Checkout

| Action | Method | Description |
| --- | --- | --- |
| [Create Checkout](actions/create-checkout.md) | POST | Creates a new checkout in Poof. |

### Deposit Address

| Action | Method | Description |
| --- | --- | --- |
| [Create Deposit Address](actions/create-deposit-address.md) | POST | Creates a new deposit address in Poof. |

### Gas Price

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Gas Price](actions/fetch-gas-price.md) | GET | Retrieves current gas price data from Poof. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Create Invoice](actions/create-invoice.md) | POST | Creates a new fiat invoice in Poof. |

### Payment Link

| Action | Method | Description |
| --- | --- | --- |
| [Create Payment Link](actions/create-payment-link.md) | POST | Creates a new payment link in Poof. |

### Price

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Price](actions/fetch-price.md) | GET | Retrieves a price quote from Poof. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Product](actions/fetch-product.md) | GET | Retrieves product details from the Poof API. |

### Smart Contract

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Smart Contracts](actions/fetch-smart-contracts.md) | GET |  |

### Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Transaction](actions/fetch-transaction.md) | GET | Retrieves a transaction record from Poof. |
| [Send Transaction](actions/send-transaction.md) | POST | Creates a new payout transaction in Poof. |
| [Transaction Query](actions/transaction-query.md) | GET | Retrieves transaction query results from Poof. |

### Transactions

| Action | Method | Description |
| --- | --- | --- |
| [Fetch All Transactions](actions/fetch-all-transactions.md) | GET | Retrieves all transaction records from Poof. |

### Transfer Status

| Action | Method | Description |
| --- | --- | --- |
| [Check Transfer Status](actions/check-transfer-status.md) | GET | Retrieves ACH transfer status from Poof. |

### Wallet

| Action | Method | Description |
| --- | --- | --- |
| [Create Wallet](actions/create-a-wallet.md) | POST | Creates a new wallet in Poof. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Receive Notifications](actions/receive-notifications.md) | POST | Creates a new webhook in Poof. |

