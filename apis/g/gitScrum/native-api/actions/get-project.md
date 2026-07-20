# Get Project with GitScrum

Retrieves details for a specific GitScrum project.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:slug`
- **Base URL:** `https://services.gitscrum.com`
- **Official documentation:** [Get Project](https://docs.gitscrum.com/en/api/projects)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `company_slug` | query | `string` | yes |
| `slug` | path | `string` | yes |
