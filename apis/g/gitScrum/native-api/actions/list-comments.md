# List Comments with GitScrum

Retrieves a list of GitScrum comments.

## Endpoint

- **Method:** `GET`
- **Path:** `/comments`
- **Base URL:** `https://services.gitscrum.com`
- **Official documentation:** [List Comments](https://docs.gitscrum.com/en/api/comments)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `company_slug` | query | `string` | no |
| `project_slug` | query | `string` | no |
| `task_uuid` | query | `string` | no |
