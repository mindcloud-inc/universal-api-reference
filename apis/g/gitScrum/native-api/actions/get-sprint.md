# Get Sprint with GitScrum

Retrieves details for a specific GitScrum sprint.

## Endpoint

- **Method:** `GET`
- **Path:** `/sprints/:slug`
- **Base URL:** `https://services.gitscrum.com`
- **Official documentation:** [Get Sprint](https://docs.gitscrum.com/en/api/sprints)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `company_slug` | query | `string` | no |
| `project_slug` | query | `string` | no |
| `slug` | path | `string` | no |
