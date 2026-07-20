# Becon: Native API Reference

A consolidated summary of Becon's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://bcon.global/integrations/api/
- **API base URL:** `https://external-api.bcon.global/api`

## Authentication

### API Key

Authenticate with a Becon store API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://bcon.global/integrations/api/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Binance Address](actions/create-binance-address.md) | `POST /v2/address` | [docs](https://bcon.global/integrations/api/) |
| [Create Bitcoin Address](actions/create-bitcoin-address.md) | `POST /v2/address` | [docs](https://bcon.global/integrations/api/) |
| [Create BNB Test Payment](actions/create-bnb-test-payment.md) | `POST /v1/test` | [docs](https://bcon.global/integrations/api/) |
| [Create BTC Test Payment](actions/create-btc-test-payment.md) | `POST /v1/test` | [docs](https://bcon.global/integrations/api/) |
| [Create Ethereum Address](actions/create-ethereum-address.md) | `POST /v2/address` | [docs](https://bcon.global/integrations/api/) |
| [Create New Address](actions/create-new-address.md) | `POST /v2/address` | [docs](https://bcon.global/integrations/api/) |
| [Create Test Payment](actions/create-test-payment.md) | `POST /v1/test` | [docs](https://bcon.global/integrations/api/) |
| [Create Tron Address](actions/create-tron-address.md) | `POST /v2/address` | [docs](https://bcon.global/integrations/api/) |
| [Get Balance](actions/get-balance.md) | `GET /v1/user/balance` | [docs](https://bcon.global/integrations/api/) |
| [Get BNB to EUR Rate](actions/get-bnb-to-eur-rate.md) | `GET /v1/currencies/:cryptoCurrencyName` | [docs](https://bcon.global/integrations/api/) |
| [Get BTC to EUR Rate](actions/get-btc-to-eur-rate.md) | `GET /v1/currencies/:cryptoCurrencyName` | [docs](https://bcon.global/integrations/api/) |
| [Get Currency Rate](actions/get-currency-rate.md) | `GET /v1/currencies/:cryptoCurrencyName` | [docs](https://bcon.global/integrations/api/) |
| [Get Current Address](actions/get-current-address.md) | `POST /v2/address?reset=1` | [docs](https://bcon.global/integrations/api/) |
| [Get Current Binance Address](actions/get-current-binance-address.md) | `POST /v2/address?reset=1` | [docs](https://bcon.global/integrations/api/) |
| [Get Current Bitcoin Address](actions/get-current-bitcoin-address.md) | `POST /v2/address?reset=1` | [docs](https://bcon.global/integrations/api/) |
| [Get Current Ethereum Address](actions/get-current-ethereum-address.md) | `POST /v2/address?reset=1` | [docs](https://bcon.global/integrations/api/) |
| [Get Current Tron Address](actions/get-current-tron-address.md) | `POST /v2/address?reset=1` | [docs](https://bcon.global/integrations/api/) |
| [Get ETH to USD Rate](actions/get-eth-to-usd-rate.md) | `GET /v1/currencies/:cryptoCurrencyName` | [docs](https://bcon.global/integrations/api/) |
| [Get Store Info](actions/get-store-info.md) | `GET /v1/stores/get_store` | [docs](https://bcon.global/integrations/api/) |
| [Get Transaction](actions/get-transaction.md) | `GET /v1/transactions/:txid` | [docs](https://bcon.global/integrations/api/) |
| [Get USDT to USD Rate](actions/get-usdt-to-usd-rate.md) | `GET /v1/currencies/:cryptoCurrencyName` | [docs](https://bcon.global/integrations/api/) |
| [List Currencies](actions/list-currencies.md) | `GET /v1/currencies` | [docs](https://bcon.global/integrations/api/) |
| [List Stores](actions/list-stores.md) | `GET /v1/stores` | [docs](https://bcon.global/integrations/api/) |
| [List Transaction History](actions/list-transaction-history.md) | `GET /v1/user/history` | [docs](https://bcon.global/integrations/api/) |
