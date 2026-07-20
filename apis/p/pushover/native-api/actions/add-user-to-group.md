# Add User to Group with Pushover

## Endpoint

- **Method:** `POST`
- **Path:** `/groups/:group/add_user.json`
- **Base URL:** `https://api.pushover.net/1`
- **Official documentation:** [Add User to Group](https://pushover.net/api/groups#add_user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group` | path | `string` | yes | Delivery group key identifying which group to modify. |
| `user` | query | `string` | yes | Pushover user key to add to the group. |
| `device` | query | `string` | no | Optional device name to restrict notifications for this group member. |
| `memo` | query | `string` | no | Optional free-text memo associated with the group user. Maximum length: 200. |
