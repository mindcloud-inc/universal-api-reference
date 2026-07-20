# Get Project Users with MantisBT

Retrieves project users from a MantisBT project.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{project_id}/users`
- **Base URL:** `{baseUrl}/api/rest`
- **Official documentation:** [Get Project Users](https://github.com/mantisbt/mantisbt/blob/release-2.28.0/api/rest/mantisbt_openapi.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `number` | yes | ID of the project whose users to return |
