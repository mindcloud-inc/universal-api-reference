# Get Token Transfers by Token with Blockscout

Retrieves transfers for a token from Blockscout.

## Endpoint

- **Method:** `GET`
- **Path:** `/:chain_id/api/v2/tokens/:address_hash_param/transfers`
- **Base URL:** `https://api.blockscout.com`
- **Official documentation:** [Get Token Transfers by Token](https://docs.blockscout.com/api-reference/get-token-token-transfers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chain_id` | path | `string` | no | Blockscout chain ID, for example 10 for Optimism. |
| `address_hash_param` | path | `string` | yes | Token contract address. |
