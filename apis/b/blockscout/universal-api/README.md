# <img src="https://images.mindcloud.co/apps/icons/favicon-docs-blockscout-com-48x48_1777044388801.png" alt="Blockscout logo" width="28" height="28"> Blockscout: Universal API

Blockscout PRO API integration for multichain EVM explorer data, including blocks, transactions, addresses, tokens, contracts, stats, and search.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/blockscout/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 33
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.blockscout.com
- **Vendor API docs:** https://docs.blockscout.com/devs/apis

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Address Counters](actions/get-address-counters.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blockscout/latest/actions/get-address-counters?connectionId=$CONNECTION_ID&address_hash_param=0xfFd12B32d000617551681973911Fd3ad49B89294" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (33)

### Addresses

| Action | Method | Description |
| --- | --- | --- |
| [Get Address Counters](actions/get-address-counters.md) | GET | Retrieves activity counters for an address from Blockscout. |
| [Get Address Info](actions/get-address-info.md) | GET | Retrieves details for an address or contract from Blockscout. |
| [Get Address Logs](actions/get-address-logs.md) | GET | Retrieves logs emitted by or involving an address from Blockscout. |
| [Get Address Token Balances](actions/get-address-token-balances.md) | GET | Retrieves token balances for an address from Blockscout. |
| [Get Addresses](actions/get-addresses.md) | GET | Retrieves native coin holders from Blockscout. |
| [Get Token Holders](actions/get-token-holders.md) | GET | Retrieves holders for a token from Blockscout. |

### Contracts

| Action | Method | Description |
| --- | --- | --- |
| [Get Smart Contract](actions/get-smart-contract.md) | GET | Retrieves details for a smart contract from Blockscout. |
| [Get Smart Contracts](actions/get-smart-contracts.md) | GET | Retrieves verified smart contracts from Blockscout. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Get Block Info](actions/get-block-info.md) | GET | Retrieves details for a specific block from Blockscout. |
| [Get Blocks](actions/get-blocks.md) | GET | Retrieves blockchain block listings from Blockscout. |
| [Get Indexing Status](actions/get-indexing-status.md) | GET | Retrieves current indexing status from Blockscout. |
| [Get Main Page Blocks](actions/get-main-page-blocks.md) | GET | Retrieves main page blocks from Blockscout. |
| [Get Market Chart](actions/get-market-chart.md) | GET | Retrieves market chart data from Blockscout. |
| [Get Stats Counters](actions/get-stats-counters.md) | GET | Retrieves current stats counters from Blockscout. |
| [Get Token Info](actions/get-token-info.md) | GET | Retrieves details for a token from Blockscout. |
| [Get Tokens](actions/get-tokens.md) | GET | Retrieves current token listings from Blockscout. |
| [Get Transactions Chart](actions/get-transactions-chart.md) | GET | Retrieves transaction chart data from Blockscout. |
| [Search](actions/search.md) | GET | Finds matching addresses, blocks, transactions, tokens, and domains in Blockscout. |

### Transactions

| Action | Method | Description |
| --- | --- | --- |
| [Get Address Internal Transactions](actions/get-address-internal-transactions.md) | GET | Retrieves internal transactions for an address from Blockscout. |
| [Get Address Token Transfers](actions/get-address-token-transfers.md) | GET | Retrieves token transfers for an address from Blockscout. |
| [Get Address Transactions](actions/get-address-transactions.md) | GET | Retrieves transactions for an address from Blockscout. |
| [Get Block Transactions](actions/get-block-transactions.md) | GET | Retrieves transactions for a block from Blockscout. |
| [Get Internal Transactions](actions/get-internal-transactions.md) | GET | Retrieves blockchain internal transactions from Blockscout. |
| [Get Main Page Transactions](actions/get-main-page-transactions.md) | GET | Retrieves main page transactions from Blockscout. |
| [Get Token Transfers](actions/get-token-transfers.md) | GET | Retrieves blockchain token transfers from Blockscout. |
| [Get Token Transfers by Token](actions/get-token-transfers-by-token.md) | GET | Retrieves transfers for a token from Blockscout. |
| [Get Transaction Info](actions/get-transaction-info.md) | GET | Retrieves a transaction's details from Blockscout. |
| [Get Transaction Internal Transactions](actions/get-transaction-internal-transactions.md) | GET | Retrieves internal transactions for a transaction from Blockscout. |
| [Get Transaction Logs](actions/get-transaction-logs.md) | GET | Retrieves logs for a transaction from Blockscout. |
| [Get Transaction State Changes](actions/get-transaction-state-changes.md) | GET | Retrieves state changes for a transaction from Blockscout. |
| [Get Transaction Summary](actions/get-transaction-summary.md) | GET | Retrieves a human-readable transaction summary from Blockscout. |
| [Get Transaction Token Transfers](actions/get-transaction-token-transfers.md) | GET | Retrieves token transfers for a transaction from Blockscout. |
| [Get Transactions](actions/get-transactions.md) | GET | Retrieves blockchain transaction listings from Blockscout. |

