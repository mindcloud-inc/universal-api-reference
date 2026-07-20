# Delete Profile Property with Mixpanel

Deletes a user profile property from Mixpanel.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.mixpanel.com/engage`
- **Base URL:** `https://mixpanel.com/api`
- **Official documentation:** [Delete Profile Property](https://developer.mixpanel.com/reference/profile-delete-property)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$distinct_id` | body | `string` | yes | Distinct ID of the user profile to update. |
| `$unset[]` | body | `array<string>` | yes | List of profile property names to delete. |
| `ip` | query | `number` | no | Set to 1 to use the request IP for geolocation updates. |
| `strict` | query | `number` | no | Set to 1 to return validation errors for invalid updates. |
| `verbose` | query | `number` | no | Set to 1 to include verbose validation messages in the response. |
