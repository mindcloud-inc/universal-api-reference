# Get Task by Code with GitScrum

Retrieves a GitScrum task by code.

## Endpoint

- **Method:** `GET`
- **Path:** `/tasks/by-code/:code`
- **Base URL:** `https://services.gitscrum.com`
- **Official documentation:** [Get Task by Code](https://docs.gitscrum.com/en/api/tasks)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `code` | path | `string` | no |
| `company_slug` | query | `string` | no |
| `project_slug` | query | `string` | no |
