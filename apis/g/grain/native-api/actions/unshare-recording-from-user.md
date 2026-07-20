# Unshare Recording from User with Grain

Unshares a recording from a user in Grain.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v2/recordings/:recording_id/users/:user_id`
- **Base URL:** `https://api.grain.com/_/public-api`
- **Official documentation:** [Unshare Recording from User](https://developers.grain.com/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `recording_id` | path | `list<string>` | yes |
| `user_id` | path | `list<string>` | yes |
