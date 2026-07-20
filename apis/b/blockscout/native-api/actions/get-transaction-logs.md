# Get Transaction Logs with Blockscout

Retrieves logs for a transaction from Blockscout.

## Endpoint

- **Method:** `GET`
- **Path:** `/:chain_id/api/v2/transactions/:transaction_hash_param/logs`
- **Base URL:** `https://api.blockscout.com`
- **Official documentation:** [Get Transaction Logs](https://docs.blockscout.com/api-reference/get-transaction-logs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chain_id` | path | `string` | no | — |
| `transaction_hash_param` | path | `string` | yes | Transaction hash to retrieve. |
