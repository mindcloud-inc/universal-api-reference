# Remove from Profile List Property with Mixpanel

Removes values from a user profile list in Mixpanel.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.mixpanel.com/engage`
- **Base URL:** `https://mixpanel.com/api`
- **Official documentation:** [Remove from Profile List Property](https://developer.mixpanel.com/reference/profile-remove-from-list-property)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$distinct_id` | body | `string` | yes | Distinct ID of the user profile to update. |
| `$remove` | body | `object` | yes | Object mapping profile list properties to values to remove. |
| `ip` | query | `number` | no | Set to 1 to use the request IP for geolocation updates. |
| `strict` | query | `number` | no | Set to 1 to return validation errors for invalid updates. |
| `verbose` | query | `number` | no | Set to 1 to include verbose validation messages in the response. |
