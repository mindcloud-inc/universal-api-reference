# Get Transaction Token Transfers with Blockscout

Retrieves token transfers for a transaction from Blockscout.

## Endpoint

- **Method:** `GET`
- **Path:** `/:chain_id/api/v2/transactions/:transaction_hash_param/token-transfers`
- **Base URL:** `https://api.blockscout.com`
- **Official documentation:** [Get Transaction Token Transfers](https://docs.blockscout.com/api-reference/get-transaction-token-transfers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chain_id` | path | `string` | no | — |
| `transaction_hash_param` | path | `string` | yes | Transaction hash to retrieve. |
