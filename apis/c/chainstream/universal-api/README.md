# <img src="https://images.mindcloud.co/apps/icons/chainstream_1775838221308.png" alt="Chainstream logo" width="28" height="28"> Chainstream: Universal API

Analyze blockchain, token, wallet, trade, and compliance data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/chainstream/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://chainstream.io
- **Vendor API docs:** https://docs.chainstream.io/en/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Blockchains](actions/list-blockchains.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chainstream/latest/actions/list-blockchains?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Blockchain

| Action | Method | Description |
| --- | --- | --- |
| [List Blockchains](actions/list-blockchains.md) | GET | Retrieves supported blockchains from Chainstream. |

### Dex Quote

| Action | Method | Description |
| --- | --- | --- |
| [Get DEX Quote](actions/get-dex-quote.md) | GET | Retrieves a DEX quote from Chainstream. |

### Dex Route

| Action | Method | Description |
| --- | --- | --- |
| [Build DEX Route](actions/build-dex-route.md) | GET | Calculates the best DEX swap route in Chainstream. |

### Dex Swap

| Action | Method | Description |
| --- | --- | --- |
| [Execute DEX Swap](actions/execute-dex-swap.md) | POST | Creates a DEX swap transaction in Chainstream. |

### Latest Block

| Action | Method | Description |
| --- | --- | --- |
| [Get Latest Block](actions/get-latest-block.md) | GET | Retrieves the latest blockchain block from Chainstream. |

### Token

| Action | Method | Description |
| --- | --- | --- |
| [Batch Get Token Metadata](actions/batch-get-token-metadata.md) | GET | Retrieves token metadata in bulk from Chainstream. |
| [Get Token Creation](actions/get-token-creation.md) | GET | Retrieves token creation details from Chainstream. |
| [Get Token Detail](actions/get-token-detail.md) | GET | Retrieves token details from Chainstream. |
| [Get Token Holders](actions/get-token-holders.md) | GET | Retrieves token holders from Chainstream. |
| [Get Token Metadata](actions/get-token-metadata.md) | GET | Retrieves token metadata from Chainstream. |
| [Get Token Pools](actions/get-token-pools.md) | GET | Retrieves token pools from Chainstream. |
| [Get Token Security](actions/get-token-security.md) | GET | Retrieves token security details from Chainstream. |
| [Get Token Stats](actions/get-token-stats.md) | GET | Retrieves token stats from Chainstream. |
| [List Tokens](actions/list-tokens.md) | GET | Retrieves tokens for a blockchain from Chainstream. |
| [Search Tokens](actions/search-tokens.md) | GET | Finds tokens in Chainstream by search query. |

### Token Ranking

| Action | Method | Description |
| --- | --- | --- |
| [Get Final Stretch Tokens](actions/get-final-stretch-tokens.md) | GET | Retrieves final stretch tokens from Chainstream. |
| [Get Hot Tokens](actions/get-hot-tokens.md) | GET | Retrieves hot tokens from Chainstream. |
| [Get Migrated Tokens](actions/get-migrated-tokens.md) | GET | Retrieves migrated tokens from Chainstream. |
| [Get New Tokens](actions/get-new-tokens.md) | GET | Retrieves new tokens from Chainstream. |

### Wallet Net Worth

| Action | Method | Description |
| --- | --- | --- |
| [Get Wallet Net Worth](actions/get-wallet-net-worth.md) | GET | Retrieves wallet net worth from Chainstream. |

### Wallet Net Worth Detail

| Action | Method | Description |
| --- | --- | --- |
| [Get Wallet Net Worth Details](actions/get-wallet-net-worth-details.md) | GET | Retrieves wallet net worth details from Chainstream. |

### Wallet Pnl

| Action | Method | Description |
| --- | --- | --- |
| [Calculate Wallet PnL](actions/calculate-wallet-pnl.md) | POST | Calculates wallet token PnL in Chainstream. |
| [Get Wallet PnL](actions/get-wallet-pnl.md) | GET | Retrieves wallet PnL from Chainstream. |

### Wallet Pnl Detail

| Action | Method | Description |
| --- | --- | --- |
| [Get Wallet PnL Details](actions/get-wallet-pnl-details.md) | GET | Retrieves wallet PnL details from Chainstream. |

### Wallet Token Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Wallet Token Balances](actions/get-wallet-token-balances.md) | GET | Retrieves wallet token balances from Chainstream. |

### Wallet Transfer

| Action | Method | Description |
| --- | --- | --- |
| [Get Wallet Transfers](actions/get-wallet-transfers.md) | GET | Retrieves wallet transfers from Chainstream. |

### Wallet Transfer Total

| Action | Method | Description |
| --- | --- | --- |
| [Get Wallet Transfer Total](actions/get-wallet-transfer-total.md) | GET | Retrieves wallet transfer totals from Chainstream. |

### Webhook Endpoint

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook Endpoint](actions/create-webhook-endpoint.md) | POST | Creates a webhook endpoint in Chainstream. |
| [Get Webhook Endpoint](actions/get-webhook-endpoint.md) | GET | Retrieves a webhook endpoint from Chainstream. |
| [List Webhook Endpoints](actions/list-webhook-endpoints.md) | GET | Retrieves webhook endpoints from Chainstream. |
| [Update Webhook Endpoint](actions/update-webhook-endpoint.md) | PUT | Updates a webhook endpoint in Chainstream. |

