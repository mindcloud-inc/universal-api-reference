# Create Function with Braintrust

Creates a new function in Braintrust.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/function`
- **Base URL:** `https://api.braintrust.dev`
- **Official documentation:** [Create Function](https://braintrust.dev/docs/api-reference/functions/create-function.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | body | `string` | yes | Project id. |
| `name` | body | `string` | yes | Function name. |
| `slug` | body | `string` | yes | Function slug. |
| `function_data` | body | `object` | yes | Function data object. |
