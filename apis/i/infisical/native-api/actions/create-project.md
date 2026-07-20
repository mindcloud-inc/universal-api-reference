# Create Project with Infisical

Creates a new project in Infisical.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/projects`
- **Base URL:** `https://app.infisical.com`
- **Official documentation:** [Create Project](https://infisical.com/docs/api-reference/endpoints/projects/create-project)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `projectName` | body | `string` | yes |
| `slug` | body | `string` | yes |
