# Cancel Lease with OnceOnly

Cancels an AI lease in OnceOnly.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/ai/cancel`
- **Base URL:** `https://api.onceonly.tech`
- **Official documentation:** [Cancel Lease](https://docs.onceonly.tech/reference/ai/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | body | `string` | yes | Lease key to cancel. |
| `lease_id` | body | `string` | yes | Active lease id. |
| `reason` | body | `string` | no | Optional cancellation reason. |
