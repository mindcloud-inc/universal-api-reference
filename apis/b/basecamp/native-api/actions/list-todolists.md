# List Todolists with Basecamp

Retrieves to-do lists from a Basecamp to-do set.

## Endpoint

- **Method:** `GET`
- **Path:** `/:accountId/todosets/:todosetId/todolists.json`
- **Base URL:** `https://3.basecampapi.com`
- **Official documentation:** [List Todolists](https://github.com/basecamp/bc3-api/blob/master/sections/todolists.md#get-to-do-lists)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | Basecamp account ID (numeric string). |
| `todosetId` | path | `number` | yes | To-do set ID from the project's dock.todoset entry. |
| `status` | query | `list<string>` | no | Optional todolist status selector. Accepted values: `active`, `archived`, `trashed`. |
