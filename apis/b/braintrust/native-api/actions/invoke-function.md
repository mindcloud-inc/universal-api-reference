# Invoke Function with Braintrust

Invokes a function in Braintrust.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/function/:function_id/invoke`
- **Base URL:** `https://api.braintrust.dev`
- **Official documentation:** [Invoke Function](https://braintrust.dev/docs/api-reference/functions/invoke-function.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `function_id` | path | `string` | yes | Function id. |
| `input` | body | `string` | no | Function input. |
