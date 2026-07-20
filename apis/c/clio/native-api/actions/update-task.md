# Update Task with Clio Manage

Updates a task in Clio Manage by task ID.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/tasks/:id.json`
- **Base URL:** `https://app.clio.com/api/v4`
- **Official documentation:** [Update Task](https://docs.developers.clio.com/clio-manage/api-reference/#tag/Tasks/operation/Task%23update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | — |
| `data.name` | body | `string` | no | — |
| `data.description` | body | `string` | no | — |
| `data.status` | body | `list` | no | Accepted values: `complete`, `draft`, `in_progress`, `in_review`, `pending`. |
