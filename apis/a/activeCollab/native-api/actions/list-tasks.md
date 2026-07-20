# List Tasks with ActiveCollab

Retrieves tasks for a project in ActiveCollab.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/tasks`
- **Base URL:** `https://app.activecollab.com/:instanceId/api/v1`
- **Official documentation:** [List Tasks](https://developers.activecollab.com/api-documentation/v1/projects/elements/tasks/tasks.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The ActiveCollab project ID. |
