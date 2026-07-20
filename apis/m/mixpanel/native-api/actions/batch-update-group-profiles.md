# Batch Update Group Profiles with Mixpanel

Updates multiple group profiles in Mixpanel.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.mixpanel.com/groups`
- **Base URL:** `https://mixpanel.com/api`
- **Official documentation:** [Batch Update Group Profiles](https://developer.mixpanel.com/reference/group-batch-update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `updates[]` | body | `array<object>` | yes | Array of Mixpanel group profile update objects. Each object must include $token, $group_key, $group_id, and exactly one update operation such as $set or $union. |
| `ip` | query | `number` | no | Set to 1 to use the request IP for geolocation updates. |
| `strict` | query | `number` | no | Set to 1 to return validation errors for invalid updates. |
| `verbose` | query | `number` | no | Set to 1 to include verbose validation messages in the response. |
