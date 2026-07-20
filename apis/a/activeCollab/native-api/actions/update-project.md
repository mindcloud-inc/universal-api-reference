# Update Project with ActiveCollab

Updates an existing project in ActiveCollab.

## Endpoint

- **Method:** `PUT`
- **Path:** `/projects/:projectId`
- **Base URL:** `https://app.activecollab.com/:instanceId/api/v1`
- **Official documentation:** [Update Project](https://developers.activecollab.com/api-documentation/v1/projects/projects.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The project ID. |
| `name` | body | `string` | no | The updated project name. |
