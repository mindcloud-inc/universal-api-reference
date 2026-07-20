# Delete Project Version with MantisBT

Deletes a project version from MantisBT.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/projects/{project_id}/versions/{version_id}`
- **Base URL:** `{baseUrl}/api/rest`
- **Official documentation:** [Delete Project Version](https://github.com/mantisbt/mantisbt/blob/release-2.28.0/api/rest/mantisbt_openapi.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `number` | yes | ID of the project that owns the version |
| `version_id` | path | `number` | yes | ID of the version to delete |
