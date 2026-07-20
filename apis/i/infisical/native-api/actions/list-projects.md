# List Projects with Infisical

Retrieves a list of projects from Infisical.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/projects`
- **Base URL:** `https://app.infisical.com`
- **Official documentation:** [List Projects](https://infisical.com/docs/api-reference/endpoints/projects/list-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `includeRoles` | query | `boolean` | no | Whether to include project roles in the response. |
| `type` | query | `string` | no | Optional project type filter. |
