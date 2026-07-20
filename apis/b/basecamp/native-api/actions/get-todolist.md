# Get Todolist with Basecamp

Retrieves a to-do list from Basecamp.

## Endpoint

- **Method:** `GET`
- **Path:** `/:accountId/todolists/:id.json`
- **Base URL:** `https://3.basecampapi.com`
- **Official documentation:** [Get Todolist](https://github.com/basecamp/bc3-api/blob/master/sections/todolists.md#get-a-to-do-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | Basecamp account ID (numeric string). |
| `id` | path | `number` | yes | To-do list ID returned by List Todolists. |
