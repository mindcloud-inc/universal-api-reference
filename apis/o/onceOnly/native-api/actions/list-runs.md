# List Runs with OnceOnly

Retrieves runs from OnceOnly.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/runs`
- **Base URL:** `https://api.onceonly.tech`
- **Official documentation:** [List Runs](https://docs.onceonly.tech/reference/runs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Results per page. |
| `offset` | query | `number` | no | Pagination offset. |
| `q` | query | `string` | no | Optional run_id prefix filter. |
