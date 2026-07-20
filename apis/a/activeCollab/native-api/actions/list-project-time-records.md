# List Project Time Records with ActiveCollab

Retrieves time records for a project in ActiveCollab.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/time-records`
- **Base URL:** `https://app.activecollab.com/:instanceId/api/v1`
- **Official documentation:** [List Project Time Records](https://developers.activecollab.com/api-documentation/v1/projects/elements/time-records/time-records.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The ActiveCollab project ID. |
