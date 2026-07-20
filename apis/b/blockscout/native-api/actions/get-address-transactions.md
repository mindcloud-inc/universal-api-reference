# Get Address Transactions with Blockscout

Retrieves transactions for an address from Blockscout.

## Endpoint

- **Method:** `GET`
- **Path:** `/:chain_id/api/v2/addresses/:address_hash_param/transactions`
- **Base URL:** `https://api.blockscout.com`
- **Official documentation:** [Get Address Transactions](https://docs.blockscout.com/api-reference/get-address-transactions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chain_id` | path | `string` | no | Blockscout chain ID, for example 10 for Optimism. |
| `address_hash_param` | path | `string` | yes | Address hash to retrieve transactions for. |
