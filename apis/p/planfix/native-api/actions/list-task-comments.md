# List Task Comments with Planfix

Retrieves comments for a task in Planfix.

## Endpoint

- **Method:** `POST`
- **Path:** `/task/:id/comments/list`
- **Base URL:** `{accountBaseUrl}/rest`
- **Official documentation:** [List Task Comments](https://help.planfix.com/restapidocs/#/Task/get-task-comments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Task identifier to read comments for. |
| `fields` | body | `string` | no | Comma-delimited comment fields to return. |
| `pageSize` | body | `number` | no | Number of comments to return. |
| `offset` | body | `number` | no | Comment list offset. |
| `typeList` | body | `string` | no | Comment list type to return. |
