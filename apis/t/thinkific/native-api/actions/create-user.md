# Create User with Thinkific

Creates a new user in Thinkific.

## Endpoint

- **Method:** `POST`
- **Path:** `/users`
- **Base URL:** `https://api.thinkific.com/api/public/v1`
- **Official documentation:** [Create User](https://developers.thinkific.com/api/api-documentation#/paths/~1users/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | User email address. |
| `first_name` | body | `string` | yes | User first name. |
| `last_name` | body | `string` | yes | User last name. |
| `send_welcome_email` | body | `boolean` | no | Send a welcome email when creating the user. |
