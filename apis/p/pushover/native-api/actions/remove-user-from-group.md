# Remove User from Group with Pushover

## Endpoint

- **Method:** `POST`
- **Path:** `/groups/:group/remove_user.json`
- **Base URL:** `https://api.pushover.net/1`
- **Official documentation:** [Remove User from Group](https://pushover.net/api/groups#remove_user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group` | path | `string` | yes | Delivery group key identifying which group to modify. |
| `user` | query | `string` | yes | Pushover user key to remove from the group. |
| `device` | query | `string` | no | Optional device name to match when removing the user from the group. |
