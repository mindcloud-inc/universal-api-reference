# Get Task with GitScrum

Retrieves details for a specific GitScrum task.

## Endpoint

- **Method:** `GET`
- **Path:** `/tasks/:uuid`
- **Base URL:** `https://services.gitscrum.com`
- **Official documentation:** [Get Task](https://docs.gitscrum.com/en/api/tasks)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `company_slug` | query | `string` | no |
| `project_slug` | query | `string` | no |
| `uuid` | path | `string` | no |
