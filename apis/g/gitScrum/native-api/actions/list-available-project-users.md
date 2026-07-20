# List Available Project Users with GitScrum

Retrieves available users for a GitScrum project.

## Endpoint

- **Method:** `GET`
- **Path:** `/project-members/:projectSlug/available-users`
- **Base URL:** `https://services.gitscrum.com`
- **Official documentation:** [List Available Project Users](https://docs.gitscrum.com/en/api/project-members)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `company_slug` | query | `string` | no |
| `project_slug` | path | `string` | no |
