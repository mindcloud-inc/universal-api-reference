# Flow Blockchain: Native API Reference

A consolidated summary of Flow Blockchain's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://developers.flow.com/http-api
- **OpenAPI specification:** https://raw.githubusercontent.com/onflow/flow/87a8f227ad761fa61576b014e3562d3b6c38d8a6/openapi/access.yaml
- **REST API base URL:** `https://rest-mainnet.onflow.org/v1`
- **REST API base URL:** `https://mainnet.evm.nodes.onflow.org`

## Authentication

### No Authentication

Public Flow Access API and Flow EVM JSON-RPC reads do not require provider-issued credentials.

This API does not require request authentication.

[Official authentication documentation](https://developers.flow.com/http-api)

## API conventions

### REST API

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

### REST API

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

- **REST API:** Retry responses with status codes `408,429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.
- **REST API:** Retry responses with status codes `408,429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Call EVM Contract](actions/call-evm-contract.md) | `POST https://mainnet.evm.nodes.onflow.org` | [docs](https://developers.flow.com/build/evm/networks) |
| [Estimate EVM Gas](actions/estimate-evm-gas.md) | `POST https://mainnet.evm.nodes.onflow.org` | [docs](https://developers.flow.com/build/evm/networks) |
| [Execute Cadence Script](actions/execute-cadence-script.md) | `POST /scripts` | [docs](https://developers.flow.com/http-api) |
| [Get Account](actions/get-account.md) | `GET /accounts/{address}` | [docs](https://developers.flow.com/http-api) |
| [Get Account Key](actions/get-account-key.md) | `GET /accounts/{address}/keys/{index}` | [docs](https://developers.flow.com/http-api) |
| [Get Block Payload](actions/get-block-payload.md) | `GET /blocks/{id}/payload` | [docs](https://developers.flow.com/http-api) |
| [Get Blocks by Height](actions/get-blocks-by-height.md) | `GET /blocks` | [docs](https://developers.flow.com/http-api) |
| [Get Blocks by ID](actions/get-blocks-by-id.md) | `GET /blocks/{id}` | [docs](https://developers.flow.com/http-api) |
| [Get Collection](actions/get-collection.md) | `GET /collections/{id}` | [docs](https://developers.flow.com/http-api) |
| [Get Events](actions/get-events.md) | `GET /events` | [docs](https://developers.flow.com/http-api) |
| [Get EVM Balance](actions/get-evm-balance.md) | `POST https://mainnet.evm.nodes.onflow.org` | [docs](https://developers.flow.com/build/evm/networks) |
| [Get EVM Block by Hash](actions/get-evm-block-by-hash.md) | `POST https://mainnet.evm.nodes.onflow.org` | [docs](https://developers.flow.com/build/evm/networks) |
| [Get EVM Block by Number](actions/get-evm-block-by-number.md) | `POST https://mainnet.evm.nodes.onflow.org` | [docs](https://developers.flow.com/build/evm/networks) |
| [Get EVM Block Number](actions/get-evm-block-number.md) | `POST https://mainnet.evm.nodes.onflow.org` | [docs](https://developers.flow.com/build/evm/networks) |
| [Get EVM Block Receipts](actions/get-evm-block-receipts.md) | `POST https://mainnet.evm.nodes.onflow.org` | [docs](https://developers.flow.com/build/evm/networks) |
| [Get EVM Block Transaction Count by Hash](actions/get-evm-block-transaction-count-by-hash.md) | `POST https://mainnet.evm.nodes.onflow.org` | [docs](https://developers.flow.com/build/evm/networks) |
| [Get EVM Block Transaction Count by Number](actions/get-evm-block-transaction-count-by-number.md) | `POST https://mainnet.evm.nodes.onflow.org` | [docs](https://developers.flow.com/build/evm/networks) |
| [Get EVM Chain ID](actions/get-evm-chain-id.md) | `POST https://mainnet.evm.nodes.onflow.org` | [docs](https://developers.flow.com/build/evm/networks) |
| [Get EVM Client Version](actions/get-evm-client-version.md) | `POST https://mainnet.evm.nodes.onflow.org` | [docs](https://developers.flow.com/build/evm/networks) |
| [Get EVM Contract Code](actions/get-evm-contract-code.md) | `POST https://mainnet.evm.nodes.onflow.org` | [docs](https://developers.flow.com/build/evm/networks) |
| [Get EVM Fee History](actions/get-evm-fee-history.md) | `POST https://mainnet.evm.nodes.onflow.org` | [docs](https://developers.flow.com/build/evm/networks) |
| [Get EVM Gas Price](actions/get-evm-gas-price.md) | `POST https://mainnet.evm.nodes.onflow.org` | [docs](https://developers.flow.com/build/evm/networks) |
| [Get EVM Logs](actions/get-evm-logs.md) | `POST https://mainnet.evm.nodes.onflow.org` | [docs](https://developers.flow.com/build/evm/networks) |
| [Get EVM Network ID](actions/get-evm-network-id.md) | `POST https://mainnet.evm.nodes.onflow.org` | [docs](https://developers.flow.com/build/evm/networks) |
| [Get EVM Priority Fee](actions/get-evm-priority-fee.md) | `POST https://mainnet.evm.nodes.onflow.org` | [docs](https://developers.flow.com/build/evm/networks) |
| [Get EVM Storage Slot](actions/get-evm-storage-slot.md) | `POST https://mainnet.evm.nodes.onflow.org` | [docs](https://developers.flow.com/build/evm/networks) |
| [Get EVM Sync Status](actions/get-evm-sync-status.md) | `POST https://mainnet.evm.nodes.onflow.org` | [docs](https://developers.flow.com/build/evm/networks) |
| [Get EVM Transaction by Block Hash and Index](actions/get-evm-transaction-by-block-hash-and-index.md) | `POST https://mainnet.evm.nodes.onflow.org` | [docs](https://developers.flow.com/build/evm/networks) |
| [Get EVM Transaction by Block Number and Index](actions/get-evm-transaction-by-block-number-and-index.md) | `POST https://mainnet.evm.nodes.onflow.org` | [docs](https://developers.flow.com/build/evm/networks) |
| [Get EVM Transaction by Hash](actions/get-evm-transaction-by-hash.md) | `POST https://mainnet.evm.nodes.onflow.org` | [docs](https://developers.flow.com/build/evm/networks) |
| [Get EVM Transaction Count](actions/get-evm-transaction-count.md) | `POST https://mainnet.evm.nodes.onflow.org` | [docs](https://developers.flow.com/build/evm/networks) |
| [Get EVM Transaction Receipt](actions/get-evm-transaction-receipt.md) | `POST https://mainnet.evm.nodes.onflow.org` | [docs](https://developers.flow.com/build/evm/networks) |
| [Get Execution Result](actions/get-execution-result.md) | `GET /execution_results/{id}` | [docs](https://developers.flow.com/http-api) |
| [Get Execution Results by Block](actions/get-execution-results-by-block.md) | `GET /execution_results` | [docs](https://developers.flow.com/http-api) |
| [Get Network Parameters](actions/get-network-parameters.md) | `GET /network/parameters` | [docs](https://developers.flow.com/http-api) |
| [Get Node Version Info](actions/get-node-version-info.md) | `GET /node_version_info` | [docs](https://developers.flow.com/http-api) |
| [Get Transaction](actions/get-transaction.md) | `GET /transactions/{id}` | [docs](https://developers.flow.com/http-api) |
| [Get Transaction Result](actions/get-transaction-result.md) | `GET /transaction_results/{transaction_id}` | [docs](https://developers.flow.com/http-api) |
| [Send EVM Raw Transaction](actions/send-evm-raw-transaction.md) | `POST https://mainnet.evm.nodes.onflow.org` | [docs](https://developers.flow.com/build/evm/networks) |
| [Submit Signed Transaction](actions/submit-signed-transaction.md) | `POST /transactions` | [docs](https://developers.flow.com/http-api) |
