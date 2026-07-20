# Update User Profile with Range

Update a user's profile fields with partial profile data.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/users/:userId/profile`
- **Base URL:** `https://api.range.co`
- **Official documentation:** [Update User Profile](https://www.range.co/docs/api#rpc-update-user-profile)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `profile` | body | `object` | no | Full or partial user profile object. |
| `user_id` | path | `string` | no | The Range user ID. |
