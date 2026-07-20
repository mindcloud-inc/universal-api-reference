# Delete Environment with Infisical

Deletes an existing environment from an Infisical project.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1/projects/:projectId/environments/:id`
- **Base URL:** `https://app.infisical.com`
- **Official documentation:** [Delete Environment](https://infisical.com/docs/api-reference/endpoints/environments/delete)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `projectId` | path | `string` | yes |
| `id` | path | `string` | yes |
