# Update Project with Infisical

Updates an existing project in Infisical.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/projects/:projectId`
- **Base URL:** `https://app.infisical.com`
- **Official documentation:** [Update Project](https://infisical.com/docs/api-reference/endpoints/projects/update-project)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `projectId` | path | `string` | yes |
| `name` | body | `string` | yes |
