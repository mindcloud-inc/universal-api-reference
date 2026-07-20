# Get Sprint Stats with GitScrum

Retrieves statistics for a GitScrum sprint.

## Endpoint

- **Method:** `GET`
- **Path:** `/sprints/:slug/stats`
- **Base URL:** `https://services.gitscrum.com`
- **Official documentation:** [Get Sprint Stats](https://docs.gitscrum.com/en/api/sprints)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `company_slug` | query | `string` | no |
| `project_slug` | query | `string` | no |
| `slug` | path | `string` | no |
