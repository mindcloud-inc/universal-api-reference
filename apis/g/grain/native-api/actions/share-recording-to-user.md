# Share Recording to User with Grain

Shares a recording with a user in Grain.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/recordings/:recording_id/users`
- **Base URL:** `https://api.grain.com/_/public-api`
- **Official documentation:** [Share Recording to User](https://developers.grain.com/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `recording_id` | path | `list<string>` | yes |
| `user_id` | body | `list<string>` | yes |
