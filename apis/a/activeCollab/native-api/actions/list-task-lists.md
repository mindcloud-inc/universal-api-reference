# List Task Lists with ActiveCollab

Retrieves task lists for a project in ActiveCollab.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/task-lists`
- **Base URL:** `https://app.activecollab.com/:instanceId/api/v1`
- **Official documentation:** [List Task Lists](https://developers.activecollab.com/api-documentation/v1/projects/elements/task-lists/task-lists.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The ActiveCollab project ID. |
