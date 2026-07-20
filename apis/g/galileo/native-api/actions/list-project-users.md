# List Project Users with Galileo

Finds user collaborators for a Galileo project.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/projects/:project_id/users`
- **Base URL:** `https://api.galileo.ai`
- **Official documentation:** [List Project Users](https://docs.galileo.ai/api-reference/projects/list-user-project-collaborators)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Galileo project UUID. |
