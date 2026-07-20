# Get Block Transactions with Blockscout

Retrieves transactions for a block from Blockscout.

## Endpoint

- **Method:** `GET`
- **Path:** `/:chain_id/api/v2/blocks/:block_hash_or_number_param/transactions`
- **Base URL:** `https://api.blockscout.com`
- **Official documentation:** [Get Block Transactions](https://docs.blockscout.com/api-reference/get-block-transactions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chain_id` | path | `string` | no | Blockscout chain ID, for example 10 for Optimism. |
| `block_hash_or_number_param` | path | `string` | yes | Block number or hash to retrieve transactions for. |
