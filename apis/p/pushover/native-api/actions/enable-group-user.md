# Enable Group User with Pushover

## Endpoint

- **Method:** `POST`
- **Path:** `/groups/:group/enable_user.json`
- **Base URL:** `https://api.pushover.net/1`
- **Official documentation:** [Enable Group User](https://pushover.net/api/groups#enable_user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group` | path | `string` | yes | Delivery group key identifying which group to modify. |
| `user` | query | `string` | yes | Pushover user key to re-enable within the group. |
| `device` | query | `string` | no | Optional device name to match when re-enabling the user in the group. |
