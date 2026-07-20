# Get subtasks from a task with Asana

Retrieves subtasks for a task from Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `tasks/:task_gid/subtasks`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get subtasks from a task](https://developers.asana.com/reference/getsubtasksfortask)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_gid` | path | `string` | yes | — |
| `opt_pretty` | query | `boolean` | no | name,completed,notes,due_on,external,num_subtasks,parent,permalink_url Send multiple values as a array. |
| `opt_fields` | query | `list<string>` | no | — |
