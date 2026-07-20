# Get Address Token Balances with Blockscout

Retrieves token balances for an address from Blockscout.

## Endpoint

- **Method:** `GET`
- **Path:** `/:chain_id/api/v2/addresses/:address_hash_param/tokens`
- **Base URL:** `https://api.blockscout.com`
- **Official documentation:** [Get Address Token Balances](https://docs.blockscout.com/api-reference/get-all-tokens-balances-for-the-address)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chain_id` | path | `string` | no | Blockscout chain ID, for example 10 for Optimism. |
| `address_hash_param` | path | `string` | yes | Address hash to retrieve token balances for. |
