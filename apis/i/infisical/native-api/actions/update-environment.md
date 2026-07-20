# Update Environment with Infisical

Updates an existing environment in an Infisical project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/projects/:projectId/environments/:id`
- **Base URL:** `https://app.infisical.com`
- **Official documentation:** [Update Environment](https://infisical.com/docs/api-reference/endpoints/environments/update)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `projectId` | path | `string` | yes |
| `id` | path | `string` | yes |
| `name` | body | `string` | yes |
