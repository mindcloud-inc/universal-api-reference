# Get Project with MantisBT

Retrieves a project from MantisBT by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{project_id}`
- **Base URL:** `{baseUrl}/api/rest`
- **Official documentation:** [Get Project](https://github.com/mantisbt/mantisbt/blob/release-2.28.0/api/rest/mantisbt_openapi.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `number` | yes | ID of the project to retrieve |
