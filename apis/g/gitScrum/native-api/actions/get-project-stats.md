# Get Project Stats with GitScrum

Retrieves statistics for a specific GitScrum project.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:slug/stats`
- **Base URL:** `https://services.gitscrum.com`
- **Official documentation:** [Get Project Stats](https://docs.gitscrum.com/en/api/projects)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `company_slug` | query | `string` | yes |
| `slug` | path | `string` | yes |
