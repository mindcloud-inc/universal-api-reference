# Create Project with Scaleway

Creates a new project in Scaleway.

## Endpoint

- **Method:** `POST`
- **Path:** `/account/v3/projects`
- **Base URL:** `https://api.scaleway.com`
- **Official documentation:** [Create Project](https://www.scaleway.com/en/developers/api/account/project-api/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `organization_id` | body | `string` | yes |
