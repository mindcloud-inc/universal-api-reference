# Create Project with Float

Creates a new project in Float.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects`
- **Base URL:** `https://api.float.com/v3`
- **Official documentation:** [Create Project](https://developer.float.com/api_reference.html#Projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_id` | body | `number` | no | The ID of the project's client |
| `name` | body | `string` | yes | The name of the project |
