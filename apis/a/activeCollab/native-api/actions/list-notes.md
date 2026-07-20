# List Notes with ActiveCollab

Retrieves notes for a project in ActiveCollab.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/notes`
- **Base URL:** `https://app.activecollab.com/:instanceId/api/v1`
- **Official documentation:** [List Notes](https://developers.activecollab.com/api-documentation/v1/projects/elements/notes/notes.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The ActiveCollab project ID. |
