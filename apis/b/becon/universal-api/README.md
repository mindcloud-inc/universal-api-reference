# <img src="https://images.mindcloud.co/apps/icons/becon_1775842486579.png" alt="Becon logo" width="28" height="28"> Becon: Universal API

Use the Becon crypto payment API to inspect balances, transactions, stores, addresses, currencies, exchange rates, and sandbox test payments.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/becon/latest
- **Category:** Commerce / Payments & Billing
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://bcon.global/
- **Vendor API docs:** https://bcon.global/integrations/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Currencies](actions/list-currencies.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/becon/latest/actions/list-currencies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Addresses

| Action | Method | Description |
| --- | --- | --- |
| [Create Binance Address](actions/create-binance-address.md) | POST | Creates a new Binance payment address in Becon. |
| [Create Bitcoin Address](actions/create-bitcoin-address.md) | POST | Creates a new Bitcoin payment address in Becon. |
| [Create Ethereum Address](actions/create-ethereum-address.md) | POST | Creates a new Ethereum payment address in Becon. |
| [Create New Address](actions/create-new-address.md) | POST | Creates a new payment address in Becon. |
| [Create Tron Address](actions/create-tron-address.md) | POST | Creates a new Tron payment address in Becon. |
| [Get Balance](actions/get-balance.md) | GET | Retrieves BTC wallet balances from Becon by address. |
| [Get Current Address](actions/get-current-address.md) | GET | Retrieves the latest payment address from Becon. |
| [Get Current Binance Address](actions/get-current-binance-address.md) | GET | Retrieves the latest Binance payment address from Becon. |
| [Get Current Bitcoin Address](actions/get-current-bitcoin-address.md) | GET | Retrieves the latest Bitcoin payment address from Becon. |
| [Get Current Ethereum Address](actions/get-current-ethereum-address.md) | GET | Retrieves the latest Ethereum payment address from Becon. |
| [Get Current Tron Address](actions/get-current-tron-address.md) | GET | Retrieves the latest Tron payment address from Becon. |

### Transactions

| Action | Method | Description |
| --- | --- | --- |
| [Create BNB Test Payment](actions/create-bnb-test-payment.md) | POST | Creates a BNB test payment in Becon. |
| [Create BTC Test Payment](actions/create-btc-test-payment.md) | POST | Creates a Bitcoin test payment in Becon. |
| [Create Test Payment](actions/create-test-payment.md) | POST | Creates a test payment in Becon. |
| [Get Transaction](actions/get-transaction.md) | GET | Retrieves a transaction from Becon by ID. |
| [List Transaction History](actions/list-transaction-history.md) | GET | Retrieves BTC transaction history from Becon by address. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get BNB to EUR Rate](actions/get-bnb-to-eur-rate.md) | GET | Retrieves the BNB-to-EUR rate from Becon. |
| [Get BTC to EUR Rate](actions/get-btc-to-eur-rate.md) | GET | Retrieves the BTC-to-EUR rate from Becon. |
| [Get Currency Rate](actions/get-currency-rate.md) | GET | Retrieves a cryptocurrency-to-fiat exchange rate from Becon. |
| [Get ETH to USD Rate](actions/get-eth-to-usd-rate.md) | GET | Retrieves the ETH-to-USD rate from Becon. |
| [Get Store Info](actions/get-store-info.md) | GET | Retrieves a specific store record from Becon. |
| [Get USDT to USD Rate](actions/get-usdt-to-usd-rate.md) | GET | Retrieves the USDT-to-USD rate from Becon. |
| [List Currencies](actions/list-currencies.md) | GET | Retrieves available currencies and chains from Becon. |
| [List Stores](actions/list-stores.md) | GET | Retrieves created store records from Becon. |

