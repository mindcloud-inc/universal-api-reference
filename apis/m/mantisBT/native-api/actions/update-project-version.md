# Update Project Version with MantisBT

Updates an existing project version in MantisBT.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/projects/{project_id}/versions/{version_id}`
- **Base URL:** `{baseUrl}/api/rest`
- **Official documentation:** [Update Project Version](https://github.com/mantisbt/mantisbt/blob/release-2.28.0/api/rest/mantisbt_openapi.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `obsolete` | body | `boolean` | yes | Whether the version should be marked obsolete |
| `project_id` | path | `number` | yes | ID of the project that owns the version |
| `version_id` | path | `number` | yes | ID of the version to update |
