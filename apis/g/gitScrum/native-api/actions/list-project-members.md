# List Project Members with GitScrum

Retrieves members of a GitScrum project.

## Endpoint

- **Method:** `GET`
- **Path:** `/project-members/:projectSlug/members`
- **Base URL:** `https://services.gitscrum.com`
- **Official documentation:** [List Project Members](https://docs.gitscrum.com/en/api/project-members)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `company_slug` | query | `string` | no |
| `project_slug` | path | `string` | no |
