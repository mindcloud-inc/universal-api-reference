# Update Project with ArcSite

Updates an existing project in ArcSite.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/projects/:projectId`
- **Base URL:** `https://api.arcsite.com/v1`
- **Official documentation:** [Update Project](https://dev.arcsite.com/#update-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_number` | body | `string` | no | Job number of the project. |
| `projectId` | path | `string` | yes | The ID of the project. |
| `name` | body | `string` | yes | Name of the project. |
| `operator` | body | `string` | yes | Valid ArcSite username or email that updates the project. |
