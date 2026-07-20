# Complete Lease with OnceOnly

Completes an AI lease in OnceOnly.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/ai/complete`
- **Base URL:** `https://api.onceonly.tech`
- **Official documentation:** [Complete Lease](https://docs.onceonly.tech/reference/ai/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | body | `string` | yes | Lease key to complete. |
| `lease_id` | body | `string` | yes | Active lease id. |
| `result` | body | `object` | yes | Completion result object to store. |
| `result_hash` | body | `string` | no | Optional hash for the result payload. |
