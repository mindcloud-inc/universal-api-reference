# Get Blocks with Blockscout

Retrieves blockchain block listings from Blockscout.

## Endpoint

- **Method:** `GET`
- **Path:** `/:chain_id/api/v2/blocks`
- **Base URL:** `https://api.blockscout.com`
- **Official documentation:** [Get Blocks](https://docs.blockscout.com/api-reference/get-blocks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chain_id` | path | `string` | no | Blockscout chain ID path segment; defaults to Optimism (10). |
| `type` | query | `string` | no | — |
