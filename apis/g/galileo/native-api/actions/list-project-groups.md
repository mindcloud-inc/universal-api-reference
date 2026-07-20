# List Project Groups with Galileo

Finds group collaborators for a Galileo project.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/projects/:project_id/groups`
- **Base URL:** `https://api.galileo.ai`
- **Official documentation:** [List Project Groups](https://docs.galileo.ai/api-reference/projects/list-group-project-collaborators)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Galileo project UUID. |
