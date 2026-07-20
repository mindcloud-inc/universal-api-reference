# Get Tool with OnceOnly

Retrieves a tool from OnceOnly.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/tools/:name`
- **Base URL:** `https://api.onceonly.tech`
- **Official documentation:** [Get Tool](https://docs.onceonly.tech/reference/tools/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | Tool name. |
| `scope_id` | query | `string` | no | Tool scope. |
