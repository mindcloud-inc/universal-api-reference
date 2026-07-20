# <img src="https://images.mindcloud.co/apps/icons/flow-blockchain_1776173982141.png" alt="Flow Blockchain logo" width="28" height="28"> Flow Blockchain: Universal API

Query Flow blocks, accounts, transactions, events, and EVM data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/flowBlockchain/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://flow.com
- **Vendor API docs:** https://developers.flow.com/http-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Call EVM Contract](actions/call-evm-contract.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flowBlockchain/latest/actions/call-evm-contract?connectionId=$CONNECTION_ID&params%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves an account from Flow Blockchain. |

### Account Key

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Key](actions/get-account-key.md) | GET | Retrieves an account key from Flow Blockchain. |

### Block

| Action | Method | Description |
| --- | --- | --- |
| [Get Blocks by Height](actions/get-blocks-by-height.md) | GET | Retrieves blocks from Flow Blockchain by height. |
| [Get Blocks by ID](actions/get-blocks-by-id.md) | GET | Retrieves blocks from Flow Blockchain by ID. |

### Block Payload

| Action | Method | Description |
| --- | --- | --- |
| [Get Block Payload](actions/get-block-payload.md) | GET | Retrieves a block payload from Flow Blockchain. |

### Collection

| Action | Method | Description |
| --- | --- | --- |
| [Get Collection](actions/get-collection.md) | GET | Retrieves a collection from Flow Blockchain. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Get Events](actions/get-events.md) | GET | Retrieves events from Flow Blockchain. |

### Evm Account

| Action | Method | Description |
| --- | --- | --- |
| [Get EVM Balance](actions/get-evm-balance.md) | GET | Retrieves an EVM balance from Flow Blockchain. |
| [Get EVM Transaction Count](actions/get-evm-transaction-count.md) | GET | Retrieves an EVM transaction count from Flow Blockchain. |

### Evm Block

| Action | Method | Description |
| --- | --- | --- |
| [Get EVM Block by Hash](actions/get-evm-block-by-hash.md) | GET | Retrieves an EVM block from Flow Blockchain by hash. |
| [Get EVM Block by Number](actions/get-evm-block-by-number.md) | GET | Retrieves an EVM block from Flow Blockchain by number. |
| [Get EVM Block Number](actions/get-evm-block-number.md) | GET | Retrieves the latest EVM block number from Flow Blockchain. |
| [Get EVM Block Transaction Count by Hash](actions/get-evm-block-transaction-count-by-hash.md) | GET | Retrieves EVM block transaction count from Flow Blockchain by hash. |
| [Get EVM Block Transaction Count by Number](actions/get-evm-block-transaction-count-by-number.md) | GET | Retrieves EVM block transaction count from Flow Blockchain by number. |

### Evm Call

| Action | Method | Description |
| --- | --- | --- |
| [Call EVM Contract](actions/call-evm-contract.md) | GET | Retrieves EVM contract call results from Flow Blockchain. |

### Evm Contract

| Action | Method | Description |
| --- | --- | --- |
| [Get EVM Contract Code](actions/get-evm-contract-code.md) | GET | Retrieves EVM contract code from Flow Blockchain. |

### Evm Fee

| Action | Method | Description |
| --- | --- | --- |
| [Get EVM Fee History](actions/get-evm-fee-history.md) | GET | Retrieves EVM fee history from Flow Blockchain. |
| [Get EVM Gas Price](actions/get-evm-gas-price.md) | GET | Retrieves the EVM gas price from Flow Blockchain. |
| [Get EVM Priority Fee](actions/get-evm-priority-fee.md) | GET | Retrieves the EVM priority fee from Flow Blockchain. |

### Evm Gas Estimate

| Action | Method | Description |
| --- | --- | --- |
| [Estimate EVM Gas](actions/estimate-evm-gas.md) | GET | Retrieves an EVM gas estimate from Flow Blockchain. |

### Evm Log

| Action | Method | Description |
| --- | --- | --- |
| [Get EVM Logs](actions/get-evm-logs.md) | GET | Retrieves EVM logs from Flow Blockchain. |

### Evm Network

| Action | Method | Description |
| --- | --- | --- |
| [Get EVM Chain ID](actions/get-evm-chain-id.md) | GET | Retrieves the EVM chain ID from Flow Blockchain. |
| [Get EVM Network ID](actions/get-evm-network-id.md) | GET | Retrieves the EVM network ID from Flow Blockchain. |

### Evm Node

| Action | Method | Description |
| --- | --- | --- |
| [Get EVM Client Version](actions/get-evm-client-version.md) | GET | Retrieves the EVM client version from Flow Blockchain. |
| [Get EVM Sync Status](actions/get-evm-sync-status.md) | GET | Retrieves EVM sync status from Flow Blockchain. |

### Evm Storage

| Action | Method | Description |
| --- | --- | --- |
| [Get EVM Storage Slot](actions/get-evm-storage-slot.md) | GET | Retrieves an EVM storage slot from Flow Blockchain. |

### Evm Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Get EVM Transaction by Block Hash and Index](actions/get-evm-transaction-by-block-hash-and-index.md) | GET | Retrieves an EVM transaction from Flow Blockchain by block hash and index. |
| [Get EVM Transaction by Block Number and Index](actions/get-evm-transaction-by-block-number-and-index.md) | GET | Retrieves an EVM transaction from Flow Blockchain by block number and index. |
| [Get EVM Transaction by Hash](actions/get-evm-transaction-by-hash.md) | GET | Retrieves an EVM transaction from Flow Blockchain by hash. |
| [Send EVM Raw Transaction](actions/send-evm-raw-transaction.md) | POST | Submits a raw EVM transaction to Flow Blockchain. |

### Evm Transaction Receipt

| Action | Method | Description |
| --- | --- | --- |
| [Get EVM Block Receipts](actions/get-evm-block-receipts.md) | GET | Retrieves EVM block receipts from Flow Blockchain. |
| [Get EVM Transaction Receipt](actions/get-evm-transaction-receipt.md) | GET | Retrieves an EVM transaction receipt from Flow Blockchain. |

### Execution Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Execution Result](actions/get-execution-result.md) | GET | Retrieves an execution result from Flow Blockchain. |
| [Get Execution Results by Block](actions/get-execution-results-by-block.md) | GET | Retrieves execution results from Flow Blockchain by block. |

### Network

| Action | Method | Description |
| --- | --- | --- |
| [Get Network Parameters](actions/get-network-parameters.md) | GET | Retrieves network parameters from Flow Blockchain. |

### Node Version

| Action | Method | Description |
| --- | --- | --- |
| [Get Node Version Info](actions/get-node-version-info.md) | GET | Retrieves node version information from Flow Blockchain. |

### Script Result

| Action | Method | Description |
| --- | --- | --- |
| [Execute Cadence Script](actions/execute-cadence-script.md) | GET | Executes a Cadence script on Flow Blockchain. |

### Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Get Transaction](actions/get-transaction.md) | GET | Retrieves a transaction from Flow Blockchain. |
| [Submit Signed Transaction](actions/submit-signed-transaction.md) | POST | Submits a signed transaction to Flow Blockchain. |

### Transaction Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Transaction Result](actions/get-transaction-result.md) | GET | Retrieves a transaction result from Flow Blockchain. |

