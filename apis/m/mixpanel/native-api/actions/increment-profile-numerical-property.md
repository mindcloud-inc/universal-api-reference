# Increment Profile Numerical Property with Mixpanel

Increments a user profile number property in Mixpanel.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.mixpanel.com/engage`
- **Base URL:** `https://mixpanel.com/api`
- **Official documentation:** [Increment Profile Numerical Property](https://developer.mixpanel.com/reference/profile-numerical-add)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$distinct_id` | body | `string` | yes | Distinct ID of the user profile to update. |
| `$add` | body | `object` | yes | Object mapping numeric profile properties to increment amounts. |
| `ip` | query | `number` | no | Set to 1 to use the request IP for geolocation updates. |
| `strict` | query | `number` | no | Set to 1 to return validation errors for invalid updates. |
| `verbose` | query | `number` | no | Set to 1 to include verbose validation messages in the response. |
