# Blockscout: Native API Reference

A consolidated summary of Blockscout's API configuration and 33 documented operations, with links to official documentation.

- **Official docs:** https://docs.blockscout.com/devs/apis
- **API base URL:** `https://api.blockscout.com`

## Authentication

### API Key

Provider-native Blockscout PRO API key. The PRO API accepts the key as an `apikey` query parameter or as an authorization header; this app maps the implicit MindCloud API key credential to the shared `apikey` query parameter for all actions.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.blockscout.com/devs/pro-api-responses-and-routes)

## API conventions

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 500 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (33 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Address Counters](actions/get-address-counters.md) | `GET /:chain_id/api/v2/addresses/:address_hash_param/counters` | [docs](https://docs.blockscout.com/api-reference/get-address-counters) |
| [Get Address Info](actions/get-address-info.md) | `GET /:chain_id/api/v2/addresses/:address_hash_param` | [docs](https://docs.blockscout.com/api-reference/get-address-info) |
| [Get Address Internal Transactions](actions/get-address-internal-transactions.md) | `GET /:chain_id/api/v2/addresses/:address_hash_param/internal-transactions` | [docs](https://docs.blockscout.com/api-reference/get-address-internal-transactions) |
| [Get Address Logs](actions/get-address-logs.md) | `GET /:chain_id/api/v2/addresses/:address_hash_param/logs` | [docs](https://docs.blockscout.com/api-reference/get-address-logs) |
| [Get Address Token Balances](actions/get-address-token-balances.md) | `GET /:chain_id/api/v2/addresses/:address_hash_param/tokens` | [docs](https://docs.blockscout.com/api-reference/get-all-tokens-balances-for-the-address) |
| [Get Address Token Transfers](actions/get-address-token-transfers.md) | `GET /:chain_id/api/v2/addresses/:address_hash_param/token-transfers` | [docs](https://docs.blockscout.com/api-reference/get-address-token-transfers) |
| [Get Address Transactions](actions/get-address-transactions.md) | `GET /:chain_id/api/v2/addresses/:address_hash_param/transactions` | [docs](https://docs.blockscout.com/api-reference/get-address-transactions) |
| [Get Addresses](actions/get-addresses.md) | `GET /:chain_id/api/v2/addresses` | [docs](https://docs.blockscout.com/api-reference/get-native-coin-holders-list) |
| [Get Block Info](actions/get-block-info.md) | `GET /:chain_id/api/v2/blocks/:block_hash_or_number_param` | [docs](https://docs.blockscout.com/api-reference/get-block-info) |
| [Get Block Transactions](actions/get-block-transactions.md) | `GET /:chain_id/api/v2/blocks/:block_hash_or_number_param/transactions` | [docs](https://docs.blockscout.com/api-reference/get-block-transactions) |
| [Get Blocks](actions/get-blocks.md) | `GET /:chain_id/api/v2/blocks` | [docs](https://docs.blockscout.com/api-reference/get-blocks) |
| [Get Indexing Status](actions/get-indexing-status.md) | `GET /:chain_id/api/v2/main-page/indexing-status` | [docs](https://docs.blockscout.com/api-reference/get-indexing-status) |
| [Get Internal Transactions](actions/get-internal-transactions.md) | `GET /:chain_id/api/v2/internal-transactions` | [docs](https://docs.blockscout.com/api-reference/get-internal-transactions) |
| [Get Main Page Blocks](actions/get-main-page-blocks.md) | `GET /:chain_id/api/v2/main-page/blocks` | [docs](https://docs.blockscout.com/api-reference/get-main-page-blocks) |
| [Get Main Page Transactions](actions/get-main-page-transactions.md) | `GET /:chain_id/api/v2/main-page/transactions` | [docs](https://docs.blockscout.com/api-reference/get-main-page-transactions) |
| [Get Market Chart](actions/get-market-chart.md) | `GET /:chain_id/api/v2/stats/charts/market` | [docs](https://docs.blockscout.com/api-reference/get-market-chart) |
| [Get Smart Contract](actions/get-smart-contract.md) | `GET /:chain_id/api/v2/smart-contracts/:address_hash_param` | [docs](https://docs.blockscout.com/api-reference/get-smart-contract) |
| [Get Smart Contracts](actions/get-smart-contracts.md) | `GET /:chain_id/api/v2/smart-contracts/` | [docs](https://docs.blockscout.com/api-reference/get-verified-smart-contracts) |
| [Get Stats Counters](actions/get-stats-counters.md) | `GET /:chain_id/api/v2/stats` | [docs](https://docs.blockscout.com/api-reference/get-stats-counters) |
| [Get Token Holders](actions/get-token-holders.md) | `GET /:chain_id/api/v2/tokens/:address_hash_param/holders` | [docs](https://docs.blockscout.com/api-reference/get-token-holders) |
| [Get Token Info](actions/get-token-info.md) | `GET /:chain_id/api/v2/tokens/:address_hash_param` | [docs](https://docs.blockscout.com/api-reference/get-token-info) |
| [Get Token Transfers](actions/get-token-transfers.md) | `GET /:chain_id/api/v2/token-transfers` | [docs](https://docs.blockscout.com/api-reference/get-token-transfers) |
| [Get Token Transfers by Token](actions/get-token-transfers-by-token.md) | `GET /:chain_id/api/v2/tokens/:address_hash_param/transfers` | [docs](https://docs.blockscout.com/api-reference/get-token-token-transfers) |
| [Get Tokens](actions/get-tokens.md) | `GET /:chain_id/api/v2/tokens/` | [docs](https://docs.blockscout.com/api-reference/get-tokens-list) |
| [Get Transaction Info](actions/get-transaction-info.md) | `GET /:chain_id/api/v2/transactions/:transaction_hash_param` | [docs](https://docs.blockscout.com/api-reference/get-transaction-info) |
| [Get Transaction Internal Transactions](actions/get-transaction-internal-transactions.md) | `GET /:chain_id/api/v2/transactions/:transaction_hash_param/internal-transactions` | [docs](https://docs.blockscout.com/api-reference/get-transaction-internal-transactions) |
| [Get Transaction Logs](actions/get-transaction-logs.md) | `GET /:chain_id/api/v2/transactions/:transaction_hash_param/logs` | [docs](https://docs.blockscout.com/api-reference/get-transaction-logs) |
| [Get Transaction State Changes](actions/get-transaction-state-changes.md) | `GET /:chain_id/api/v2/transactions/:transaction_hash_param/state-changes` | [docs](https://docs.blockscout.com/api-reference/get-transaction-state-changes) |
| [Get Transaction Summary](actions/get-transaction-summary.md) | `GET /:chain_id/api/v2/transactions/:transaction_hash_param/summary` | [docs](https://docs.blockscout.com/api-reference/get-human-readable-transaction-summary) |
| [Get Transaction Token Transfers](actions/get-transaction-token-transfers.md) | `GET /:chain_id/api/v2/transactions/:transaction_hash_param/token-transfers` | [docs](https://docs.blockscout.com/api-reference/get-transaction-token-transfers) |
| [Get Transactions](actions/get-transactions.md) | `GET /:chain_id/api/v2/transactions` | [docs](https://docs.blockscout.com/api-reference/get-transactions) |
| [Get Transactions Chart](actions/get-transactions-chart.md) | `GET /:chain_id/api/v2/stats/charts/transactions` | [docs](https://docs.blockscout.com/api-reference/get-transactions-chart) |
| [Search](actions/search.md) | `GET /:chain_id/api/v2/search` | [docs](https://docs.blockscout.com/api-reference/search) |
