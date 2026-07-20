# Get Project Handlers with MantisBT

Retrieves available project handlers from MantisBT.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{project_id}/handlers`
- **Base URL:** `{baseUrl}/api/rest`
- **Official documentation:** [Get Project Handlers](https://github.com/mantisbt/mantisbt/blob/release-2.28.0/api/rest/mantisbt_openapi.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `number` | yes | ID of the project whose assignable handlers to return |
