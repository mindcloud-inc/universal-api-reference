# Create Lease with OnceOnly

Creates an AI lease in OnceOnly.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/ai/lease`
- **Base URL:** `https://api.onceonly.tech`
- **Official documentation:** [Create Lease](https://docs.onceonly.tech/reference/ai/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | body | `string` | yes | Unique lease key. |
| `ttl` | body | `number` | no | Lease duration in seconds. |
| `metadata` | body | `object` | no | Optional metadata object for the lease. |
