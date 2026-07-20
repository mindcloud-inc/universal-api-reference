# List Tasks with GitScrum

Retrieves a list of GitScrum tasks.

## Endpoint

- **Method:** `GET`
- **Path:** `/tasks`
- **Base URL:** `https://services.gitscrum.com`
- **Official documentation:** [List Tasks](https://docs.gitscrum.com/en/api/tasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_slug` | query | `string` | no | — |
| `per_page` | query | `string` | no | Maximum number of tasks to return. |
| `project_slug` | query | `string` | no | — |
