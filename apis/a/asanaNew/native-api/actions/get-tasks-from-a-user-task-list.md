# Get tasks from a user task list with Asana

Retrieves tasks from a user task list in Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `user_task_lists/:user_task_list_gid/tasks`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get tasks from a user task list](https://developers.asana.com/reference/gettasksforusertasklist)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `completed_since` | query | `string` | no | Asana completed since parameter. |
| `user_task_list_gid` | path | `string` | yes | Asana user task list gid parameter. |
| `opt_pretty` | query | `boolean` | no | Asana opt pretty parameter. |
| `limit` | query | `number` | no | Asana limit parameter. |
| `offset` | query | `string` | no | Asana offset parameter. |
| `opt_fields` | query | `list<string>` | no | Asana opt fields parameter. |
