# Update User with Instabot

Updates an existing user in Instabot.

## Endpoint

- **Method:** `PUT`
- **Path:** `/users/:id`
- **Base URL:** `https://api.instabot.io/v1`
- **Official documentation:** [Update User](https://docs.instabot.io/docs/serverapi-users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Instabot user object identifier. |
| `username` | body | `string` | yes | Unique user name. |
| `name` | body | `string` | no | User display name. |
| `description` | body | `string` | no | User description. |
| `email` | body | `string` | no | User email address. |
