# Create User with Instabot

Creates a new user in Instabot.

## Endpoint

- **Method:** `POST`
- **Path:** `/users`
- **Base URL:** `https://api.instabot.io/v1`
- **Official documentation:** [Create User](https://docs.instabot.io/docs/serverapi-users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `username` | body | `string` | yes | Unique Instabot username for the new user. |
| `userpassword` | body | `string` | yes | Initial password for the new user. |
| `email` | body | `string` | no | Email address for the new user. |
