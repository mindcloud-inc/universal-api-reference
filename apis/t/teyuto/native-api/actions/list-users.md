# List Users with Teyuto

Retrieves all users from a Teyuto account.

## Endpoint

- **Method:** `GET`
- **Path:** `/users`
- **Base URL:** `https://api.teyuto.tv/v2`
- **Official documentation:** [List Users](https://apidocs.teyuto.com/api-9259124)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | no | Filter users by email address. |
| `page` | query | `number` | no | Page of users to return. |
| `group_id` | query | `string` | no | Filter users to a specific group. |
| `search` | query | `string` | no | Search users by text. |
| `client_user_id` | query | `string` | no | Filter users by external client user ID. |
