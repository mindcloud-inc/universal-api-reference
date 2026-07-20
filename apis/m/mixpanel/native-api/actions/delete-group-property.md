# Delete Group Property with Mixpanel

Deletes a group property from Mixpanel.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.mixpanel.com/groups`
- **Base URL:** `https://mixpanel.com/api`
- **Official documentation:** [Delete Group Property](https://developer.mixpanel.com/reference/group-delete-property)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$group_key` | body | `string` | yes | Group key that identifies the type of group profile to update. |
| `$group_id` | body | `string` | yes | ID of the specific group profile to update. |
| `$unset[]` | body | `array<string>` | yes | List of group profile property names to delete. |
| `ip` | query | `number` | no | Set to 1 to use the request IP for geolocation updates. |
| `strict` | query | `number` | no | Set to 1 to return validation errors for invalid updates. |
| `verbose` | query | `number` | no | Set to 1 to include verbose validation messages in the response. |
