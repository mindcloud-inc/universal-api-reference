# List Todos with Basecamp

Retrieves to-dos from a Basecamp to-do list.

## Endpoint

- **Method:** `GET`
- **Path:** `/:accountId/todolists/:todolistId/todos.json`
- **Base URL:** `https://3.basecampapi.com`
- **Official documentation:** [List Todos](https://github.com/basecamp/bc3-api/blob/master/sections/todos.md#get-to-dos)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | Basecamp account ID (numeric string). |
| `todolistId` | path | `number` | yes | To-do list ID returned by List Todolists. |
| `status` | query | `list<string>` | no | Optional todo status selector. Accepted values: `active`, `archived`, `trashed`. |
| `completed` | query | `boolean` | no | Optional completion-state selector. |
