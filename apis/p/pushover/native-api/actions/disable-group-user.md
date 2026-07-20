# Disable Group User with Pushover

## Endpoint

- **Method:** `POST`
- **Path:** `/groups/:group/disable_user.json`
- **Base URL:** `https://api.pushover.net/1`
- **Official documentation:** [Disable Group User](https://pushover.net/api/groups#disable_user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group` | path | `string` | yes | Delivery group key identifying which group to modify. |
| `user` | query | `string` | yes | Pushover user key to disable within the group. |
| `device` | query | `string` | no | Optional device name to match when disabling the user in the group. |
