# <img src="https://images.mindcloud.co/apps/icons/coin-gate_1775135549564.png" alt="CoinGate logo" width="28" height="28"> CoinGate: Universal API

Accept cryptocurrency payments, manage refunds and billing, run payouts, and inspect ledger activity in CoinGate.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/coinGate/latest
- **Category:** Commerce
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://coingate.com
- **Vendor API docs:** https://developer.coingate.com/reference/cryptocurrency-payment-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Orders](actions/list-orders.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/list-orders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Beneficiary

| Action | Method | Description |
| --- | --- | --- |
| [Create Beneficiary](actions/create-beneficiary.md) | POST | Creates a new beneficiary in CoinGate. |
| [Get Beneficiary](actions/get-beneficiary.md) | GET | Retrieves a beneficiary from CoinGate by ID. |
| [List Beneficiaries](actions/list-beneficiaries.md) | GET | Retrieves beneficiaries from your CoinGate account. |

### Billing Request

| Action | Method | Description |
| --- | --- | --- |
| [Create Billing Request](actions/create-billing-request.md) | POST | Creates a new billing request in CoinGate. |
| [Get Billing Request](actions/get-billing-request.md) | GET | Retrieves a billing request from CoinGate by ID. |
| [List Billing Requests](actions/list-billing-requests.md) | GET | Retrieves billing requests from your CoinGate account. |

### Blockchain Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Get Order Transaction](actions/get-order-transaction.md) | GET | Retrieves a blockchain transaction for a CoinGate order. |
| [List Order Transactions](actions/list-order-transactions.md) | GET | Retrieves blockchain transactions for a specific CoinGate order. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Billing Contact](actions/create-billing-contact.md) | POST | Creates a new billing contact in CoinGate. |
| [Get Billing Contact](actions/get-billing-contact.md) | GET | Retrieves a billing contact from CoinGate by ID. |
| [List Billing Contacts](actions/list-billing-contacts.md) | GET | Retrieves billing contacts from your CoinGate account. |

### Conversion

| Action | Method | Description |
| --- | --- | --- |
| [Create Conversion](actions/create-conversion.md) | POST | Creates a new currency conversion in CoinGate. |
| [Get Conversion](actions/get-conversion.md) | GET | Retrieves a currency conversion from CoinGate by ID. |
| [List Conversions](actions/list-conversions.md) | GET | Retrieves conversions from your CoinGate account. |

### Deposit Currency

| Action | Method | Description |
| --- | --- | --- |
| [List Supported Deposit Currencies](actions/list-supported-deposit-currencies.md) | GET | Retrieves supported deposit currencies and platforms from CoinGate. |

### Exchange Rates

| Action | Method | Description |
| --- | --- | --- |
| [List Conversion Rates](actions/list-conversion-rates.md) | GET | Retrieves supported conversion rates from CoinGate. |
| [List Exchange Rates](actions/list-exchange-rates.md) | GET | Retrieves current exchange rates from CoinGate. |

### General Ledger Transactions

| Action | Method | Description |
| --- | --- | --- |
| [Get Ledger Transaction](actions/get-ledger-transaction.md) | GET | Retrieves a ledger transaction from CoinGate by ID. |
| [List Ledger Transactions](actions/list-ledger-transactions.md) | GET | Retrieves ledger transactions from your CoinGate account. |

### Ledger Accounts

| Action | Method | Description |
| --- | --- | --- |
| [Get Ledger Account](actions/get-ledger-account.md) | GET | Retrieves a ledger account from CoinGate by ID. |
| [List Ledger Accounts](actions/list-ledger-accounts.md) | GET | Retrieves ledger accounts from your CoinGate account. |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [Checkout](actions/checkout.md) | POST | Creates a checkout session for an existing CoinGate order. |
| [Create Order](actions/create-order.md) | POST | Creates a new order in CoinGate. |
| [Get Order](actions/get-order.md) | GET | Retrieves an order from CoinGate by ID. |
| [List Orders](actions/list-orders.md) | GET | Retrieves orders from your CoinGate account. |

### Payment Currency

| Action | Method | Description |
| --- | --- | --- |
| [List Supported Payment Currencies](actions/list-supported-payment-currencies.md) | GET | Retrieves supported payment currencies from CoinGate. |

### Payout Currency

| Action | Method | Description |
| --- | --- | --- |
| [List Supported Payout Currencies](actions/list-supported-payout-currencies.md) | GET | Retrieves supported payout currencies and platforms from CoinGate. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Create Billing Product](actions/create-billing-product.md) | POST | Creates a new billing product in CoinGate. |
| [Get Billing Product](actions/get-billing-product.md) | GET | Retrieves a billing product from CoinGate by ID. |
| [List Billing Products](actions/list-billing-products.md) | GET | Retrieves billing products from your CoinGate account. |

### Refund Currency

| Action | Method | Description |
| --- | --- | --- |
| [List Refund Supported Currencies](actions/list-refund-supported-currencies.md) | GET | Retrieves supported refund currencies and platforms from CoinGate. |

### Refunds

| Action | Method | Description |
| --- | --- | --- |
| [Create Order Refund](actions/create-order-refund.md) | POST | Creates a refund for a specific CoinGate order. |
| [Get Order Refund](actions/get-order-refund.md) | GET | Retrieves a refund for a specific CoinGate order. |
| [List Order Refunds](actions/list-order-refunds.md) | GET | Retrieves refunds for a specific CoinGate order. |
| [List Refunds](actions/list-refunds.md) | GET | Retrieves all refunds from your CoinGate account. |

### Send Request

| Action | Method | Description |
| --- | --- | --- |
| [Create Send Request](actions/create-send-request.md) | POST | Creates a new send request in CoinGate. |
| [Get Send Request](actions/get-send-request.md) | GET | Retrieves a send request from CoinGate by ID. |
| [List Send Requests](actions/list-send-requests.md) | GET | Retrieves send requests from your CoinGate account. |

### Withdrawal

| Action | Method | Description |
| --- | --- | --- |
| [Get Withdrawal](actions/get-withdrawal.md) | GET | Retrieves a withdrawal from CoinGate by ID. |
| [List Withdrawals](actions/list-withdrawals.md) | GET | Retrieves withdrawals from your CoinGate account. |

