# Update Task with Nutshell

Updates an existing task in Nutshell.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/tasks/:id`
- **Base URL:** `https://app.nutshell.com/rest`
- **Official documentation:** [Update Task](https://developers.nutshell.com/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Nutshell task ID to update. |
| `patches[].op` | body | `string` | no | JSON Patch operation to perform. |
| `patches[].path` | body | `string` | no | JSON Pointer path to update. |
| `patches[].value` | body | `string` | no | Value to apply for the patch operation. |
