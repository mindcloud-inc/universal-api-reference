# Set Group Property Once with Mixpanel

Sets a group property once in Mixpanel.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.mixpanel.com/groups`
- **Base URL:** `https://mixpanel.com/api`
- **Official documentation:** [Set Group Property Once](https://developer.mixpanel.com/reference/group-set-property-once)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$group_key` | body | `string` | yes | Group key that identifies the type of group profile to update. |
| `$group_id` | body | `string` | yes | ID of the specific group profile to update. |
| `$set_once` | body | `object` | yes | Object of group profile properties to set only when they do not already exist. |
| `ip` | query | `number` | no | Set to 1 to use the request IP for geolocation updates. |
| `strict` | query | `number` | no | Set to 1 to return validation errors for invalid updates. |
| `verbose` | query | `number` | no | Set to 1 to include verbose validation messages in the response. |
