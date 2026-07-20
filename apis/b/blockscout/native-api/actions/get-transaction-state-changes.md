# Get Transaction State Changes with Blockscout

Retrieves state changes for a transaction from Blockscout.

## Endpoint

- **Method:** `GET`
- **Path:** `/:chain_id/api/v2/transactions/:transaction_hash_param/state-changes`
- **Base URL:** `https://api.blockscout.com`
- **Official documentation:** [Get Transaction State Changes](https://docs.blockscout.com/api-reference/get-transaction-state-changes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chain_id` | path | `string` | no | — |
| `transaction_hash_param` | path | `string` | yes | Transaction hash to retrieve. |
