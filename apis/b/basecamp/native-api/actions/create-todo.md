# Create Todo with Basecamp

Creates a new to-do in a Basecamp to-do list.

## Endpoint

- **Method:** `POST`
- **Path:** `/:accountId/todolists/:todolistId/todos.json`
- **Base URL:** `https://3.basecampapi.com`
- **Official documentation:** [Create Todo](https://github.com/basecamp/bc3-api/blob/master/sections/todos.md#create-a-to-do)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | — |
| `todolistId` | path | `number` | yes | — |
| `content` | body | `string` | yes | — |
| `description` | body | `string` | no | — |
| `assignee_ids` | body | `list<number>` | no | Send multiple values as a array. |
| `due_on` | body | `date` | no | — |
| `starts_on` | body | `date` | no | — |
| `completion_subscriber_ids` | body | `list<number>` | no | Send multiple values as a array. |
| `notify` | body | `boolean` | no | — |
