# Get Transaction Summary with Blockscout

Retrieves a human-readable transaction summary from Blockscout.

## Endpoint

- **Method:** `GET`
- **Path:** `/:chain_id/api/v2/transactions/:transaction_hash_param/summary`
- **Base URL:** `https://api.blockscout.com`
- **Official documentation:** [Get Transaction Summary](https://docs.blockscout.com/api-reference/get-human-readable-transaction-summary)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chain_id` | path | `string` | no | — |
| `transaction_hash_param` | path | `string` | yes | Transaction hash to retrieve. |
