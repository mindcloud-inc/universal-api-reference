# Mempool: Native API Reference

A consolidated summary of Mempool's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://mempool.space/docs/api/rest
- **API base URL:** `https://mempool.space/api`

## Authentication

### Public Mempool API

Mempool public read endpoints used by this app do not require authentication.

This API does not require request authentication.

[Official authentication documentation](https://mempool.space/docs/api/rest)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Address Summary](actions/get-address-summary.md) | `GET /address/[:address]` | [docs](https://mempool.space/docs/api/rest) |
| [Get Bitcoin Prices](actions/get-bitcoin-prices.md) | `GET /v1/prices` | [docs](https://mempool.space/docs/api/rest) |
| [Get Block](actions/get-block.md) | `GET /block/[:hash]` | [docs](https://mempool.space/docs/api/rest) |
| [Get Block Header](actions/get-block-header.md) | `GET /block/[:hash]/header` | [docs](https://mempool.space/docs/api/rest) |
| [Get Block Status](actions/get-block-status.md) | `GET /block/[:hash]/status` | [docs](https://mempool.space/docs/api/rest) |
| [Get Block Transaction ID at Index](actions/get-block-transaction-id-at-index.md) | `GET /block/[:hash]/txid/[:index]` | [docs](https://mempool.space/docs/api/rest) |
| [Get Difficulty Adjustment](actions/get-difficulty-adjustment.md) | `GET /v1/difficulty-adjustment` | [docs](https://mempool.space/docs/api/rest) |
| [Get Mempool Summary](actions/get-mempool-summary.md) | `GET /mempool` | [docs](https://mempool.space/docs/api/rest) |
| [Get Mining Hashrate](actions/get-mining-hashrate.md) | `GET /v1/mining/hashrate/[:time_period]` | [docs](https://mempool.space/docs/api/rest) |
| [Get Mining Pool](actions/get-mining-pool.md) | `GET /v1/mining/pool/[:slug]` | [docs](https://mempool.space/docs/api/rest) |
| [Get Recommended Fees](actions/get-recommended-fees.md) | `GET /v1/fees/recommended` | [docs](https://mempool.space/docs/api/rest) |
| [Get Tip Hash](actions/get-tip-hash.md) | `GET /blocks/tip/hash` | [docs](https://mempool.space/docs/api/rest) |
| [Get Tip Height](actions/get-tip-height.md) | `GET /blocks/tip/height` | [docs](https://mempool.space/docs/api/rest) |
| [Get Transaction](actions/get-transaction.md) | `GET /tx/[:txid]` | [docs](https://mempool.space/docs/api/rest) |
| [Get Transaction Hex](actions/get-transaction-hex.md) | `GET /tx/[:txid]/hex` | [docs](https://mempool.space/docs/api/rest) |
| [Get Transaction Status](actions/get-transaction-status.md) | `GET /tx/[:txid]/status` | [docs](https://mempool.space/docs/api/rest) |
| [List Address Mempool Transactions](actions/list-address-mempool-transactions.md) | `GET /address/[:address]/txs/mempool` | [docs](https://mempool.space/docs/api/rest) |
| [List Address Transactions](actions/list-address-transactions.md) | `GET /address/[:address]/txs` | [docs](https://mempool.space/docs/api/rest) |
| [List Block Transaction IDs](actions/list-block-transaction-ids.md) | `GET /block/[:hash]/txids` | [docs](https://mempool.space/docs/api/rest) |
| [List Block Transactions](actions/list-block-transactions.md) | `GET /block/[:hash]/txs/[:start_index]` | [docs](https://mempool.space/docs/api/rest) |
| [List Mempool Transaction IDs](actions/list-mempool-transaction-ids.md) | `GET /mempool/txids` | [docs](https://mempool.space/docs/api/rest) |
| [List Mining Pools](actions/list-mining-pools.md) | `GET /v1/mining/pools/[:time_period]` | [docs](https://mempool.space/docs/api/rest) |
| [List Recent Blocks](actions/list-recent-blocks.md) | `GET /v1/blocks` | [docs](https://mempool.space/docs/api/rest) |
| [List Recent Mempool Transactions](actions/list-recent-mempool-transactions.md) | `GET /mempool/recent` | [docs](https://mempool.space/docs/api/rest) |
