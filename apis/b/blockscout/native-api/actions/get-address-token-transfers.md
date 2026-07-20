# Get Address Token Transfers with Blockscout

Retrieves token transfers for an address from Blockscout.

## Endpoint

- **Method:** `GET`
- **Path:** `/:chain_id/api/v2/addresses/:address_hash_param/token-transfers`
- **Base URL:** `https://api.blockscout.com`
- **Official documentation:** [Get Address Token Transfers](https://docs.blockscout.com/api-reference/get-address-token-transfers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chain_id` | path | `string` | no | Blockscout chain ID, for example 10 for Optimism. |
| `address_hash_param` | path | `string` | yes | Address hash to retrieve token transfers for. |
