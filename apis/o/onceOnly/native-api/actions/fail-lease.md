# Fail Lease with OnceOnly

Marks an AI lease as failed in OnceOnly.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/ai/fail`
- **Base URL:** `https://api.onceonly.tech`
- **Official documentation:** [Fail Lease](https://docs.onceonly.tech/reference/ai/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | body | `string` | yes | Lease key to fail. |
| `lease_id` | body | `string` | yes | Active lease id. |
| `error_code` | body | `string` | yes | Provider error code to persist. |
