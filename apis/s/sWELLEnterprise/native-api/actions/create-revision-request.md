# Create Revision Request with SWELLEnterprise

Creates a revision request in SWELLEnterprise.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/projects/:project_id/revision-requests`
- **Base URL:** `https://dashboard.swellsystem.com/api/v1`
- **Official documentation:** [Create Revision Request](https://dashboard.swellsystem.com/docs#endpoints-POSTapi-v1-projects-projects--project_id--revision-requests)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `number` | yes | The ID of the project. |
| `title` | body | `string` | yes | The revision request title. |
