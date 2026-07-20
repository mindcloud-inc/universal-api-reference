# Get Tokens with Blockscout

Retrieves current token listings from Blockscout.

## Endpoint

- **Method:** `GET`
- **Path:** `/:chain_id/api/v2/tokens/`
- **Base URL:** `https://api.blockscout.com`
- **Official documentation:** [Get Tokens](https://docs.blockscout.com/api-reference/get-tokens-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chain_id` | path | `string` | no | Blockscout chain ID, for example 10 for Optimism. |
