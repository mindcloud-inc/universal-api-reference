# Delete Tool with OnceOnly

Deletes a tool from OnceOnly.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/tools/:name`
- **Base URL:** `https://api.onceonly.tech`
- **Official documentation:** [Delete Tool](https://docs.onceonly.tech/reference/tools/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | Tool name. |
| `scope_id` | query | `string` | no | Tool scope. |
