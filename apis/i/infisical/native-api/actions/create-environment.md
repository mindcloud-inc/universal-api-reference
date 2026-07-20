# Create Environment with Infisical

Creates a new environment in an Infisical project.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/projects/:projectId/environments`
- **Base URL:** `https://app.infisical.com`
- **Official documentation:** [Create Environment](https://infisical.com/docs/api-reference/endpoints/environments/create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `projectId` | path | `string` | yes |
| `name` | body | `string` | yes |
| `slug` | body | `string` | yes |
