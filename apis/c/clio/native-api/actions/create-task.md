# Create Task with Clio Manage

Creates a new task in Clio Manage.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks.json`
- **Base URL:** `https://app.clio.com/api/v4`
- **Official documentation:** [Create Task](https://docs.developers.clio.com/clio-manage/api-reference/#tag/Tasks/operation/Task%23create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.name` | body | `string` | yes | — |
| `data.description` | body | `string` | yes | — |
| `data.assignee.id` | body | `number` | yes | — |
| `data.assignee.type` | body | `list` | yes | Accepted values: `Contact`, `User`. |
| `data.matter.id` | body | `number` | no | — |
