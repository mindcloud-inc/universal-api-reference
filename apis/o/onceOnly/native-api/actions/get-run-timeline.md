# Get Run Timeline with OnceOnly

Retrieves a run timeline from OnceOnly.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/runs/:run_id`
- **Base URL:** `https://api.onceonly.tech`
- **Official documentation:** [Get Run Timeline](https://docs.onceonly.tech/reference/runs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `run_id` | path | `string` | yes | Run id to inspect. |
| `limit` | query | `number` | no | Events per page. |
| `offset` | query | `number` | no | Pagination offset. |
