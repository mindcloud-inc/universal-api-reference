# Create Project Version with MantisBT

Creates a new project version in MantisBT.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/{project_id}/versions`
- **Base URL:** `{baseUrl}/api/rest`
- **Official documentation:** [Create Project Version](https://github.com/mantisbt/mantisbt/blob/release-2.28.0/api/rest/mantisbt_openapi.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Description of the project version |
| `name` | body | `string` | yes | Name of the version to create |
| `obsolete` | body | `boolean` | no | Whether the version is obsolete |
| `project_id` | path | `number` | yes | ID of the project where the version will be created |
| `released` | body | `boolean` | no | Whether the version is released |
