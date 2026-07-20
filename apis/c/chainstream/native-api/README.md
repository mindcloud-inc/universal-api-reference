# Chainstream: Native API Reference

A consolidated summary of Chainstream's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://docs.chainstream.io/en/api-reference
- **API base URL:** `https://api.chainstream.io`

## Authentication

### OAuth2 Client Credentials

Connect with Chainstream using OAuth2 client credentials.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://dex.asia.auth.chainstream.io/oauth/token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `webhook.read webhook.write kyt.read kyt.write`.

A machine-to-machine flow is configured.

[Official authentication documentation](https://docs.chainstream.io/en/api-reference/authentication/authenticate)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The next-page cursor is read from `endCursor`.

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Batch Get Token Metadata](actions/batch-get-token-metadata.md) | `GET /v2/token/:chain/metadata/multi` | [docs](https://docs.chainstream.io/en/api-reference/endpoint/data/token/v2/token-chain-metadata-multi-get) |
| [Build DEX Route](actions/build-dex-route.md) | `POST /v2/dex/:chain/route` | [docs](https://docs.chainstream.io/en/api-reference/endpoint/defi/dex/v2/dex-chain-route-post) |
| [Calculate Wallet PnL](actions/calculate-wallet-pnl.md) | `POST /v2/wallet/:chain/:walletAddress/calculate-pnl` | [docs](https://docs.chainstream.io/en/api-reference/endpoint/data/wallet/v2/wallet-chain-walletaddress-calculate-pnl-post) |
| [Create Webhook Endpoint](actions/create-webhook-endpoint.md) | `POST /v2/webhook/endpoint` | [docs](https://docs.chainstream.io/en/api-reference/endpoint/data/webhook/v2/webhook-endpoint-post) |
| [Execute DEX Swap](actions/execute-dex-swap.md) | `POST /v2/dex/:chain/swap` | [docs](https://docs.chainstream.io/en/api-reference/endpoint/defi/dex/v2/dex-chain-swap-post) |
| [Get DEX Quote](actions/get-dex-quote.md) | `GET /v2/dex/:chain/quote` | [docs](https://docs.chainstream.io/en/api-reference/endpoint/defi/dex/v2/dex-chain-quote-get) |
| [Get Final Stretch Tokens](actions/get-final-stretch-tokens.md) | `GET /v2/ranking/:chain/finalStretch` | [docs](https://docs.chainstream.io/en/api-reference/endpoint/data/ranking/v2/ranking-chain-finalstretch-get) |
| [Get Hot Tokens](actions/get-hot-tokens.md) | `GET /v2/ranking/:chain/hotTokens/:duration` | [docs](https://docs.chainstream.io/en/api-reference/endpoint/data/ranking/v2/ranking-chain-hottokens-duration-get) |
| [Get Latest Block](actions/get-latest-block.md) | `GET /v2/blockchain/:chain/latest_block` | [docs](https://docs.chainstream.io/en/api-reference/endpoint/data/blockchain/v2/blockchain-chain-latest_block-get) |
| [Get Migrated Tokens](actions/get-migrated-tokens.md) | `GET /v2/ranking/:chain/migrated` | [docs](https://docs.chainstream.io/en/api-reference/endpoint/data/ranking/v2/ranking-chain-migrated-get) |
| [Get New Tokens](actions/get-new-tokens.md) | `GET /v2/ranking/:chain/newTokens` | [docs](https://docs.chainstream.io/en/api-reference/endpoint/data/ranking/v2/ranking-chain-newtokens-get) |
| [Get Token Creation](actions/get-token-creation.md) | `GET /v2/token/:chain/:tokenAddress/creation` | [docs](https://docs.chainstream.io/en/api-reference/endpoint/data/token/v2/token-chain-tokenaddress-creation-get) |
| [Get Token Detail](actions/get-token-detail.md) | `GET /v2/token/:chain/:tokenAddress` | [docs](https://docs.chainstream.io/en/api-reference/endpoint/data/token/v2/token-chain-tokenaddress-get) |
| [Get Token Holders](actions/get-token-holders.md) | `GET /v2/token/:chain/:tokenAddress/holders` | [docs](https://docs.chainstream.io/en/api-reference/endpoint/data/token/v2/token-chain-tokenaddress-holders-get) |
| [Get Token Metadata](actions/get-token-metadata.md) | `GET /v2/token/:chain/:tokenAddress/metadata` | [docs](https://docs.chainstream.io/en/api-reference/endpoint/data/token/v2/token-chain-tokenaddress-metadata-get) |
| [Get Token Pools](actions/get-token-pools.md) | `GET /v2/token/:chain/:tokenAddress/pools` | [docs](https://docs.chainstream.io/en/api-reference/endpoint/data/token/v2/token-chain-tokenaddress-pools-get) |
| [Get Token Security](actions/get-token-security.md) | `GET /v2/token/:chain/:tokenAddress/security` | [docs](https://docs.chainstream.io/en/api-reference/endpoint/data/token/v2/token-chain-tokenaddress-security-get) |
| [Get Token Stats](actions/get-token-stats.md) | `GET /v2/token/:chain/:tokenAddress/stats` | [docs](https://docs.chainstream.io/en/api-reference/endpoint/data/token/v2/token-chain-tokenaddress-stats-get) |
| [Get Wallet Net Worth](actions/get-wallet-net-worth.md) | `GET /v2/wallet/:chain/:walletAddress/net-worth` | [docs](https://docs.chainstream.io/en/api-reference/endpoint/data/wallet/v2/wallet-chain-walletaddress-net-worth-get) |
| [Get Wallet Net Worth Details](actions/get-wallet-net-worth-details.md) | `GET /v2/wallet/:chain/:walletAddress/net-worth-details` | [docs](https://docs.chainstream.io/en/api-reference/endpoint/data/wallet/v2/wallet-chain-walletaddress-net-worth-details-get) |
| [Get Wallet PnL](actions/get-wallet-pnl.md) | `GET /v2/wallet/:chain/:walletAddress/pnl` | [docs](https://docs.chainstream.io/en/api-reference/endpoint/data/wallet/v2/wallet-chain-walletaddress-pnl-get) |
| [Get Wallet PnL Details](actions/get-wallet-pnl-details.md) | `GET /v2/wallet/:chain/:walletAddress/pnl-details` | [docs](https://docs.chainstream.io/en/api-reference/endpoint/data/wallet/v2/wallet-chain-walletaddress-pnl-details-get) |
| [Get Wallet Token Balances](actions/get-wallet-token-balances.md) | `GET /v2/wallet/:chain/:walletAddress/tokens-balance` | [docs](https://docs.chainstream.io/en/api-reference/endpoint/data/wallet/v2/wallet-chain-walletaddress-tokens-balance-get) |
| [Get Wallet Transfer Total](actions/get-wallet-transfer-total.md) | `GET /v2/wallet/:chain/:walletAddress/transfer-total` | [docs](https://docs.chainstream.io/en/api-reference/endpoint/data/wallet/v2/wallet-chain-walletaddress-transfer-total-get) |
| [Get Wallet Transfers](actions/get-wallet-transfers.md) | `GET /v2/wallet/:chain/:walletAddress/transfers` | [docs](https://docs.chainstream.io/en/api-reference/endpoint/data/wallet/v2/wallet-chain-walletaddress-transfers-get) |
| [Get Webhook Endpoint](actions/get-webhook-endpoint.md) | `GET /v2/webhook/endpoint/:id` | [docs](https://docs.chainstream.io/en/api-reference/endpoint/data/webhook/v2/webhook-endpoint-id-get) |
| [List Blockchains](actions/list-blockchains.md) | `GET /v1/blockchain` | [docs](https://docs.chainstream.io/en/api-reference/endpoint/blockchain/v1/blockchain-get) |
| [List Tokens](actions/list-tokens.md) | `GET /v2/token/:chain/list` | [docs](https://docs.chainstream.io/en/api-reference/endpoint/data/token/v2/token-chain-list-get) |
| [List Webhook Endpoints](actions/list-webhook-endpoints.md) | `GET /v2/webhook/endpoint` | [docs](https://docs.chainstream.io/en/api-reference/endpoint/data/webhook/v2/webhook-endpoint-get) |
| [Search Tokens](actions/search-tokens.md) | `GET /v2/token/search` | [docs](https://docs.chainstream.io/en/api-reference/endpoint/data/token/v2/token-search-get) |
| [Update Webhook Endpoint](actions/update-webhook-endpoint.md) | `PATCH /v2/webhook/endpoint` | [docs](https://docs.chainstream.io/en/api-reference/endpoint/data/webhook/v2/webhook-endpoint-patch) |
