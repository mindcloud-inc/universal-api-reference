# Get Transaction Internal Transactions with Blockscout

Retrieves internal transactions for a transaction from Blockscout.

## Endpoint

- **Method:** `GET`
- **Path:** `/:chain_id/api/v2/transactions/:transaction_hash_param/internal-transactions`
- **Base URL:** `https://api.blockscout.com`
- **Official documentation:** [Get Transaction Internal Transactions](https://docs.blockscout.com/api-reference/get-transaction-internal-transactions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chain_id` | path | `string` | no | — |
| `transaction_hash_param` | path | `string` | yes | Transaction hash to retrieve. |
