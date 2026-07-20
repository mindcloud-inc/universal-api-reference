# Check Lock with OnceOnly

Checks an idempotency lock in OnceOnly.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/check-lock`
- **Base URL:** `https://api.onceonly.tech`
- **Official documentation:** [Check Lock](https://docs.onceonly.tech/reference/idempotency/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | body | `string` | yes | Unique idempotency key for the action. |
| `ttl` | body | `number` | no | Lock duration in seconds. |
| `metadata` | body | `object` | no | Optional metadata object stored with the lock. |
