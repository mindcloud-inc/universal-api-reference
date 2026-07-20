# Update Workflow with Userback

Updates a workflow in Userback.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/workflow/:id`
- **Base URL:** `https://rest.userback.io/1.0`
- **Official documentation:** [Update Workflow](https://docs.userback.io/reference/updateworkflow)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The workflow ID to update. |
| `name` | body | `string` | yes | The updated workflow name. |
| `color` | body | `string` | yes | The updated workflow color in hex format. |
