# List Discussions with ActiveCollab

Retrieves discussions for a project in ActiveCollab.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/discussions`
- **Base URL:** `https://app.activecollab.com/:instanceId/api/v1`
- **Official documentation:** [List Discussions](https://developers.activecollab.com/api-documentation/v1/projects/elements/discussions.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The ActiveCollab project ID. |
