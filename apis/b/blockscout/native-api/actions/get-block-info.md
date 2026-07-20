# Get Block Info with Blockscout

Retrieves details for a specific block from Blockscout.

## Endpoint

- **Method:** `GET`
- **Path:** `/:chain_id/api/v2/blocks/:block_hash_or_number_param`
- **Base URL:** `https://api.blockscout.com`
- **Official documentation:** [Get Block Info](https://docs.blockscout.com/api-reference/get-block-info)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chain_id` | path | `string` | no | — |
| `block_hash_or_number_param` | path | `string` | yes | Block number or hash to retrieve. |
