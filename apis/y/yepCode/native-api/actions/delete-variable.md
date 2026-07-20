# Delete variable with YepCode

Deletes an existing variable from YepCode.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/variables/:id`
- **Base URL:** `https://cloud.yepcode.io/api/{team}/rest`
- **Official documentation:** [Delete variable](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Variables/deleteVariable)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique identifier of the variable to delete. |
