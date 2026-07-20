# <img src="https://images.mindcloud.co/apps/icons/mempool_1778000616349.png" alt="Mempool logo" width="28" height="28"> Mempool: Universal API

Explore Bitcoin blockchain, mempool, fee, mining, address, transaction, and block data using the public Mempool API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mempool/latest
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://mempool.space
- **Vendor API docs:** https://mempool.space/docs/api/rest

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Address Summary](actions/get-address-summary.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mempool/latest/actions/get-address-summary?connectionId=$CONNECTION_ID&address=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Address Mempool Transaction

| Action | Method | Description |
| --- | --- | --- |
| [List Address Mempool Transactions](actions/list-address-mempool-transactions.md) | GET | Retrieves unconfirmed transaction history for an address from Mempool. |

### Address Transaction

| Action | Method | Description |
| --- | --- | --- |
| [List Address Transactions](actions/list-address-transactions.md) | GET | Retrieves transaction history for an address from Mempool. |

### Bitcoin Address

| Action | Method | Description |
| --- | --- | --- |
| [Get Address Summary](actions/get-address-summary.md) | GET | Retrieves summary details for an address from Mempool. |

### Bitcoin Prices

| Action | Method | Description |
| --- | --- | --- |
| [Get Bitcoin Prices](actions/get-bitcoin-prices.md) | GET | Retrieves Bitcoin price data from Mempool. |

### Block

| Action | Method | Description |
| --- | --- | --- |
| [Get Block](actions/get-block.md) | GET | Retrieves details about a block from Mempool. |
| [List Recent Blocks](actions/list-recent-blocks.md) | GET | Retrieves recent blocks with fee and mining details from Mempool. |

### Block Hash

| Action | Method | Description |
| --- | --- | --- |
| [Get Tip Hash](actions/get-tip-hash.md) | GET | Retrieves the current block hash from Mempool. |

### Block Header

| Action | Method | Description |
| --- | --- | --- |
| [Get Block Header](actions/get-block-header.md) | GET | Retrieves a block header from Mempool. |

### Block Height

| Action | Method | Description |
| --- | --- | --- |
| [Get Tip Height](actions/get-tip-height.md) | GET | Retrieves the current block height from Mempool. |

### Block Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Block Status](actions/get-block-status.md) | GET | Retrieves the confirmation status of a block from Mempool. |

### Block Transaction

| Action | Method | Description |
| --- | --- | --- |
| [List Block Transactions](actions/list-block-transactions.md) | GET | Retrieves transactions from a block in Mempool. |

### Difficulty Adjustment

| Action | Method | Description |
| --- | --- | --- |
| [Get Difficulty Adjustment](actions/get-difficulty-adjustment.md) | GET | Retrieves difficulty adjustment details from Mempool. |

### Mempool Summary

| Action | Method | Description |
| --- | --- | --- |
| [Get Mempool Summary](actions/get-mempool-summary.md) | GET | Retrieves current mempool backlog statistics from Mempool. |

### Mempool Transaction

| Action | Method | Description |
| --- | --- | --- |
| [List Recent Mempool Transactions](actions/list-recent-mempool-transactions.md) | GET | Retrieves recent mempool transactions from Mempool. |

### Mining Hashrate

| Action | Method | Description |
| --- | --- | --- |
| [Get Mining Hashrate](actions/get-mining-hashrate.md) | GET | Retrieves network hashrate and difficulty from Mempool. |

### Mining Pool

| Action | Method | Description |
| --- | --- | --- |
| [Get Mining Pool](actions/get-mining-pool.md) | GET | Retrieves mining pool details from Mempool. |
| [List Mining Pools](actions/list-mining-pools.md) | GET | Retrieves mining pools from Mempool for a time period. |

### Recommended Fees

| Action | Method | Description |
| --- | --- | --- |
| [Get Recommended Fees](actions/get-recommended-fees.md) | GET | Retrieves recommended transaction fees from Mempool. |

### Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Get Transaction](actions/get-transaction.md) | GET | Retrieves full transaction details from Mempool. |

### Transaction Hex

| Action | Method | Description |
| --- | --- | --- |
| [Get Transaction Hex](actions/get-transaction-hex.md) | GET | Retrieves a transaction serialized as hex from Mempool. |

### Transaction Id

| Action | Method | Description |
| --- | --- | --- |
| [Get Block Transaction ID at Index](actions/get-block-transaction-id-at-index.md) | GET | Retrieves a block transaction ID from Mempool by index. |
| [List Block Transaction IDs](actions/list-block-transaction-ids.md) | GET | Retrieves all transaction IDs for a block from Mempool. |
| [List Mempool Transaction IDs](actions/list-mempool-transaction-ids.md) | GET | Retrieves all mempool transaction IDs from Mempool. |

### Transaction Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Transaction Status](actions/get-transaction-status.md) | GET | Retrieves transaction confirmation status from Mempool. |

