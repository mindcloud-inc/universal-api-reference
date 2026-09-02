# Get User with ClickUp

Retrieves details for a ClickUp Workspace user.

## Endpoint

- **Method:** `GET`
- **Path:** `team/:team_id/user/:user_id`
- **Base URL:** `https://api.clickup.com/api/v2/`
- **Official documentation:** [Get User](https://developer.clickup.com/reference/getuser)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `include_shared` | query | `boolean` | no |
| `team_id` | path | `list` | yes |
| `user_id` | path | `number` | yes |
