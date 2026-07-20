# Complete Todo with Basecamp

Marks a to-do as completed in Basecamp.

## Endpoint

- **Method:** `POST`
- **Path:** `/:accountId/todos/:todoId/completion.json`
- **Base URL:** `https://3.basecampapi.com`
- **Official documentation:** [Complete Todo](https://github.com/basecamp/bc3-api/blob/master/sections/todos.md#complete-a-to-do)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `accountId` | path | `string` | yes |
| `todoId` | path | `number` | yes |
