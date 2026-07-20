# Union Profile List Property with Mixpanel

Unions values into a user profile list in Mixpanel.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.mixpanel.com/engage`
- **Base URL:** `https://mixpanel.com/api`
- **Official documentation:** [Union Profile List Property](https://developer.mixpanel.com/reference/user-profile-union)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$distinct_id` | body | `string` | yes | Distinct ID of the user profile to update. |
| `$union` | body | `object` | yes | Object mapping profile list properties to values that should be unioned. |
| `ip` | query | `number` | no | Set to 1 to use the request IP for geolocation updates. |
| `strict` | query | `number` | no | Set to 1 to return validation errors for invalid updates. |
| `verbose` | query | `number` | no | Set to 1 to include verbose validation messages in the response. |
