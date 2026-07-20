# Get Todo with Basecamp

Retrieves a to-do from Basecamp.

## Endpoint

- **Method:** `GET`
- **Path:** `/:accountId/todos/:todoId.json`
- **Base URL:** `https://3.basecampapi.com`
- **Official documentation:** [Get Todo](https://github.com/basecamp/bc3-api/blob/master/sections/todos.md#get-a-to-do)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | Basecamp account ID (numeric string). |
| `todoId` | path | `number` | yes | To-do ID returned by List Todos or Create Todo. |
