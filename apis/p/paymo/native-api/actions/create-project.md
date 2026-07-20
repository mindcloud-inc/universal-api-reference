# Create Project with Paymo

Creates a project in Paymo.

## Endpoint

- **Method:** `POST`
- **Path:** `projects`
- **Base URL:** `https://app.paymoapp.com/api/`
- **Official documentation:** [Create Project](https://github.com/paymo-org/api/blob/master/sections/projects.md#creating-a-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The project name. |
| `client_id` | body | `number` | no | Optional client id to attach the project to a specific Paymo client. |
| `description` | body | `string` | no | Optional project description. |
