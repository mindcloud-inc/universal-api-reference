# Update Function with Braintrust

Updates an existing function in Braintrust.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/function/:function_id`
- **Base URL:** `https://api.braintrust.dev`
- **Official documentation:** [Update Function](https://braintrust.dev/docs/api-reference/functions/partially-update-function.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `function_id` | path | `string` | yes | Function id. |
| `description` | body | `string` | no | Updated function description. |
| `prompt_data` | body | `object` | no | Prompt data object. |
