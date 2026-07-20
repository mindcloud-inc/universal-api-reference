# Extend Lease with OnceOnly

Extends an AI lease in OnceOnly.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/ai/extend`
- **Base URL:** `https://api.onceonly.tech`
- **Official documentation:** [Extend Lease](https://docs.onceonly.tech/reference/ai/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | body | `string` | yes | Lease key to extend. |
| `lease_id` | body | `string` | yes | Active lease id. |
| `ttl` | body | `number` | yes | New lease duration in seconds. |
