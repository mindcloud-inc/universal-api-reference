# Get a user's task list with Asana

Retrieves a user's task list from Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `users/:user_gid/user_task_list`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get a user's task list](https://developers.asana.com/reference/getusertasklistforuser)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `opt_fields[]` | query | `array<string>` | no | — |
| `user_gid` | path | `string` | yes | Path parameter: user_gid |
