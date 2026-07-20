# Get Transaction Result with Flow Blockchain

Retrieves a transaction result from Flow Blockchain.

## Endpoint

- **Method:** `GET`
- **Path:** `/transaction_results/{transaction_id}`
- **Base URL:** `https://rest-mainnet.onflow.org/v1`
- **API:** rest
- **Official documentation:** [Get Transaction Result](https://developers.flow.com/http-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transaction_id` | path | `string` | yes | Transaction ID whose result should be returned. |
