# Update Project with Paymo

Updates an existing project in Paymo.

## Endpoint

- **Method:** `PUT`
- **Path:** `projects/:projectId`
- **Base URL:** `https://app.paymoapp.com/api/`
- **Official documentation:** [Update Project](https://github.com/paymo-org/api/blob/master/sections/projects.md#updating-a-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `number` | yes | The Paymo project id. |
| `name` | body | `string` | no | Updated project name. |
| `description` | body | `string` | no | Updated project description. |
