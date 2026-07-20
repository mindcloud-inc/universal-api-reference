# Update variable with YepCode

Updates an existing variable in YepCode.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/variables/:id`
- **Base URL:** `https://cloud.yepcode.io/api/{team}/rest`
- **Official documentation:** [Update variable](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Variables/updateVariable)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique identifier of the variable to update. |
| `key` | body | `string` | no | Updated variable key or name. |
| `value` | body | `string` | no | Updated variable value. |
