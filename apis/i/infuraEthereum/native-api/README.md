# Infura Ethereum: Native API Reference

A consolidated summary of Infura Ethereum's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://docs.metamask.io/services/
- **API base URL:** `https://mainnet.infura.io`

## Authentication

### API Key

Connect with an Infura API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://support.metamask.io/develop/building-with-infura/general-knowledge/cors-infura-api/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `result`.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Call Contract](actions/call-contract.md) | `POST /v3/:apiKey` | [docs](https://docs.metamask.io/services/reference/ethereum/json-rpc-methods/eth_call/) |
| [Create Access List](actions/create-access-list.md) | `POST /v3/:apiKey` | [docs](https://docs.metamask.io/services/reference/ethereum/json-rpc-methods/eth_createaccesslist/) |
| [Estimate Gas](actions/estimate-gas.md) | `POST /v3/:apiKey` | [docs](https://docs.metamask.io/services/reference/ethereum/json-rpc-methods/eth_estimategas/) |
| [Get Balance](actions/get-balance.md) | `POST /v3/:apiKey` | [docs](https://docs.metamask.io/services/reference/ethereum/json-rpc-methods/eth_getbalance/) |
| [Get Blob Base Fee](actions/get-blob-base-fee.md) | `POST /v3/:apiKey` | [docs](https://docs.metamask.io/services/reference/ethereum/json-rpc-methods/eth_blobbasefee/) |
| [Get Block By Hash](actions/get-block-by-hash.md) | `POST /v3/:apiKey` | [docs](https://docs.metamask.io/services/reference/ethereum/json-rpc-methods/eth_getblockbyhash/) |
| [Get Block By Number](actions/get-block-by-number.md) | `POST /v3/:apiKey` | [docs](https://docs.metamask.io/services/reference/ethereum/json-rpc-methods/eth_getblockbynumber/) |
| [Get Block Receipts](actions/get-block-receipts.md) | `POST /v3/:apiKey` | [docs](https://docs.metamask.io/services/reference/ethereum/json-rpc-methods/eth_getblockreceipts/) |
| [Get Block Transaction Count By Number](actions/get-block-transaction-count-by-number.md) | `POST /v3/:apiKey` | [docs](https://docs.metamask.io/services/reference/ethereum/json-rpc-methods/eth_getblocktransactioncountbynumber/) |
| [Get Chain ID](actions/get-chain-id.md) | `POST /v3/:apiKey` | [docs](https://docs.metamask.io/services/reference/ethereum/json-rpc-methods/eth_chainid/) |
| [Get Contract Code](actions/get-contract-code.md) | `POST /v3/:apiKey` | [docs](https://docs.metamask.io/services/reference/ethereum/json-rpc-methods/eth_getcode/) |
| [Get Fee History](actions/get-fee-history.md) | `POST /v3/:apiKey` | [docs](https://docs.metamask.io/services/reference/ethereum/json-rpc-methods/eth_feehistory/) |
| [Get Gas Price](actions/get-gas-price.md) | `POST /v3/:apiKey` | [docs](https://docs.metamask.io/services/reference/ethereum/json-rpc-methods/eth_gasprice/) |
| [Get Latest Block Number](actions/get-latest-block-number.md) | `POST /v3/:apiKey` | [docs](https://docs.metamask.io/services/reference/ethereum/json-rpc-methods/eth_blocknumber/) |
| [Get Logs](actions/get-logs.md) | `POST /v3/:apiKey` | [docs](https://docs.metamask.io/services/reference/ethereum/json-rpc-methods/eth_getlogs/) |
| [Get Max Priority Fee Per Gas](actions/get-max-priority-fee-per-gas.md) | `POST /v3/:apiKey` | [docs](https://docs.metamask.io/services/reference/ethereum/json-rpc-methods/eth_maxpriorityfeepergas/) |
| [Get Transaction By Block Number And Index](actions/get-transaction-by-block-number-and-index.md) | `POST /v3/:apiKey` | [docs](https://docs.metamask.io/services/reference/ethereum/json-rpc-methods/eth_gettransactionbyblocknumberandindex/) |
| [Get Transaction By Hash](actions/get-transaction-by-hash.md) | `POST /v3/:apiKey` | [docs](https://docs.metamask.io/services/reference/ethereum/json-rpc-methods/eth_gettransactionbyhash/) |
| [Get Transaction Count](actions/get-transaction-count.md) | `POST /v3/:apiKey` | [docs](https://docs.metamask.io/services/reference/ethereum/json-rpc-methods/eth_gettransactioncount/) |
| [Get Transaction Receipt](actions/get-transaction-receipt.md) | `POST /v3/:apiKey` | [docs](https://docs.metamask.io/services/reference/ethereum/json-rpc-methods/eth_gettransactionreceipt/) |
