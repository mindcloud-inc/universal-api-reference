# Get Token Info with Blockscout

Retrieves details for a token from Blockscout.

## Endpoint

- **Method:** `GET`
- **Path:** `/:chain_id/api/v2/tokens/:address_hash_param`
- **Base URL:** `https://api.blockscout.com`
- **Official documentation:** [Get Token Info](https://docs.blockscout.com/api-reference/get-token-info)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chain_id` | path | `string` | no | Blockscout chain ID, for example 10 for Optimism. |
| `address_hash_param` | path | `string` | yes | Token contract address. |
