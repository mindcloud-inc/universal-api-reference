# Union Group List Property with Mixpanel

Unions values into a group list in Mixpanel.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.mixpanel.com/groups`
- **Base URL:** `https://mixpanel.com/api`
- **Official documentation:** [Union Group List Property](https://developer.mixpanel.com/reference/group-union)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$group_key` | body | `string` | yes | Group key that identifies the type of group profile to update. |
| `$group_id` | body | `string` | yes | ID of the specific group profile to update. |
| `$union` | body | `object` | yes | Object mapping group profile list properties to values that should be unioned. |
| `ip` | query | `number` | no | Set to 1 to use the request IP for geolocation updates. |
| `strict` | query | `number` | no | Set to 1 to return validation errors for invalid updates. |
| `verbose` | query | `number` | no | Set to 1 to include verbose validation messages in the response. |
