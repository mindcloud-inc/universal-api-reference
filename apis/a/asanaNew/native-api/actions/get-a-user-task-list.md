# Get a user task list with Asana

Retrieves a user task list from Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `user_task_lists/:user_task_list_gid`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get a user task list](https://developers.asana.com/reference/getusertasklist)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `user_task_list_gid` | path | `string` | yes |
| `opt_pretty` | query | `boolean` | no |
| `opt_fields` | query | `list<string>` | no |
