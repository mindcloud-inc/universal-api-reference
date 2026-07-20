# <img src="https://images.mindcloud.co/apps/icons/a305553a-cc31-41f6-833b-423548d6ac91-2_1777581296015.png" alt="Infura Ethereum logo" width="28" height="28"> Infura Ethereum: Universal API

Access Ethereum JSON-RPC endpoints and manage Infura API keys

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/infuraEthereum/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.infura.io
- **Vendor API docs:** https://docs.metamask.io/services/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Latest Block Number](actions/get-latest-block-number.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/infuraEthereum/latest/actions/get-latest-block-number?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Access List

| Action | Method | Description |
| --- | --- | --- |
| [Create Access List](actions/create-access-list.md) | GET | Retrieves an access list from Infura Ethereum. |

### Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Balance](actions/get-balance.md) | GET | Retrieves an address balance from Infura Ethereum. |

### Blob Base Fee

| Action | Method | Description |
| --- | --- | --- |
| [Get Blob Base Fee](actions/get-blob-base-fee.md) | GET | Retrieves the blob base fee from Infura Ethereum. |

### Block

| Action | Method | Description |
| --- | --- | --- |
| [Get Block By Hash](actions/get-block-by-hash.md) | GET | Retrieves a block from Infura Ethereum by hash. |
| [Get Block By Number](actions/get-block-by-number.md) | GET | Retrieves a block from Infura Ethereum by number. |

### Block Number

| Action | Method | Description |
| --- | --- | --- |
| [Get Latest Block Number](actions/get-latest-block-number.md) | GET | Retrieves the latest block number from Infura Ethereum. |

### Block Receipt

| Action | Method | Description |
| --- | --- | --- |
| [Get Block Receipts](actions/get-block-receipts.md) | GET | Retrieves block receipts from Infura Ethereum. |

### Block Transaction Count

| Action | Method | Description |
| --- | --- | --- |
| [Get Block Transaction Count By Number](actions/get-block-transaction-count-by-number.md) | GET | Retrieves block transaction count from Infura Ethereum by number. |

### Call Result

| Action | Method | Description |
| --- | --- | --- |
| [Call Contract](actions/call-contract.md) | GET | Retrieves a contract call result from Infura Ethereum. |

### Chain Id

| Action | Method | Description |
| --- | --- | --- |
| [Get Chain ID](actions/get-chain-id.md) | GET | Retrieves the chain ID from Infura Ethereum. |

### Contract Code

| Action | Method | Description |
| --- | --- | --- |
| [Get Contract Code](actions/get-contract-code.md) | GET | Retrieves contract code from Infura Ethereum. |

### Fee History

| Action | Method | Description |
| --- | --- | --- |
| [Get Fee History](actions/get-fee-history.md) | GET | Retrieves fee history from Infura Ethereum. |

### Gas Estimate

| Action | Method | Description |
| --- | --- | --- |
| [Estimate Gas](actions/estimate-gas.md) | GET | Retrieves a gas estimate from Infura Ethereum. |

### Gas Price

| Action | Method | Description |
| --- | --- | --- |
| [Get Gas Price](actions/get-gas-price.md) | GET | Retrieves the gas price from Infura Ethereum. |

### Log

| Action | Method | Description |
| --- | --- | --- |
| [Get Logs](actions/get-logs.md) | GET | Retrieves logs from Infura Ethereum. |

### Max Priority Fee Per Gas

| Action | Method | Description |
| --- | --- | --- |
| [Get Max Priority Fee Per Gas](actions/get-max-priority-fee-per-gas.md) | GET | Retrieves the max priority fee per gas from Infura Ethereum. |

### Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Get Transaction By Block Number And Index](actions/get-transaction-by-block-number-and-index.md) | GET | Retrieves a transaction from Infura Ethereum by block and index. |
| [Get Transaction By Hash](actions/get-transaction-by-hash.md) | GET | Retrieves a transaction from Infura Ethereum by hash. |

### Transaction Count

| Action | Method | Description |
| --- | --- | --- |
| [Get Transaction Count](actions/get-transaction-count.md) | GET | Retrieves an address transaction count from Infura Ethereum. |

### Transaction Receipt

| Action | Method | Description |
| --- | --- | --- |
| [Get Transaction Receipt](actions/get-transaction-receipt.md) | GET | Retrieves a transaction receipt from Infura Ethereum. |

