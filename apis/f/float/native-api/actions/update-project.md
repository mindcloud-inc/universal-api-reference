# Update Project with Float

Updates an existing project in Float.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/projects/:project_id`
- **Base URL:** `https://api.float.com/v3`
- **Official documentation:** [Update Project](https://developer.float.com/api_reference.html#Projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `notes` | body | `string` | no | Notes for this project |
| `project_id` | path | `number` | yes | The project's ID |
