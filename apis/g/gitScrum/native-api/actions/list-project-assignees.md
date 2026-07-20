# List Project Assignees with GitScrum

Retrieves assignees for a GitScrum project.

## Endpoint

- **Method:** `GET`
- **Path:** `/project-members/:projectSlug/assignees`
- **Base URL:** `https://services.gitscrum.com`
- **Official documentation:** [List Project Assignees](https://docs.gitscrum.com/en/api/project-members)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `company_slug` | query | `string` | no |
| `project_slug` | path | `string` | no |
