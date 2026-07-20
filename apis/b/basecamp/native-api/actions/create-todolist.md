# Create Todolist with Basecamp

Creates a new to-do list in a Basecamp to-do set.

## Endpoint

- **Method:** `POST`
- **Path:** `/:accountId/todosets/:todosetId/todolists.json`
- **Base URL:** `https://3.basecampapi.com`
- **Official documentation:** [Create Todolist](https://github.com/basecamp/bc3-api/blob/master/sections/todolists.md#create-a-to-do-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | Basecamp account ID (numeric string). |
| `todosetId` | path | `number` | yes | To-do set ID from the project's dock.todoset entry. |
| `name` | body | `string` | yes | Name of the to-do list. |
| `description` | body | `string` | no | Optional Basecamp rich-text HTML description. |
