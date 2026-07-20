# Get Execution Results by Block with Flow Blockchain

Retrieves execution results from Flow Blockchain by block.

## Endpoint

- **Method:** `GET`
- **Path:** `/execution_results`
- **Base URL:** `https://rest-mainnet.onflow.org/v1`
- **API:** rest
- **Official documentation:** [Get Execution Results by Block](https://developers.flow.com/http-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `block_id` | query | `string` | yes | Block ID for the execution result lookup. |
