# Get Todoset with Basecamp

Retrieves a to-do set from Basecamp.

## Endpoint

- **Method:** `GET`
- **Path:** `/:accountId/todosets/:todosetId.json`
- **Base URL:** `https://3.basecampapi.com`
- **Official documentation:** [Get Todoset](https://github.com/basecamp/bc3-api/blob/master/sections/todosets.md#get-to-do-set)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | Basecamp account ID (numeric string). |
| `todosetId` | path | `number` | yes | To-do set ID from the project's dock.todoset entry. |
