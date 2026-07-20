# Create User with Sendbird

## Endpoint

- **Method:** `POST`
- **Path:** `/users`
- **Base URL:** `https://api-{applicationId}.sendbird.com/v3`
- **Official documentation:** [Create User](https://docs.sendbird.com/docs/chat/platform-api/v3/user/managing-users/create-a-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `nickname` | body | `string` | no | The user's nickname. |
| `profile_url` | body | `string` | no | The profile image URL. |
| `user_id` | body | `string` | yes | The unique ID for the user. |
