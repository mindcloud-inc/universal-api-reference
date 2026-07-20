# Get Transaction Info with Blockscout

Retrieves a transaction's details from Blockscout.

## Endpoint

- **Method:** `GET`
- **Path:** `/:chain_id/api/v2/transactions/:transaction_hash_param`
- **Base URL:** `https://api.blockscout.com`
- **Official documentation:** [Get Transaction Info](https://docs.blockscout.com/api-reference/get-transaction-info)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chain_id` | path | `string` | no | — |
| `transaction_hash_param` | path | `string` | yes | Transaction hash to retrieve. |
